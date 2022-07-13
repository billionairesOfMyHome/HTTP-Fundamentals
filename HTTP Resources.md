# URL 组成



> URL Scheme**://**Host**:**Port**/**URL Path**?**q**=**food**&**color**=**green**#**Fragment



注意 #Fragment 只能放最后，也就是查询参数的后面，否则放查询参数前面，查询参数会被认为是 Fragment 的一部分，就被服务器忽略掉



## URL Scheme

URL Scheme 有 HTTP, HTTPS, FTP



## Host

Host 一般是网站的名字，而不是 IP 地址，便于记忆，更友好



## Port

Port 在 HTTP 协议下默认是 80，HTTPS 协议下默认是 443



## URL Path 

URL Path 有时会指向主机中的真实资源，比如图标，但像动态的资源比如 ASP，HTML不会被直接指向



## Fragment 

Fragment 不由服务器处理，仅在客户端使用



## Query 

Query 以键值对出现，& 分隔，API 可以之前从 URL 拿到查询参数



## URL 是否区分大小写？

https://stackoverflow.com/questions/7996919/should-url-be-case-sensitive

原则：可能有 URL 的一部分，大小写无关紧要，但识别这些可能并不容易。用户应始终认为 URL 区分大小写。

理论上：

取决于服务器托管的操作系统。托管在 Windows 上的站点往往不区分大小写，因为底层文件系统不区分大小写。托管在 Unix 类型系统上的站点往往区分大小写，因为它们的底层文件系统通常区分大小写。URL 的主机名部分始终不区分大小写，路径的其余部分会有所不同。

# URL 编码



## 安全字符



容易引起歧义的不安全字符不应该出现在 URL 中，安全的字符包括：

> 大小写字母，数字，$-_.+*'(),



## 百分比编码（URL 编码）



以下是一些必须进行编码的常见字符：

| 不安全的字符 | 编码值 |
| :----------- | :----- |
| 空格         | `%20`  |
| "            | `%22`  |
| <            | `%3C`  |
| >            | `%3E`  |
| #            | `%23`  |
| %            | `%25`  |
| \|           | `%7C`  |



# Content MIME Types



浏览器首先通过 MIME types 确定接受的 content 类型，最后才是文件扩展名



## 常见 MIME 类型



| 扩展名         | 文档类型                                                     | MIME 类型                       |
| :------------- | :----------------------------------------------------------- | :------------------------------ |
| `.json`        | JSON format                                                  | `application/json`              |
| 纯文本         | 没有语法，通常会加 ;charset=utf-8                            | `text/plain;charset=utf-8`      |
| `.css`         | Cascading Style Sheets (CSS)                                 | `text/css`                      |
| `.csv`         | Comma-separated values (CSV)                                 | `text/csv`                      |
| `.htm.html`    | HyperText Markup Language (HTML)                             | `text/html`                     |
| `.js`          | JavaScript                                                   | `text/javascript`               |
| `.jpeg` `.jpg` | JPEG images                                                  | `image/jpeg`                    |
| `.gif`         | Graphics Interchange Format (GIF)                            | `image/gif`                     |
| `.mp3`         | MP3 audio                                                    | `audio/mpeg`                    |
| `.png`         | Portable Network Graphics                                    | `image/png`                     |
| `.pdf`         | Adobe [Portable Document Format](https://acrobat.adobe.com/us/en/why-adobe/about-adobe-pdf.html) (PDF) | `application/pdf`               |
| `.ppt`         | Microsoft PowerPoint                                         | `application/vnd.ms-powerpoint` |