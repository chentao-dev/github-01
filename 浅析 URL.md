## URL

![img](https://raw.githubusercontent.com/chentao-dev/image-hosting/master/%E7%9F%B3%E5%A2%A8%E6%96%87%E6%A1%A3/url.7ec58rgm4i40.webp)



## DNS

```
用于映射域名和ip,  访问域名时会通过dns先去找ip, 找到了在返回结果, 进行访问

nslookup 域名        //查询域名绑定的所有ip
```



## IP

```
1.表示设备的地址、2.封装数据跟其他设备交流

分为内网ip(局域网), 外网ip(互联网)

ping 域名/ip        //查询域名/ip是否可用
```





## 域名

```
就是绑定ip的

域名类型       //com顶级域名、xxx.com二级域名(常用)、xxx.xxx.com三级域名

远程域名       //花钱买  

本地域名       //hosts文件添加 "ip  域名"

负载均衡       //一个域名绑多个ip,  一个网站用多个服务器分流,  防止压力过大

共享主机       //一个ip绑多个域名,  一个服务器运行多个网站,  太穷了服务器太贵

hosts文件     //win在C:\Windows\System32\drivers\etc\hosts、linux在/etc/hosts

```



