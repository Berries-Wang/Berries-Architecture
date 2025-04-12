# HAProxy
HAProxy is a free, very fast and reliable reverse-proxy offering high availability, load balancing, and proxying for TCP and HTTP-based applications. It is particularly suited for very high traffic web sites and powers a significant portion of the world's most visited ones. (HAProxy 是一种免费、非常快速且可靠的反向代理，为基于 TCP 和 HTTP 的应用程序提供高可用性 、 负载均衡和代理。它特别适用于流量非常高的网站，并为世界上访问量最大的网站提供很大一部分支持。)


## HAProxy优缺点
### HAProxy优点
+ HAProxy是支持虚拟主机的，可以工作在4、7层(支持多网段)
+ HAProxy的优点能够补充Nginx的一些缺点，比如支持Session的保持，Cookie的引导；同时支持通过获取指定的url来检测后端服务器的状态。
+ HAProxy跟LVS类似，本身就只是一款负载均衡软件；单纯从效率上来讲HAProxy会比Nginx有更出色的负载均衡速度，在并发处理上也是优于Nginx的。
+ HAProxy支持TCP协议的负载均衡转发，可以对MySQL读进行负载均衡，对后端的MySQL节点进行检测和负载均衡，大家可以用LVS+Keepalived对MySQL主从做负载均衡。

### HAPorxy缺点：
+ 不支持POP/SMTP协议
+ 不支持SPDY协议
+ 不支持HTTP cache功能。现在不少开源的lb项目，都或多或少具备HTTP cache功能。
+ 重载配置的功能需要重启进程，虽然也是soft restart，但没有Nginx的reaload更为平滑和友好。
+ 多进程模式支持不够好, [线程性能低于多进程版本](./000.REFS/000.NGINX%20and%20HAProxy_%20Testing%20User%20Experience%20in%20the%20Cloud%20–%20NGINX%20Community%20Blog.pdf) 


## 参考资料
1. [https://www.haproxy.com/blog/haproxy-forwards-over-2-million-http-requests-per-second-on-a-single-aws-arm-instance](https://www.haproxy.com/blog/haproxy-forwards-over-2-million-http-requests-per-second-on-a-single-aws-arm-instance)
2. [https://blog.nginx.org/blog/nginx-and-haproxy-testing-user-experience-in-the-cloud](https://blog.nginx.org/blog/nginx-and-haproxy-testing-user-experience-in-the-cloud)
