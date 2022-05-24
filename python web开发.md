# 1、快速开发网站

# 2、浏览器能识别的标签



## 2.1编码（head)

<meta charset="UTF-8">



## 2.2 Title (head)

<head>
    <meta charset="UTF-8">
    <title>中国联通</title>
</head>

<img src="C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220426014735001.png" alt="image-20220426014735001" style="zoom:80%;" />

## 2.3 标题（body)

```html
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
<h4>四级标题</h4>
<h5>五级标题</h5>
<h6>六级标题</h6>
```



<img src="C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220426015556033.png" alt="image-20220426015556033" style="zoom:67%;" />

## 2.4 div和span（body)

```html
<div>内容</div>
<span>asdfa</span>
```

- div 一个人占一整行 【块级标签】


```html
<body>
    <div>挖掘机技术哪家强</div><div>山东蓝翔</div>
</body>
```

![image-20220426020424408](C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220426020424408.png)

- span,自己多大占多少【行内标签】


```html
<body>
    <span>挖掘机技术哪家强</span>
    <sapn>山东蓝翔</sapn>
</body>
```

![image-20220426020631619](C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220426020631619.png)

## 2.5 超链接 （body)

```html
跳转到其他人的网站
<a href="https://www.bilibili.com/">点击跳转</a>
```

```html
跳转到自己网站的其他地址
<a href="/get/news">查看更多</a>
```

<img src="C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220426222732262.png" alt="image-20220426222732262" style="zoom:50%;" />

## 2.6 图片(body)

```html
<img src="图片地址" />
```

```html
直接显示别人的图片地址（防盗链）
<img src="https://pic3.zhimg.com/80/v2-181af0100b884fe71dc2b593500c76a1_400x224.jpg?source=4e949a73" />
```

```html
显示自己图片
	-自己项目创建一个static目录，图片要放在static
	-页面上引入图片
<img src="/static/img.png" />
```

```html
设置图片高度、宽度设置
<body>
    <div>
        刻刻帝<a href="https://www.bilibili.com/">点击跳转</a>
        <img src="https://pic3.zhimg.com/80/v2-181af0100b884fe71dc2b593500c76a1_400x224.jpg?source=4e949a73" />
    </div>
    <sapn>
        时崎狂三<a href="/get/news">查看更多</a>
        <img style="height:500px" src="/static/img.png" />
    </sapn>

</body>
```

<img src="C:\Users\RUWU\Desktop\image-20220427002838507.png" alt="image-20220427002838507" style="zoom: 50%;" />



## 小结

- **学习的标签**

```html
<h1></h1>
<div></div>
<span></span>
<a></a>
<img />
```



- **划分**

```html
-块级标签（占一行）
<h1></h1>
<div></div>
-行内标签（有几行占几行）
<span></span>
<a></a>
<img />
```

- **嵌套**

  ```html
  <div>
      <span>XXX</span>
      <img />
      <a> </a>
  </div>
  ```



## 2.7 列表标签

- 无序列表

```html
<h1>运营商</h1>
<Ul>
    <li>中国移动</li>
    <li>中国联通</li>
    <li>中国电信</li>
</Ul>
```

<img src="C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220427221045777.png" alt="image-20220427221045777" style="zoom:67%;" />

- 有序列表

```html
<h1>运营商</h1>
<ol>
    <li>中国移动</li>
    <li>中国联通</li>
    <li>中国电信</li>
</ol>
```

<img src="C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220427221453727.png" alt="image-20220427221453727" style="zoom:67%;" />



## 2.8 表格

```html
<h1>法外狂徒</h1>
<table>
   	<thead>
    	<tr>	<th>ID</th>		<th>姓名</th>		<th>年龄</th>	</tr>
    </thead>
    <tbody>	
              <tr>    <td>1001</td>		<td>张三</td>		<td>18</td>	</tr>
              <tr>   <td>2002</td>		<td>李四</td>		<td>18</td>	</tr>
              <tr>  <td>3003</td>		<td>王五</td>		<td>18</td>	</tr>
	</tbody>
</table>
```



<img src="C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220427222435785.png" alt="image-20220427222435785" style="zoom:67%;" />

### 2.8.1 案例

```html
<body>
    <table>
       <thead>
         <tr>
        	<th>ID</th>
            <th>姓名</th>
            <th>头像</th>
            <th>邮箱</th>
        </tr>
        </thead>
        <tbody>
            <tr>
				<td>1001</td>
                <td>张三</td>
                <td><img style="height:50px" src="/static/img.png" /></td>
                <td>zhangsan.com</td>
            </tr>
        </tbody>
    </table>
    
</body>
```

![image-20220428204052409](C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220428204052409.png)

## 2.9 input系列（7个）

```html
<h1>输入</h1>
<input type="text" />
<input type="password" />
<input type="file" />
<input type="radio"name="n1" />男
<input type="radio"name="n1" />女

<input type="checkbox"/>篮球
<input type="checkbox"/>足球
<input type="checkbox"/>乒乓球

<input type="button" value="提交"> #普通的按钮
<input type="submit" value="提交"> #提交表单
```

<img src="C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220430012553592.png" alt="image-20220430012553592" style="zoom:67%;" />



## 2.10 下拉框

```html
<select>
    <option>北京</option>
    <option>上海</option>
    <option>深圳</option>
</select>
<select multiple>
    <option>北京</option>
    <option>上海</option>
    <option>深圳</option>
</select>
```

<img src="C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220430013054785.png" alt="image-20220430013054785" style="zoom: 80%;" />

## 2.11 多行文本

```html
<h1>多行文本</h1>
<textarea rows="5"></textarea>
```

<img src="C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220430013451555.png" alt="image-20220430013451555" style="zoom:80%;" />



## 案例：用户注册

```html
<body>
<h1>用户注册</h1>
<div>
  用户名：<input type="text" />
</div>
<div>
  密码：<input type="password" />
</div>
<div>
  性别 <input type="radio">男
      <input type="radio">女
</div>

<div>
  爱好：
  <input type="checkbox">篮球
  <input type="checkbox">足球
  <input type="checkbox">乒乓球
</div>

<div>
  <select>
  城市：
  <option>上海</option>
  <option>深圳</option>
  <option>广东</option>
    </select>
</div>

<div>
  擅长领域：
  <select multiple>
    <option>打游戏</option>
    <option>睡觉</option>
    <option>吃饭</option>
  </select>
</div>
<h1>备注</h1>
<textarea rows="5"></textarea>
<div>
  <input type="button" value="提交">
</div>
</body>
```

![image-20220430015409237](C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220430015409237.png)

## 知识点回顾和补充

1、网站请求的流程

<img src="C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220504223213952.png" alt="image-20220504223213952" style="zoom:50%;" />

2、一大堆标签<----------------------------------------------------------------------------------------->



- 3、网络请求

  - 在浏览器的URL中写入地址，点击回车，访问	

  ```html
  浏览器会发送数据过去，本质上发送的是字符串：
  “GET/explore http.······”
  
  浏览器会发送数据过去，本质上发送的是字符串：
  "POST/explore http.······"
  ```

  - 浏览器向后端发送请求时

    - GET请求【URL访问/表单提交】

      - 现象：GET请求、跳转、向后台传入数据会拼接在URL。

        ```html
        https://www.so.com/s?ie=utf-8&src=hao_360so_a1004_b_cube&shb=1&hsid=4e1aac42ae03c0ea&ssid=&q=URL
        ```

        注意：GET请求数据会在URL中体现。

    - POST请求【表单提交】

      - 现象：提交数据不在URL中体现，而是在请求体中。




## 案例：用户注册

- 新创建一个项目
- 创建flask代码



页面上的数据，想要提交到后台：

- form标签包裹要提交的数据的标签。

  - 提交方式：method="get"
  - 提交的地址：action="提交的地址"
  - form标签里面必须有一个submit标签

- 在form里面的一些标签：input/select/textarea

  - 一定要写name数据

  



## 总结

1、称呼

```html
-浏览器能够识别的标签（不专业）
-HTML标签

什么是html？超文本传输语言（与浏览器搭配）
```

2、HTML标签（默认格式样式、以后通过手段可以修改）

3、html标签与编程语言无关

- Java+html
- c#+html
- php+html
- python+html

4、提醒：html标签比较多，标签还有很多很多，不必一一学会。





# 3、CSS样式

css,专门用来“美化”标签。

- 基础CSS，写简单页面&看懂&改
- 模块，调整和修改。



## 3.1 快速了解

```html
<img src="..."style="height:100px"/>

<div style="color:red;">中国联通</div>
```



## 3.2 CSS应用方式

### 1.在标签上

```html
<img scr="..." style="hight:100px" />

<div style="color:red;">中国联通</div>
```



### 2.在head标签中写style标签(*)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>用户注册</title>
    <style>
        .c1{
            color:red
        }
    </style>
</head>
<body>
<h1 class='c1'>用户注册</h1>
<h1 class='c1'>用户注册</h1>
<h1 class='c1'>用户注册</h1>

</body>
</html>
```



### 3.写到文件中(*)

```css
.cl{
    height:100px;
    
}
.c2{
    color:red;
}
```



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>用户注册</title>
    <link rel='stylesheet' href="common.css"/>
</head>
<body>
<h1 class='c1'>用户注册</h1>
<h1 class='c1'>用户注册</h1>
<h1 class='c2'>用户注册</h1>
<h1 class='c1'>用户注册</h1>
<h1 class='c2'>用户注册</h1>


</body>
</html>
```





### **案例：在flask中的引用**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>用户注册</title>
    <style>
        .c1{
        color:red;
        }
        .c2{
        height:50px;
        }
    </style>
</head>
<body>
<h1 class="c1">用户注册</h1>
<form method="get" action="/do/reg">
    <div class="c2">
  用户名：<input type="text" name="uu"/>
    </div>
    <div class="c2">
  密码：<input type="password" name="pp"/>
    </div>
  <input type="button" value="button按钮">
  <input type="submit" value="submit按钮">
</form>
</body>
</html>
    
```

### 引用css文件

```html
<link rel="stylesheet" href="../static/commons.css">
```





### 问题：用flask框架开发不方便

- 每次都需要重启
- 规定有些文件必须放在特定的文件夹
- 新创建一个页面
  - 函数
  - HTML文件

有没有一种方式，可以让我们快速编写前端的代码并查看效果，最后再将页面集中到flask中

pycharm为我们提供了一种便捷的前端开发工具。

![image-20220516211346528](C:\Users\RUWU\AppData\Roaming\Typora\typora-user-images\image-20220516211346528.png)



## 3.3 CSS的选择器

- id选择器（id只能有一个）

  ```html
  #c1{
  
  }
  <div id="c1"></div>
  ```

  

- 类选择器（用的最多）

  ```html
  .c1{
  
  }
  <div class="c1"></div>
  ```

  

- 标签选择器（太绝对）

  ```html
  div{
  
  }
  <div>xxx</div>
  ```

- 属性选择器

  ```html
  input[type='text']{
              border:1px solid red;
          }
  .v1[xx="456"]{
  	color:gold;
   }
  
  <input type="text">
  <input type="password">
  
  <div class="v1" xx="123">s</div>
  <div class="v1" xx="456">f</div>
  <div class="v1" xx="999">h</div>
  ```

- 后代选择器	

```html
.yy > a{
            color:pink;
        }
```

```html
<div class="yy">
    <a>百度</a>
    <div>
        <a>谷歌</a>
    </div>
    <ul>
        <li>北京</li>
        <li>上海</li>
        <li>广东</li>
    </ul>
</div>
```



关于选择器

```html
多：类选择器、标签选择器、后代选择器
少：属性选择器、ID选择器
```

关于多个样式&覆盖的问题

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
  <style>
    .c1{
      color:red;
      border:1px solid red;
    }
    .c2{
        font-size:28px;
        color:green;
    }
  </style>
</head>
<body>
  <div class="c1 c2">中国联通</div>
</body>
</html>
```



补充：下面的不要覆盖我。

```html
<style>
    .c1{
      color:red !important;
      border:1px solid red;
    }
    .c2{
        font-size:28px;
        color:green;
    }
  </style>
```



## 3.4 样式

### 1.高度和宽度

```html
<style>
    .c1{
    height:300px;
    width:500px;
    }
  </style>
```

- 宽度，支持百分比；高度不支持。
- 行内标签：默认无效
- 块级标签：默认有效（霸道，右侧区域空白，也不给你占用）



### 2.块级和行内标签

- 块级
- 行内
- css样式：标签->`display:inline->block`



示例：行内&块级特性

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .c1{
        display:inline-block;
        height:100px;
        width:300px;
        border:1px solid red;
        }
    </style>
</head>
<body>
<div class="c1">中国</div>
<div class="c1">联通</div>

</body>
</html>
```

注意：块级+块级&行内



### 3.字体设置

- 颜色
- 大小
- 加粗
- 字体格式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .c1{
            color:red;
            font-size:19px;
            font-weight:400;
            font-family: Microsoft Yahei;
        }
    </style>
</head>
<body>
  <div class="c1">中国联通</div>
    <div>中国移动</div>
</body>
</html>
```



### 4.文字对其方式

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .c1{
            color:red;
            font-size:19px;
            font-weight:400;
            font-family: Microsoft Yahei;
            border:1px solid red;
            text-align:center; /*水平方向居中*/
            line-height:59px; /*垂直方向居中*/
        }
    </style>
</head>
<body>
  <div class="c1">中国联通</div>
    <div>中国移动</div>
</body>

```



### 5.浮动

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<div>
    <span>左边</span>
    <span style="float: right">右边</span>
</div>

</body>
</html>
```

div默认块级标签（霸道），如果浮动起来，就不一样了

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .c1{
            float:left;
            width:280px;
            height:170px;
            border:1px solid red;
        }
    </style>
</head>
<body>
<div>
    <div class="c1"></div>
    <div class="c1"></div>
    <div class="c1"></div>
    <div class="c1"></div>
    <div class="c1"></div>

</div>

</body>
</html>
```



如果你让标签浮动起来之后，就会脱离文档流。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .c1{
            float:left;
            width:280px;
            height:170px;
            border:1px solid red;
        }
    </style>
</head>
<body>
<div style="background-color:blue">
    <div class="c1"></div>
    <div class="c1"></div>
    <div class="c1"></div>
    <div class="c1"></div>
    <div class="c1"></div>
    <div style="clear:both;"></div>

</div>

</body>

```



### 6.内边距

内边距，我自己的内部设置一点距离。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .outer{
            border: 1px solid red;
            height:400px;
            width:200px;
            padding-top:20px;
            padding-left:20px;
            padding-right:20px;
            padding-bottom:20px;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div style="background-color:gold">
            听妈妈的话
        </div>
        <div>小朋友，你是否有很多问号</div>
    </div>

</body>

```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        .outer{
            border: 1px solid red;
            height:400px;
            width:200px;
            padding:20px;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div style="background-color:gold">
            听妈妈的话
        </div>
        <div>小朋友，你是否有很多问号</div>
    </div>

</body>

```

### 7.外边距

外边距：我与别人加点距离。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <div style="height:200px;background-color:blue;"></div>
    <div style="background-color:red;height:100px;margin-top:100px"></div>
</body>
</html>
```



### ###案例：小米商城

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
  <style>
        body{
            margin:0;
        }
    .header{

      background-color:black;

    }
    .header .menu{
        float:left;
        color:white;
        height:38px;
        line-height:38px;
    }
    .header .account{
        float:right;
        color:white;
        height:38px;
        line-height:38px;
    }
    .container{
        width:1226px;
        margin:0 auto;

    }
  </style>
</head>
<body>
  <div class="header">
        <div class="container">
          <div class="menu">
              <a>小米商城</a>
              <a>MIUI</a>
              <a>云服务</a>
              <a>有品</a>
              <a>小爱开放平台</a>
          </div>
          <div class="account">右边</div>
          <div style="clear:both"></div>
        </div>
  </div>

</body>

```

