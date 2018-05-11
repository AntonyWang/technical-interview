# Technical-interview
Web面试题

## Frontend
web前端面试题

### HTML
>#### html有哪些常用标签（tag）?
- 基本框架元素有：html head title body  
- 行内元素有：a b span img input select strong  
- 块级元素有：div ul ol li dl dt dd h1 h2 h3 h4…p  
- 常见的空元素：br img input link meta  

>#### html5文件与html4文件的区别？
- !DOCTYPE HTML  

>#### 浏览器有哪些的本地存贮技术
- Cookies  
- LocalStorage  
- SessionStorage  
- WebDB  
- IndexedDB  

>#### 常见的浏览器内核有哪些？
- Webkit内核：Safari,Chrome等。  
- Trident内核：IE,MaxThon,TT,The World,360,搜狗浏览器等。  
- Gecko内核：Netscape6及以上版本，FF,MozillaSuite/SeaMonkey等  
- Presto内核：Opera7及以上。

### CSS 
>#### 介绍一下标准的CSS的盒子模型？
- 盒模型：内容(content)、填充(padding)、边界(margin)、 边框(border)；  
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
- !important > id > class > tag  
important 比 内联优先级高,但内联比 id 要高


### Javascript
>#### js的闭包拥有哪些特性？
- 闭包是指有权访问另一个函数作用域中的变量的函数，创建闭包的最常见的方式就是在一个函数内创建另一个函数，通过另一个函数访问这个函数的局部变量。使用闭包有一个优点，也是它的缺点，就是可以把局部变量驻留在内存中，可以避免使用全局变量。  
1.函数嵌套函数  
2.函数内部可以引用外部的参数和变量  
3.参数和变量不会被垃圾回收机制回收  

>#### eval是做什么的？
由JSON字符串转换为JSON对象的时候可以用eval，var obj =eval('('+ str +')')  

>#### Ajax是什么? 如何创建一个Ajax？
- ajax的全称：Asynchronous Javascript And XML。异步传输+js+xml  
 所谓异步，在这里简单地解释就是：向服务器发送请求的时候，我们不必等待结果，而是可以同时做其他的事情，等到有了结果它自己会根据设定进行后续操作，与此同时，页面是不会发生整页刷新的，提高了用户体验。  
 (1)创建XMLHttpRequest对象,也就是创建一个异步调用对象  
 (2)创建一个新的HTTP请求,并指定该HTTP请求的方法、URL及验证信息  
 (3)设置响应HTTP请求状态变化的函数  
 (4)发送HTTP请求  
 (5)获取异步调用返回的数据  
 (6)使用JavaScript和DOM实现局部刷新  

### 框架
>#### 前端框架有哪些？
- AngularJS  
- Vue.js  
- React.native  

### 其他问题
>#### http状态码有那些？分别代表是什么意思？
- 100  Continue 一般在发送post请求时，已发送了http header之后服务端将返回此信息，表示确认，之后发送具体参数信息  
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
- `封装`：封装的意义，在于明确标识出允许外部使用的所有成员函数和数据项，或者叫接口。
- `继承`：
    继承基类的方法，并做出自己的扩展；
    声明某个子类兼容于某基类（或者说，接口上完全兼容于基类），外部调用者可无需关注其差别（内部机制会自动把请求派发`dispatch`到合适的逻辑）。
- `多态`：基于对象所属类的不同，外部对同一个方法的调用，实际执行的逻辑不同。

>#### final, finally, finalize 的区别
- final 是一个修饰符，可以修饰变量、方法和类。如果 final 修饰变量，意味着该变量的值在初始化后不能被改变。
- finally 是一个关键字，与 try 和 catch 一起用于异常的处理。finally 块一定会被执行，无论在 try 块中是否有发生异常。
- finalize 方法是在对象被回收之前调用的方法，给对象自己最后一个复活的机会，但是什么时候调用 finalize 没有保证。

>#### int 和 Integer 有什么区别
- Java是一个近乎纯洁的面向对象编程语言，但是为了编程的方便还是引入了基本数据类型，但是为了能够将这些基本数据类型当成对象操作，Java为每一个基本数据类型都引入了对应的包装类型（wrapper class），int的包装类就是Integer。Java 为每个原始类型提供了包装类型：  
	- 原始类型: boolean，char，byte，short，int，long，float，double  
	- 包装类型：Boolean，Character，Byte，Short，Integer，Long，Float，Double  
Integer 对象会占用更多的内存。Integer 是一个对象，需要存储对象的元数据。但是 int 是一个原始类型的数据，所以占用的空间更少。

>#### 重载和重写的区别
- 方法的重载和重写都是实现多态的方式，区别在于前者实现的是编译时的多态性，而后者实现的是运行时的多态性。重载发生在一个类中，同名的方法如果有不同的参数列表（参数类型不同、参数个数不同或者二者都不同）则视为重载；重写发生在子类与父类之间，重写要求子类被重写方法与父类被重写方法有相同的返回类型，比父类被重写方法更好访问，不能比父类被重写方法声明更多的异常（里氏代换原则）。重载对返回类型没有特殊的要求。

>#### HTTP 请求的 GET 与 POST 方式的区别
- get参数通过url传递，post放在request body中。
- get请求在url中传递的参数是有长度限制的，而post没有。
- get比post更不安全，因为参数直接暴露在url中，所以不能用来传递敏感信息。

>#### session 与 cookie 区别
- 存在的位置
cookie 存在于客户端，临时文件夹中  
session：存在于服务器的内存中，一个session域对象为一个用户浏览器服务  
- 访问范围
session为一个用户浏览器独享  
cookie为多个用户浏览器共享  

>#### MVC 设计思想

>#### "a==b"和"a.equals(b)"有什么区别？
- 如果 a 和 b 都是对象，则 a==b 是比较两个对象的引用，只有当 a 和 b 指向的是堆中的同一个对象才会返回 true，而 a.equals(b) 是进行逻辑比较，所以通常需要重写该方法来提供逻辑一致性的比较。例如，String 类重写 equals() 方法，所以可以用于两个不同对象，但是包含的字母相同的比较。默认下，对象用==比较时，比较的是内存地址，如果需要比较对象内容，需要重写equal方法

### Java 进阶
>#### 手写单例模式代码；

>#### 获取已知数组中升序最大数组；

>#### 用string的api完成字符串转化为数字(只能是string的api)；

>#### 多线程所有知识点；
- 线程是进程的子集，一个进程可以有很多线程，每条线程并行执行不同的任务。不同的进程使用不同的内存空间，而所有的线程共享一片相同的内存空间。别把它和栈内存搞混，每个线程都拥有单独的栈内存用来存储本地数据。

>#### 什么是线程池？ 为什么要使用它？
- 创建线程要花费昂贵的资源和时间，如果任务来了才创建线程那么响应时间会变长，而且一个进程能创建的线程数有限。为了避免这些问题，在程序启动的时候就创建若干线程来响应处理，它们被称为线程池，里面的线程叫工作线程。Java API 提供了 Executor 框架让你可以创建不同的线程池。比如单线程池，每次处理一个任务；数目固定的线程池或者是缓存线程池（一个适合很多生存期短的任务的程序的可扩展线程池）。

>#### Java中堆和栈有什么不同？
- 因为栈是一块和线程紧密相关的内存区域。每个线程都有自己的栈内存，用于存储本地变量，方法参数和栈调用，一个线程中存储的变量对其它线程是不可见的。而堆是所有线程共享的一片公用内存区域。对象都在堆里创建，为了提升效率线程会从堆中弄一个缓存到自己的栈，如果多个线程使用该变量就可能引发问题，这时 volatile 变量就可以发挥作用了，它要求线程从主存中读取变量的值。

>#### 接口和抽象类(包含java8新特性)；
- Java 中，抽象类和接口有很多不同之处，但是最重要的一个是 Java 中限制一个类只能继承一个类，但是可以实现多个接口。抽象类可以很好的定义一个家族类的默认行为，而接口能更好的定义类型，有助于后面实现多态机制。
>#### 枚举类；

>#### spring特性以及多种注解之间的区别；

>#### hashmap的put和get底层代码实现；

>#### 两个文件，如何打印出重复的部分(只能Java实现，不可使用第三方工具)；

### Database
>#### 写模糊查询SQL；
	select * from table where name like "% %";
>#### 写分组查询SQL；
	select department,max(age) from table orderby department;
>#### 数据库锁的理解及利弊；

>#### JDBC 流程

### Linux
>#### Linux命令(需要手写出完整的命令，不仅限单个单词，如tail，net stat，chmod等)。

