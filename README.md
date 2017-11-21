#苹果 
ipv6审核被拒解决方案


1.检查http请求是否使用了NSURLConnection，苹果iOS9.0之后，为支持ipv6，在NSURLSession中支持ipv6访问，放弃NSURLConnection；


使用AFNetWork的，需要升级AFNetWork到3.0以上；


2.代码中不要使用ip作为请求的NSURL；使用域名作为请求的NSURL；


#如果做到以上两点；app端的问题就已经解决了；剩下的就是后端域名的配置；





