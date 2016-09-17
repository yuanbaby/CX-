# **web面试试题** #
**1**. 正整数A的“DA（为1位整数）部分”定义为由A中所有DA组成的新整数PA。例如：给定A = 3862767，DA = 6，则A的“6部分”PA是66，因为A中有2个6。

现给定A、DA、B、DB，请编写程序计算PA + PB。

输入格式：

输入在一行中依次给出A、DA、B、DB，中间以空格分隔，其中0 < A, B < 1010。

输出格式：

在一行中输出PA + PB的值。

输入样例1：
3862767 6 13530293 3
输出样例1：
399
输入样例2：
3862767 1 13530293 8<br>
	答：
		源代码：<br>
		#include<iostream>  
		#include<string>  
		using namespace std;  
		int main()  
		{  
		    string str1,str2;  
		    char ch1,ch2;  
		    int sum1=0,sum2=0,sum3=0;  
		    int count1 = 1,count2 =1;  
		    cin>>str1>>ch1>>str2>>ch2;  
		    for(int i=0;i<str1.length();i++)  
		    {     
		        if(str1[i]==ch1)  
		        {  
		            sum1+= count1*(ch1-48);  
		            count1*=10;  
		        }  
		    }  
		    for(int i=0;i<str2.length();i++)  
		    {     
		        if(str2[i]==ch2)  
		        {  
		            sum2+= count2*(ch2-48);  
		            count2*=10;  
		        }  
		    }  
		    cout<<sum1+sum2<<endl;  
		    system("pause");  
		    return 0;  
		}  
**2**.在jquery中想要找到所有元素的同辈元素，下面哪一个是可以实现的？<br>
	答：sibling([expr])相邻元素。<br>
**3**.常见的http错误描述原因有哪些？<br>
	答：	A、404-Not found（没有找到）<br>
		B、302-暂时重定向  //  301 - 永久重定向<br>
		C、500-内部服务器错误<br>
		D、403- IP address rejected<br>
**4**. 下面哪个不属于Promise的状态？（D） <br>
		A、Unfulfilled
		B、Rejected
		C、Resolved
		D、Pause  
	解析：promise模式在任何时刻都处于以下三种状态之一：未完成（unfulfilled）、已完成（resolved）和拒绝（rejected）。<br> 
**5**.  我们常说的mvc框架是指的什么？ <br>
	答：MVC全名是**Model View Controller**，是模型(model)-视图(view)-控制器(controller)的缩写，一种软件设计典范，用一种业务逻辑、数据、界面显示分离的方法组织代码，将业务逻辑聚集到一个部件里面，在改进和个性化定制界面及用户交互的同时，不需要重新编写业务逻辑。MVC被独特的发展起来用于映射传统的输入、处理和输出功能在一个逻辑的图形化用户界面的结构中。<br>   
**6**.  使用css的flexbox布局，不能实现一下哪一个效果： （D）  <br>      
			A、三列布局，随容器宽度等宽弹性伸缩
			B、多列布局，每列的高度按内容最高的一列等高
			C、三列布局，左列宽度像素数确定，中、右列随容器宽度等宽弹性伸缩
			D、多个宽高不等的元素，实现无缝瀑布流布局   
**7**.  以下哪一个不是块状元素？ （A）<br> 
		A、span
		B、h1
		C、p
		D、div   
**8**.  现有如下html结构<br>
	<ul>
		<li>click me</li>
		<li>click me</li>
		<li>click me</li>
		<li>click me</li>
	</ul>
现运行如下代码：<br>
	var elements = document.getElementsByTagName("li");
	var lengths = elements.length;
	for(var i=0; i<lengths; i++){
		elements[i].onclick = function(){
			alert(i);
		}
	}
依次点击4个li标签，正确的运行结果是？<br>
	答：依次弹出 4 4 4 4.

##  Web前端开发面试题集及答案 ##
***一、填空题***<br>
	1、目前常用的WEB标准静态页面语言是__ **html__**____。<br>
	2、改变元素的外边距用_**margin**___，改变元素的内填充用__**padding**_。<br> 
	3、在Table中，TR是__**行**__，TD是__**列**__。<br>
	4、如果给一行两列的表格（table）定义高度样式，在_**css样式**_标签中定义最合理，最能减少代码的臃肿<br>
	5、对ul li的样式设成无，应该是用什么属性_**list-styl-type：none；**_。<br>
	7、Color:#666666;可缩写为_**color：#666**__。<br>
	8、合理的页面布局中常听过结构与表现分离，那么结构是_**div**__，表现是_**css**__。<br>

**二、选择题**
1、在下面的XHTML中，哪个可以正确地标记折行？（A）<br>
	A：<br /> B：<break/> C：<br>

2、下列哪些是格式良好的XHTML？（B）<br>
	A：<p>A <b><i>short</b></i> paragraph</p>
	B：<p>A <b><i>short</i></b> paragraph</p>
	C：<p>A <b><i>short</i></b> paragraph

3、在以下的HTML中，哪个是正确引用外部样式表的方法？（B）<br>
	A：<style src="mystyle.css">
	B：<link rel="stylesheet" type="text/css" href="mystyle.css">
	C：<stylesheet>mystyle.css</stylesheet>

4、在HTML文档中，引用外部样式表的正确位置是？（D）<br>
	A：文档的末尾 B：文档的顶部
	C：<body>部分D：<head>部分
**
三、问答题（40分）**
1、请写出超链接的顺序或者你在初始样式中的链接方法。（要求默认无下线，鼠标经过有下划线）<br>
	L-V-H-A
	a:link { line-style：none；}
	a:hover { line-style：underlin；}
	
	或者
	
	a:link{text-decoration:none;}
	a:hover{text-decoration:underline;}
2、当float和margin同时使用时，IE6的双倍边距BUG如何解决？<br>

	display：inline；或者margin-right:-3px;
3、为什么无法定义1px左右高度的容器？<br>

	好像是有个默认高度，大约是10px这样，参考答案

4、Firefox中标签的居中问题的解决方法？<br>

		*{margin：0px auto；}	
5、请写出XHTML和CSS如何注释？（5分），<br>

	<div><!-- 注释内容-->...</div>
	   .class{/* 注释内容*/...}
6、请以缩写方法写出1px直线（实线）灰色（任意灰色代码值），上面无边框的矩形边框样式。（7分）<br>

	.***{border：1px solid #000；border-top：0px；}或者border:1px solid  #ccc;border-top:none;
	
7.为什么无法定义1px左右高度的容器？<br>
	IE6有默认行高

**百度校园招聘web前端开发面试题（含参考答案）**
 1、JS主要数据类型？（5分）
	答：主要的类型有 number、string、object 以及 Boolean 类型,其他两种类型为 null 和 undefined。

2、img的alt和title的异同？（10分）
	答：title属性为设置该属性的元素提供建议性的信息。比如为链接添加描述性文字。
	为不能显示图像、窗体或applets的用户代理（UA），alt属性用来指定替换文字。使用alt属性是为了给那些不能看到你文档中图像的浏览者提供文字说明。

3、CSS的JS调用？如font-family, -moz-border-radius 。（10分）
	答：fontFamily、MozBorderRadius

4、CSS布局：两列，左边宽度自适应，右边宽度固定200px。 （15分）

    #box1{width:100%;height:600px;position:relative;}
    #left1{margin-right:200px;border:1px solid red;height:100%;}
    #right1{width:200px;height:100%;position:absolute;top:0px;right:0px;border:1px solid blue;}   
 
5、js对象的深度克隆？（20分）
    Object.prototype.deepClone=function(){
           function cloneObj(){}   
           cloneObj.prototype=this;
           var obj=new cloneObj();
     for(var o in obj){
               if(typeof(obj[o])=="object")obj[o]=obj[o].deepClone();
               }    return obj;
    }
 

6、动态打印时间，格式为yyyy-MM-dd hh:mm:ss? （15分）

    function printTime(){
        var timer1=new Date();
        var timer=timer1.toLocaleString();
        timer=timer.replace(/[年月]/g,"-");
        timer=timer.replace(/日/,"");
        time.innerHTML=timer;
    }setInterval("printTime()",1000);
 

7、Flash、Ajax各自的优缺点，在使用中如何取舍？（10分）

	1、Flash ajax对比
	Flash适合处理多媒体、矢量图形、访问机器；对CSS、处理文本上不足，不容易被搜索。
	Ajax对CSS、文本支持很好，支持搜索；多媒体、矢量图形、机器访问不足。
	共同点：与服务器的无刷新传递消息、用户离线和在线状态、操作DOM
