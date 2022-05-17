# HTTP Message Type

单个 HTTP 事务中包含一个 request 和一个 response，他们总是成对出现的



# 手动发送一个 HTTP request



当在浏览器输入 URL 时，实际上发生了什么？

<img src="img\a_manual_request_2.png" style="zoom: 33%;" />



<img src="img\a_manual_request_0.png" style="zoom:33%;" />



任何可以通过网络发送数据的应用程序都可以发出 HTTP request

![](img\a_manual_request.png)



可以看到，它先通过 DNS 拿到目标网站的 IP，并连接，这时可以发送 request 请求，指定哪些内容？HTTP Method Get，请求资源路径和名称，协议，Host 地址

得到 response，显示被永久移动了，告诉了 location，如果你是浏览器的话，就要解析这个响应



![](img\a_manual_request_1.png)



再次请求时，输入上述的 Host，得到了需要的资源

