# Cookie



<img src="img\cookie.png" style="zoom:60%;" />



cookie 最大约为 4 KB



## 会话 cookie



会话 cookie（ session cookies），仅用于当个用户会话，当用户关闭浏览器时，它将被清除

此外， cookie 不是服务器的的会话对象或会话数据（session object）



<img src="img\cookie_1.png" style="zoom:67%;" />



<img src="img\cookie_2.png" style="zoom:80%;" />







## 持久性 cookie



<img src="img\cookie_3.png" style="zoom:80%;" />



# Authentication 身份认证



认证的协议有 basic authentication，digest authentication，windows authentication，form authentication, open ID, HTTPS 等，只有 basic authentication，digest authentication 是 HTTP 规范中的正式协议



## Basic Authentication



如果请求了被保护的资源，比如 WEB-INF 里面的资源，没有认证就会返回 401，basic authentication 就是在请求头中加一个 authentication，值是客户端用户和密码的 base64 编码值，因此很不安全，没有被广泛应用，使用它时会加上 HTTPS

<img src="img\authentication.png" style="zoom:60%;" />



<img src="img\authentication1.png" style="zoom:60%;" />



<img src="img\authentication2.png" style="zoom:60%;" />



<img src="img\authentication3.png" style="zoom:60%;" />



## Digest Authentication



![](C:\Learning\HTTP-Fundamentals\img\authentication5.png)



## Windows Authentication



windows authentication 类似于上面两个，它需要 windows 机器作为 Web 服务器

<img src="img\authentication6.png" style="zoom:60%;" />



<img src="img\authentication7.png" style="zoom:60%;" />



## Form Authentication



<img src="img\authentication8.png" style="zoom:600%;" />



尽管如此，表单身份验证依然受欢迎，因为它使你可以完全控制登录体验



<img src="img\authentication9.png" alt="authentication9" style="zoom:60%;" />



## Open ID



<img src="img\authentication10.png" style="zoom:60%;" />

 

##  Secure HTTP



HTPP message 的优势就是可读性，但一些消息不想让别人看到，比如密码、信用卡信息等，就可以用secure http ( https / ssl / tls ) 。HTTPS 在 message 开始传播之前对其加密。



### 原理



<img src="img\https.png" style="zoom:67%;" />



所有通过 HTTPS 的请求和响应都会被加密，包含 HTTP 头，消息正文M，URL 路径，URL 查询字符串，所有的 cookie，几乎除了 HOST name 的所有。



HTTPS 不对客户端进行身份验证，因此，程序需要实现表单身份验证或前面提到的其他身份验证协议



### 缺点



由于需要加密解密，Web 服务器有加密计算的负担，大型站点经常使用专用硬件，即 SSL 加速器，因此 HTTPS 在计算上很昂贵

<img src="img\HTTPS1.png" style="zoom:60%;" />



<img src="img\https2.png" style="zoom:60%;" />

