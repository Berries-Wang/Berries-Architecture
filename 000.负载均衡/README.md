# 负载均衡
> 先阅读:[LVS 与 NGINX：探究两种主流负载均衡](./999.REF-DOCS/LVS%20与%20NGINX：探究两种主流负载均衡.pdf) & [10.Server Load Balancer (SLB)](../999.REF-DOCS/Alibaba%20Cloud%20Apsara%20Stack%20Enterprise%201911,%20Internal_%20V3.10.0%20Technical%20Wtepaper%2020210806.pdf)# ‘10.Server Load Balancer (SLB)’ 章节 & [2.1 自建数据中心的负载均衡](../999.REF-DOCS/bestpractice-cloudpond-pdf.pdf)#'2.1 自建数据中心的负载均衡'章节

需要了解：
1. LVS 、 Keepalived是什么
2. Nginx 和 LVS+Keepalived 负载均衡区别是什么? 实现原理有什么区别
3. 分别能承受多大的并发量
   ```txt
      NGINX: 10w并发
      LVS+Keepalived: 10w+ , 不够就加机器
   ```
4. 两种方式的优缺点
   - LVS+Keepalived 存在网络攻击隐患，但ali SLB已处理,参考: [LVS 与 NGINX：探究两种主流负载均衡](./999.REF-DOCS/LVS%20与%20NGINX：探究两种主流负载均衡.pdf) & [10.Server Load Balancer (SLB)](../999.REF-DOCS/Alibaba%20Cloud%20Apsara%20Stack%20Enterprise%201911,%20Internal_%20V3.10.0%20Technical%20Wtepaper%2020210806.pdf)# ‘10.Server Load Balancer (SLB)’ 章节
5. 为你的场景选择合适的
   ```txt
      1. NGINX 10w以内并发
      2. 10w+并发: LVS + Nginx
   ```

---

## 参考资料
1. [keepalived](https://www.keepalived.org/)
   - Github:[https://github.com/acassen/keepalived](https://github.com/acassen/keepalived)
2. [alibaba LVS](https://github.com/alibaba/LVS)
3. [引用资料: 999.REF-DOCS](./999.REF-DOCS/)
