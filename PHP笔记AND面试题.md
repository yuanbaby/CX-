#PHP笔记 AND 面试题#
> PHP，一个嵌套的缩写名称，是英文超级文本预处理语言（**PHP:Hypertext Preprocessor**）的缩写。PHP 是一种 HTML 内嵌式的语言，PHP与微软的ASP颇有几分相似，都是一种在服务器端执行的嵌入HTML文档的脚本语言.
> 
>PHP结构：<?php  ---   ?>

>    echo  页面输出语句
    
>### get与post的区别  （重中之重面试题）

>**get**:在基于浏览器的基础上，地址栏显示name,浏览器当中设置只能传1KB字符左右，大概256个字符。

> **post**:在基于浏览器的基础上，地址栏不显示name,浏览器当中设置字符是任意长度的。

---

>### 双引号和单引号的区别   （重中之重面试题）

>1.双引号能解析变量，但是单引号不能解析变量.

>2.在双引号里插入变量，变量如果有英文或中文字符，它会把这个字符和变量拼接起来，视为一个整变量。**一定要在变量后面接上特殊字符，例如空格等分开。**

>3.如果在双引号里 插入变量，后面不想有空格，可以拿大括号将变量包起来。**（推荐写法）**

>4.双引号解析转义字符，单引号不能解析转义字符，但是，单引能解析 \ 和 /.

>5.单引号效率高于双引号，尽可能使用单引号。**（推荐使用单引号）**

>6.双引号和单引号可以互相使用！双引号当中插入引号，单引号中插入变量，这个变量会被解析。

>7.神奇的字符串拼接胶水——（.）点，用来拼接字符串。

>8.我们将定界符声明字符串视为双引号一样的功能来看待。

---

>### window.onload和$(function())的区别   （重中之重面试题）

>1.window.onload有且只有一次，定义多次之后，后者覆盖前者。$(function())可调用多次。

>2.window.onload是指页面中的所有资源加载完毕之后执行，比较慢。$(function())是当页面中的DOM元素加载完毕之后执行。

>3.window.onload没有简写。$(function())的全写为：$(document).ready(function(){}).

---

>### JavaScript对象和jquery对象如何进行相互的抓换？   （重中之重面试题）
---JavaScript
>var account_js = document.getElementById("account");

>转换成jquery对象，那么直接在其周围$(account_js);
>

>jquery对象转换成js对象

>var account_js =$("#account");

>alert($(account_js)[0]);

>alert($(account_js).get(0));