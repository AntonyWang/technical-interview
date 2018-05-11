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
### 面向对象的特征
面向对象三要素：封装、继承、多态  
- `封装`：封装的意义，在于明确标识出允许外部使用的所有成员函数和数据项，或者叫接口。
- `继承`：
    继承基类的方法，并做出自己的扩展；
    声明某个子类兼容于某基类（或者说，接口上完全兼容于基类），外部调用者可无需关注其差别（内部机制会自动把请求派发`dispatch`到合适的逻辑）。
- `多态`：基于对象所属类的不同，外部对同一个方法的调用，实际执行的逻辑不同。**很显然，多态实际上是依附于继承的第二种含义的**。
### final, finally, finalize 的区别
final 是一个修饰符，可以修饰变量、方法和类。如果 final 修饰变量，意味着该变量的值在初始化后不能被改变。  
finally 是一个关键字，与 try 和 catch 一起用于异常的处理。finally 块一定会被执行，无论在 try 块中是否有发生异常。  
finalize 方法是在对象被回收之前调用的方法，给对象自己最后一个复活的机会，但是什么时候调用 finalize 没有保证。  
### int 和 Integer 有什么区别
Java是一个近乎纯洁的面向对象编程语言，但是为了编程的方便还是引入了基本数据类型，但是为了能够将这些基本数据类型当成对象操作，Java为每一个基本数据类型都引入了对应的包装类型（wrapper class），int的包装类就是Integer，从Java 5开始引入了自动装箱/拆箱机制，使得二者可以相互转换。  
Java 为每个原始类型提供了包装类型：  
- 原始类型: boolean，char，byte，short，int，long，float，double  
- 包装类型：Boolean，Character，Byte，Short，Integer，Long，Float，Double  
Integer 对象会占用更多的内存。Integer 是一个对象，需要存储对象的元数据。但是 int 是一个原始类型的数据，所以占用的空间更少。
### 重载和重写的区别
方法的重载和重写都是实现多态的方式，区别在于前者实现的是编译时的多态性，而后者实现的是运行时的多态性。重载发生在一个类中，同名的方法如果有不同的参数列表（参数类型不同、参数个数不同或者二者都不同）则视为重载；重写发生在子类与父类之间，重写要求子类被重写方法与父类被重写方法有相同的返回类型，比父类被重写方法更好访问，不能比父类被重写方法声明更多的异常（里氏代换原则）。重载对返回类型没有特殊的要求。
### 说说反射的用途及实现
当程序运行时，允许改变程序结构或变量类型，这种语言称为动态语言。我们认为 Java 并不是动态语言，但是它却又一个非常突出的动态相关的机制，俗称：反射。  
Reflection 是Java 程序开发语言的特征之一，它允许运行中的 Java 程序获取自身的信息，并且可以操作类和对象的内部属性。  
通过反射，我们可以在运行时获得程序或程序集中每一个类型成员和成员变量的信息。  
程序中一般的对象类型都是在编译期就确定下来的，而Java 反射机制可以动态的创建对象并调用其属性，这样对象的类型在编译期是未知的。所以我们可以通过反射机制直接创建对象即使这个对象在编译期是未知的。  
反射的核心：是 JVM 在运行时 才动态加载的类或调用方法或属性，他不需要事先（写代码的时候或编译期）知道运行对象是谁。
### HTTP 请求的 GET 与 POST 方式的区别
对于GET方式的请求，浏览器会把http header和data一并发送出去，服务器响应200（返回数据）；  
而对于POST，浏览器先发送header，服务器响应100 continue，浏览器再发送data，服务器响应200 ok（返回数据）。  
- get参数通过url传递，post放在request body中。  
- get请求在url中传递的参数是有长度限制的，而post没有。  
- get比post更不安全，因为参数直接暴露在url中，所以不能用来传递敏感信息。
### session 与 cookie 区别
- 存在的位置  
cookie 存在于客户端，临时文件夹中  
session：存在于服务器的内存中，一个session域对象为一个用户浏览器服务  
- 安全性  
cookie是以明文的方式存放在客户端的，安全性低，可以通过一个加密算法进行加密后存放  
session存放于服务器的内存中，所以安全性好  
- 网络传输量  
cookie会传递消息给服务器
session本身存放于服务器，不会有传送流量
- 生命周期(以20分钟为例)  
cookie的生命周期是累计的，从创建时，就开始计时，20分钟后，cookie生命周期结束  
session的生命周期是间隔的，从创建时，开始计时如在20分钟，没有访问session，那么session生命周期被销毁  
但是，如果在20分钟内（如在第19分钟时）访问过session，那么，将重新计算session的生命周期  
关机会造成session生命周期的结束，但是对cookie没有影响  
- 访问范围  
session为一个用户浏览器独享  
cookie为多个用户浏览器共享  
### MVC 设计思想

### equals 与 == 的区别
==是运算符，用于比较两个变量是否相等，而equals是Object类的方法，用于比较两个对象是否相等。默认Object类的equals方法是比较两个对象的地址,此时和==的结果一样。  
换句话说:基本类型比较用==，比较的是他们的值。默认下，对象用==比较时，比较的是内存地址，如果需要比较对象内容，需要重写equal方法
### Java 进阶
>#### 手写单例模式代码；

>#### 获取已知数组中升序最大数组；

>#### 用string的api完成字符串转化为数字(只能是string的api)；

>#### 多线程所有知识点；

>#### 接口和抽象类(包含java8新特性)；
Java 中，抽象类和接口有很多不同之处，但是最重要的一个是 Java 中限制一个类只能继承一个类，但是可以实现多个接口。  
抽象类可以很好的定义一个家族类的默认行为，而接口能更好的定义类型，有助于后面实现多态机制。
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














