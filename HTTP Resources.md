# URL 组成



> URL Scheme**://**Host**:**Port**/**URL Path**#**Fragment**?**q**=**food**&**color**=**green



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