# Web 开发
### 概念
&emsp;&emsp;**Web 开发:** 网站只是 Web 开发技术的一种应用，诸如微信公众号平台、小程序、iOS和Andriod都需要 Web 开发技术支持
&emsp;&emsp;**Web 框架:** 进行 Web 应用开发的一种软件架构，已提供比较完整的业务和功能服务，开发者只需在此基础上进行轻量级开发即可
&emsp;&emsp;**全栈开发技术:** 前端开发技术、后端开发技术、数据库技术、安全开发技术等主流开发技术集合
&emsp;&emsp;**前端开发基础:** HTML、CSS、Javascript ( ES5 )、JQuery
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 主流前端框架: Vue、React、Augular、Bootstrap
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 其他前端技术:HTML5、CSS3、 ES6、Typescript
&emsp;&emsp;**后端开发基础:** Python、Go、Java、PHP
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 主流后端框架: Python ( Flask、Django、Tornado )、Go ( Beego、Gin )等
&emsp;&emsp;**数据库开发基础:** MySQL、MSSQL、PostgreSQL、Redis、MongoDB
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; 中间件: ORM
&emsp;&emsp;**安全开发基础:** 服务器安全、数据库安全、代码安全开发
&emsp;&emsp;**网站设计模式:** MVC、MVVM、MVP
&emsp;&emsp;**初识MVC模式:** 核心在于分层，**V** 指 View 前端视图，**C **指 Controller 用于调度，**M** 指 Model 模型，例如 DB 表作为模型
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; MVC 相互独立，工作原理，用户通过前端视图发起请求，调度中心调度对应的模型，模型是根据DB的表生成的模型返回调度中心即可
![](/assets/22C6E500FDE45F2A8A33D98E3B443858.png)
### HTTP 与 HTTPS
&emsp;&emsp;**HTTP:** 基于TCP/IP的一种超文本传输协议，所有 WWW 文件都必须遵循该协议
&emsp;&emsp;**HTTPS:** 在 HTTP 基础上加入了 SSL 协议，通过通信加密和身份验证保证数据传输安全
&emsp;&emsp;**常见请求方法:** 
### URL 详解
&emsp;&emsp;**URL:**  统一资源定位符
```html
  scheme://host:port/path/?query-string=xxx#achor

```
* **scheme:** 代表访问的协议，一般为 http 或者 https 以及 FTP 等
* **host:** 主机名，域名，比如 www.baidu.com
* **port:** 端口号，浏览器默认使用80端口，所以一般不用写也能解析
* **query-string:** 查询字符串，比如: www.baidu.con/s?wd=python，后面 wd=python 就是查询字符串
* **anchor:** 锚点，前端用来做页面定位的，例如: 百度百科
### 重定向
* **永久性重定向:** http的状态是 301，多用于旧网址被废弃转到新网址
* **暂时性重定向:** http的状态是 302，多用于访问一个有权限或者要登录才能看得页面时，重定向到授权或者注册页面









 













