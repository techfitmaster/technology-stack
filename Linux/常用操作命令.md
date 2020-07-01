# curl

> 基于网络协议，对指定URL进行网络传输
>
> curl支持的通讯协定有DICT, FILE, FTP, FTPS, GOPHER, HTTP, HTTPS, IMAP, IMAPS, LDAP, LDAPS, POP3, POP3S, RTMP, RTMPS, RTSP, SCP, SFTP, SMB, SBMS, SMTP, SMTPS, TELNET 和TFTP



**HTTP  GET 请求 **



```shell
curl https://curl.haxx.se
```



**HTTP POST 请求**



```shell
curl --data "birthyear=1905&press=%20OK%20"  http://www.example.com/when.cgi
```



**HTTP POST  Content-Type: application/json" **请求

```shell
curl -H "Content-Type: application/json" --data "{"key":value}"  http://www.example.com/when.cgi
```





**技巧**

1. 在后面加`| json_pp`,输出会以JSON格式输出

```shell
curl https://curl.haxx.se | json_pp
```





**参考文档**

- [官方文档](https://curl.haxx.se/)

- [Http相关操作文档](Using curl to automate HTTP jobs)