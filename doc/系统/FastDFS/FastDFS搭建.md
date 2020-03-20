# 1. 准备材料
[FastDFS材料下载地址](https://download.csdn.net/download/qq_36325121/11139324)


# 2. 安装libfastcommon-master

## 2.1 解压文件

```sh
upzip libfastcommon-master.zip
```


## 2.2  进入文件，进行编译安装

```shell
#进入文件夹
cd libfastcommon-master
# 编译安装
./make.sh 
./make.sh install
```

# 3. 安装FastDFS
## 3.1 解压
```shell
tar -xvf FastDFS_v5.08.tar.gz
```

## 3.2 进入FastDFS目录，编译安装
```shell
./make.sh 
./make.sh install
```

进入` /etc/fdfs` 会看到三个simple配置文件

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190423170859278.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzI1MTIx,size_16,color_FFFFFF,t_70)


## 3.3 配置tracker
1. 修改配置文件名称

		`cp tracker.conf.sample tracker.conf`

	![在这里插入图片描述](https://img-blog.csdnimg.cn/20190423171302229.png)


2. 修改配置文件部分配置
     `vim tracker.conf`

     ```shell
     # 数据日志保存路径
     base_path=/var/fdfs/tracker
     ```

     **注意** ：设置的日志保存路径必须要存在，负责启动不成功。

3. 启动tracker

     `service fdfs_trackerd start`

     **注意** ：提示启动ok不一定启动成功，需要通过查看端口22122端fdfs_trackerd服务器是否启动。

4. 查看启动
    	
    `netstat -nltp`

    ![在这里插入图片描述](https://img-blog.csdnimg.cn/20190423172217157.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzI1MTIx,size_16,color_FFFFFF,t_70)



## 3.4 配置storage

和配置tracker差不多

1. 修改名称	
	`cp storage.conf.sample storage.conf`
	
2. 修改配置
     	
    `vim storage.conf`
    	

    ```shell
    # 文件保存路径
    base_path=/var/fdfs/storage
    
    #和上面相同，必须保证下面目录存在，不然会启动不了
    store_path0=/var/fdfs/storage
    
    # 设置tracker的地址Ip
    tracker_server=127.0.0.1:22122
    ```

    **注意** ：设置的文件保存路径必须要存在，负责启动不成功。

3. 启动

    `service fdfs_storaged start`

4. 查看

     `ps -ef | grep fdfs`
     	 
     如果没有这三个进程，或者少了，其中一个，就有问题。	
     ![在这里插入图片描述](https://img-blog.csdnimg.cn/20190423173138328.png)


# 4 整合Springboot
通过整合Springboot 测试上传

## 4.1 添加依赖
```xml
<dependency>
            <groupId>com.github.tobato</groupId>
            <artifactId>fastdfs-client</artifactId>
            <version>1.26.1-RELEASE</version>
 </dependency>
```

 	 

## 4.2 添加配置
1. yml文件中添加配置
	
```
	fdfs:
			  # 连接Tracker服务器超时时间
			  connect-timeout: 10000
			  # storage服务器响应的超时时间
			  so-timeout: 3000
			  #  trakcer服务器的数量
			  tracker-list:
			    - 47.97.3.96:22122
			  pool:
			  	# 这句必须加，不然会启动宝座
		    jmx-enabled: false
```


​	
2.  启动类添加
			
	```
	@Import(FdfsClientConfig.class)
	```
	
	![在这里插入图片描述](https://img-blog.csdnimg.cn/20190423174324999.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzI1MTIx,size_16,color_FFFFFF,t_70)


## 4.3 文件上传代码

```java
	import java.io.IOException;
	
	/**
	 * @Auther: Albert
	 * @Date: 2019-04-23 09:40
	 * @Description:
	 */
	@Api(description = "文件上传")
	@RestController()
	@RequestMapping("upload/")
	public class UploadController {
	
	    @Autowired
	    private DefaultFastFileStorageClient fastFileStorageClient;
	
	    @ApiOperation(value = "上传文件",httpMethod = HttpMethodConstants.POST)
	    @RequestMapping("file/")
	    public ResponseBase<String> uploadFile(@ApiParam("文件") @RequestPart("file")MultipartFile file) {
	        try {
	            String originalFilename = file.getOriginalFilename();
	            StorePath storePath = fastFileStorageClient.uploadFile(file.getInputStream(), file.getSize(), originalFilename.substring(originalFilename.lastIndexOf(".") + 1), null);
	            return ResponseBase.ok(JsonUtils.objectToJson(storePath));
	        } catch (IOException e) {
	            e.printStackTrace();
	        }
	        return null;
	    }
	}
```


## 4.4 测试

wagger测试，返回路径，则成功，现在是不能直接访问图片，必须要整合nginx

1. 选择照片上传
		![在这里插入图片描述](https://img-blog.csdnimg.cn/20190423182550666.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzI1MTIx,size_16,color_FFFFFF,t_70)

2. 查看结果

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190423174807795.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzI1MTIx,size_16,color_FFFFFF,t_70)

# 5 整合Nginx
## 5.1 安装fastdfs-nginx-module
1. 进入安装目录，解压
	
		```
	tar -xvf fastdfs-nginx-module_v1.16.tar.gz
	```
	
2. 配置config

    ```
    cd /fastdfs-nginx-module/src/
        # 修改配置
        vim config
        # 执行下面命令（将配置中的/usr/local改为/usr）：
        :%s+/usr/local/+/usr/+g
    ```


3. 配置mod_fastdfs.conf			

    ```shell
    #将mod_fastdfs.conf复制到 /etc/fdfs目录
    sudo cp mod_fastdfs.conf /etc/fdfs/
    # 编辑/etc/fdfs下的该文件
    sudo vim /etc/fdfs/mod_fastdfs.conf		
    #需要修改的配置
    connect_timeout=10                  		# 客户端访问文件连接超时时长（单位：秒）
    tracker_server=127.0.0.1:22122  			# tracker服务IP和端口
    url_have_group_name=true            		# 访问链接前缀加上组名
    store_path0=/var/fdfs/storage        		# 文件存储路径
    ```

4. 复制 FastDFS的部分配置文件到/etc/fdfs目录(这一步必须加)

    1).  进入FastDFS安装目录下面的conf目录

    ![image-20200319103604099](https://tva1.sinaimg.cn/large/00831rSTly1gcz1aikf2mj30q607wta2.jpg)

    2).  将`http.conf` 和`mines.types`文件复制到`/etc/fdfs`

    ```shell
    cp http.conf mime.types /etc/fdfs/
    ```

    `/etc/fdfs`下文件	![image-20200319103835301](https://tva1.sinaimg.cn/large/00831rSTly1gcz1d4jt6jj30si08a75q.jpg)

    

## 5.2 安装Nignx
1. 进入Nginx所在目录，解压
	```
	tar -xvf nginx-1.10.0.tar.gz
	```
	
2. 配置

    ```
    //如果没有安装prec 则需要安装
    yum -y install pcre pcre-devel zlib zlib-devel openssl openssl-devel
    ```

    ```
    ./configure --prefix=/opt/nginx --sbin-path=/usr/bin/nginx --add-module=/usr/local/fastdfs-nginx-module/src
    ```

3. 编译安装

    ```
    make && sudo make install
    ```

4. 修改配置文件

    ```
    #编辑配置文件
    vim  /opt/nginx/conf/nginx.conf
    ```

    把配置改成如下，端口必须和`storage.conf`，里面配置的`http.server_port`一样
    	
    ```
    server {
        listen       8888;
        server_name  localhost;
        location ~/group([0-9])/M00 {
            root /var/fdfs/data;
            ngx_fastdfs_module;
        }
    
        location / {
            root   html;
            index  index.html index.htm;
        }
    
        error_page   500 502 503 504  /50x.html;
        location = /50x.html {
            root   html;
        }
    }
    ```
    
5. 启动查看
    	![在这里插入图片描述](https://img-blog.csdnimg.cn/20190423182159910.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzI1MTIx,size_16,color_FFFFFF,t_70)

6. 测试访问上传图片
   
	文件访问地址：ip:8888/上传文件返回的路径
	
	http://47.96.2.97:8888/group1/M00/00/00/rBB3A1y-tLmAEs92AAE2Xb2fD-w204.jpg
	  	![在这里插入图片描述](https://img-blog.csdnimg.cn/20190423182310317.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzI1MTIx,size_16,color_FFFFFF,t_70)
