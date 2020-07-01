# Java环境配置



## Centos7配置Jdk1.8

### 1. 下载JDK

[官方JDK1.8下载地址](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

我选择是tar.gz格式。

注意查看Centos系统多少位，如果是32位就选择x86的。

![image-20200319093124879](https://tva1.sinaimg.cn/large/007S8ZIlly1ggan529zeyj31h40u0n7b.jpg)

### 2. 解压
`tar -zxvf jdk-8u201-linux-x64.tar.gz`
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190307130951248.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzI1MTIx,size_16,color_FFFFFF,t_70)

### 3. 环境配置

1. 编辑/etc/profile文件

   `vim /etc/profile`

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190307131253869.png)

2. 添加如下配置

   ```sh
   # 所配置jdk的路径
   export JAVA_HOME=/usr/local/java/jdk1.8.0_201
   export JRE_HOME=${JAVA_HOME}/jre
   export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
   export PATH=${JAVA_HOME}/bin:$PATH
   ```

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190307131521803.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MzI1MTIx,size_16,color_FFFFFF,t_70)

3. 执行` source /etc/profile`

### 4. 验证

​	输入` java -version`查看版本。显示如下，完成。

![image-20200319093948350](https://tva1.sinaimg.cn/large/00831rSTly1gcyzrhvpnwj30ti02w0t6.jpg)

