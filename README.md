# Technical-interview
Web面试题

## Frontend
web前端面试题

### HTML
>#### html有哪些常用标签（tag）?
基本框架元素有：html head title body  
行内元素有：a b span img input select strong  
块级元素有：div ul ol li dl dt dd h1 h2 h3 h4…p  
常见的空元素：br img input link meta  
>#### html5文件与html4文件的区别？
!DOCTYPE HTML  
>#### 浏览器有哪些的本地存贮技术
Cookies  
LocalStorage  
SessionStorage  
WebDB  
IndexedDB  
>#### 常见的浏览器内核有哪些？
Webkit内核：Safari,Chrome等。  
Trident内核：IE,MaxThon,TT,The World,360,搜狗浏览器等。  
Gecko内核：Netscape6及以上版本，FF,MozillaSuite/SeaMonkey等  
Presto内核：Opera7及以上。  


### CSS 
>#### 介绍一下标准的CSS的盒子模型？
盒模型：内容(content)、填充(padding)、边界(margin)、 边框(border)；  

>#### CSS选择符有哪些？
```
1.id选择器（ # myid）
2.类选择器（.myclassname）
3.标签选择器（div, h1, p）
4.相邻选择器（h1 + p）
5.子选择器（ul > li）
6.后代选择器（li a）
7.通配符选择器（ * ）
8.属性选择器（a[rel = "external"]）
9.伪类选择器（a: hover, li:nth-child）
```
>#### CSS选择符优先顺序？
!important > id > class > tag  
important 比 内联优先级高,但内联比 id 要高


### Javascript
>#### js的闭包拥有哪些特性？
闭包是指有权访问另一个函数作用域中的变量的函数，创建闭包的最常见的方式就是在一个函数内创建另一个函数，通过另一个函数访问这个函数的局部变量。使用闭包有一个优点，也是它的缺点，就是可以把局部变量驻留在内存中，可以避免使用全局变量。  
1.函数嵌套函数  
2.函数内部可以引用外部的参数和变量  
3.参数和变量不会被垃圾回收机制回收  

>#### eval是做什么的？
由JSON字符串转换为JSON对象的时候可以用eval，var obj =eval('('+ str +')')  

>#### Ajax是什么? 如何创建一个Ajax？
 ajax的全称：Asynchronous Javascript And XML。异步传输+js+xml  
 所谓异步，在这里简单地解释就是：向服务器发送请求的时候，我们不必等待结果，而是可以同时做其他的事情，等到有了结果它自己会根据设定进行后续操作，与此同时，页面是不会发生整页刷新的，提高了用户体验。  
 (1)创建XMLHttpRequest对象,也就是创建一个异步调用对象  
 (2)创建一个新的HTTP请求,并指定该HTTP请求的方法、URL及验证信息  
 (3)设置响应HTTP请求状态变化的函数  
 (4)发送HTTP请求  
 (5)获取异步调用返回的数据  
 (6)使用JavaScript和DOM实现局部刷新  


### 框架
>#### 前端框架有哪些？
AngularJS  
Vue.js  
React.native  

### 其他问题
>#### http状态码有那些？分别代表是什么意思？
100  Continue 一般在发送post请求时，已发送了http header之后服务端将返回此信息，表示确认，之后发送具体参数信息  
200  OK 正常返回信息  
201  Created  	请求成功并且服务器创建了新的资源  
202  Accepted 	服务器已接受请求，但尚未处理  
301  Moved Permanently  请求的网页已永久移动到新位置  
302 Found 临时性重定向  
303 See Other  	临时性重定向，且总是使用 GET 请求新的 URI  
304  Not Modified 自从上次请求后，请求的网页未修改过  
400 Bad Request  服务器无法理解请求的格式，客户端不应当尝试再次使用相同的内容发起请求  
401 Unauthorized 请求未授权  
403 Forbidden  	禁止访问  
404 Not Found  	找不到如何与 URI 相匹配的资源  
500 Internal Server Error  最常见的服务器端错误  
503 Service Unavailable 服务器端暂时无法处理请求（可能是过载或维护）  

## Backend
web后端/服务器端面试题

### Java基本功
>#### 面向对象的特征

>#### final, finally, finalize 的区别

>#### int 和 Integer 有什么区别

>#### 重载和重写的区别

>#### 说说反射的用途及实现

>#### HTTP 请求的 GET 与 POST 方式的区别

>#### session 与 cookie 区别

>#### MVC 设计思想

>#### equals 与 == 的区别

### Java 进阶
>#### 手写单例模式代码；

>#### 获取已知数组中升序最大数组；

>#### 用string的api完成字符串转化为数字(只能是string的api)；

>#### 多线程所有知识点；

>#### 接口和抽象类(包含java8新特性)；

>#### 枚举类；

>#### spring特性以及多种注解之间的区别；

>####  hash map的put和get底层代码实现；

>#### 两个文件，如何打印出重复的部分(只能Java实现，不可使用第三方工具)；

### DB
>#### 写分组查询SQL；

>#### 数据库锁的理解及利弊；

>#### JDBC 流程

### Linux
>#### Linux命令(需要手写出完整的命令，不仅限单个单词，如tail，net stat，chmod等)。














