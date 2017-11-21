#苹果 
ipv6审核被拒解决方案


1.检查http请求是否使用了NSURLConnection，苹果iOS9.0之后，为支持ipv6，在NSURLSession中支持ipv6访问，放弃NSURLConnection；


使用AFNetWork的，需要升级AFNetWork到3.0以上；


2.代码中不要使用ip作为请求的NSURL；使用域名作为请求的NSURL；


#如果做到以上两点；app端的问题就已经解决了；剩下的就是后端域名的配置；


后端配置
1.配置ipv6，这个目前还没有找到办法；国内配置ip
2.不配置ipv6；其实就是配置好一个域名，苹果审核的时候，是ipv6-only环境，所以，首先是向dns服务器，请求，如果能获取到ipv6；就直接访问；不能，就通过nat64网络，转换成ipv4的环境；


