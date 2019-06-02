[TOC]



# 如何用 MarkDown 生成左边框目录

### 步骤1 : 使用`[TOC]`生成一个自带的目录

### 步骤2 :   导出生成 .html 文件

### 步骤3 : 删除body样式,添加如下样式

```css
body {
    /*width: 45em;*/
    border: 1px solid #ddd;
    outline: 1300px solid #fff;
    margin: 16px auto;
}

/*左边目录框的样式*/
.left-div 
{
height: 100%; /*目录框的高度*/
float:left;/*目录框的位置*/
overflow-y:scroll;/*目录框添加滚动条*/
padding-right: 10px;
position: fixed;/*目录框相对浏览器进行定位*/
width:17%;/*目录框的宽度*/
}
/*右边正文的样式*/
.right-div 
{
float:right;/*正文的位置*/
padding-left: 10px;/*边距*/
width:80%;/*正文的宽度*/
}
```

### 步骤4 : 修改HTML

```css
<body>
<div class="left-div">
这里是[TOC]命令生成的目录
</div>

<div class="right-div">
    这里是正文部分
</div>
</body>
```



大体如下:

```html
<html>
<head>
    <style>
        body 
        {
        /*width: 45em;*/
        border: 1px solid #ddd;
        outline: 1300px solid #fff;
        margin: 16px auto;
        }
        .left-div 
        {width:17%;
        float:left;
        padding-right: 10px;
        position: fixed;
        overflow-y:scroll;
        height: 80%}
        .right-div 
        {
        width:80%;
        float:right;
        padding-left: 10px;
        }
    </style>
</head>
<body>
    <!--article标签中就是我们编写的文本内容-->
    <article>
        <div class="left-div">这里是[TOC]命令生成的目录</div>
        <div class="right-div">这里是正文部分</div>
    </article>
</body>
</html>
```





https://blog.csdn.net/zjiang1994/article/details/52250363