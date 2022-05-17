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



## required header for get requests

For get requests, you typically don't see a body. You just see the start line and then one or more headers. And I keep saying one or more, because, remember, **the host header is a required header**.



## 常见的请求头

<img src="img\request_headers.png" style="zoom:50%;" />



## 响应状态码

<img src="img\response_status_codes.png" style="zoom:40%;" />

<img src="img\response_status_code.png" style="zoom:50%;" />



# HTTP Methods



常用的就前面两个：

<img src="img\request_methods.png" style="zoom:35%;" />

## GET Method

GET 是安全的 method，它不会带来改变，只请求资源

它可能附带在 URL 上，URL Scheme://Host**:**Port**/**URL Path**?q=food&color=green**



## POST Method

POST 不是安全的 method
