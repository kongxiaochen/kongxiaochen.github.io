# HTML5&CSS3

## HTML5

- 新增的标签
1. datalist 
`<datalist>
<label for="country_name">国家 : </label><input id="country_name" name="country_name" type="text" list="country" />
<datalist id="country">
   <option value="Afghanistan 阿富汗">
   <option value="Albania 阿尔巴尼亚">
   <option value="Algeria 阿尔及利亚">
   <option value="Andorra 安道尔共和国">
   <option value="Angola 安哥拉">
</datalist>
`
2. output
`
<form oninput="x.value=parseInt(a.value)+parseInt(b.value)">0
<input type="range" id="a" value="50">100
+<input type="number" id="b" value="50">
=<output name="x" for="a b"></output>
</form>
`
3. video audio
4. progess
5. canvas

- 新增的语义化标签
(5) <article>
定义外部的内容。比如来自一个外部的新闻提供者的一篇新的文章，或者来自 blog 的文本，或者是来自论坛的文本。亦或是来自其他外部源内容。
(6) <aside>
标签定义 article 以外的内容。aside 的内容应该与 article 的内容相关。
(7) <section>
(8) <header> <footer>
在HTML5标准中，新加了几个用于增添页面语义的标签，这些标签有：article、section、nav和aside等。与别的大多数标签不同，浏览器在解释渲染这些标签的时候仅仅把它作为普通的div块级元素来处理，不会添加任何额外的展现逻辑；也即，这些标签仅用于增添语义。对于Web开发人员而言，使用这些标签的实际意义主要有2点：搜索引擎优化，以及增加页面的可用性(accessibility)。
在元素分类上，article、section、nav和aside称之为“Sectioning Content”

HTML5提供了新的语义元素来明确一个Web页面的不同部分。
  ● <header>：描述了文档的头部区域，于定义内容的介绍展示区域
  ● <nav>：定义导航链接的部分。
  ● <section>：定义文档中的节（section、区段）。比如章节、页眉、页脚或文档中的其他部分，section通常 包含了一组内容及其标题。
  ● <article>：定义独立的内容。
  ● <aside>：定义页面主区域内容之外的内容（比如侧边栏）。
  ● <figure>：标签规定独立的流内容（图像、图表、照片、代码等等）。
  ● <figcaption>：定义 <figure> 元素的标题。
  ● <footer>：述了文档的底部区域，一个页脚通常包含文档的作者，著作权信息，链接的使用条款，联系信息等。
在一个网页中，这些新的语义标签元素位置如下图所示：


2. 新增的属性
表单属性
（1）placeholder
（2）required="required"
（3）form属性，表单外部的元素也属于表单范围
（4）autofocus
（5）autocomplete="off"/"on"
（6）list 与datalist元素一起使用
其他属性
（3）manifest属性 html标签上使用

（3）data 属性  存储用户的自定义数据
<div id=”myDiv” data-custom-attr=”My Value”> Bla Bla </div> 
CSS中使用： 
<style> 
h1:hover:after { 
content: attr(data-hover-response); 
color: black; 
position: absolute; 
left: 0; 
} 
</style> 
<h1 data-hover-response=”I Said Don’t Touch Me!”> Don’t Touch Me </h1> 
（4）input type="range"
<input type=”range”  step=”1″ value=”5"> 
3.客户端存储
localStorage  永久
sessionStorage 一次会话
方法
locationStorage.setItem('key', value);
locationStorage.getItem('key');
locationStorage.removeItem('key');
locationStorage.clear();
4. 新的技术 websocket
http://www.cnblogs.com/doudouxiaoye/p/5656681.html
var socket=new WebSocket('ws://game.example.com:12010/updates');
socket.onopen = function(){
  setInterval(function(){
  if(socket.bufferedAmount == 0)
     socket.send(getUpdateData();
  },50) 
}
CSS3
1.动画 animation
<!DOCTYPE html>
<html>
<head>
<style> 
div
{
width:100px;
height:100px;
background:red;
position:relative;
animation:myfirst 5s linear 2s infinite alternate;
/* Firefox: */
-moz-animation:myfirst 5s linear 2s infinite alternate;
/* Safari and Chrome: */
-webkit-animation:myfirst 5s linear 2s infinite alternate;
/* Opera: */
-o-animation:myfirst 5s linear 2s infinite alternate;
}

@keyframes myfirst
{
0%   {background:red; left:0px; top:0px;}
25%  {background:yellow; left:200px; top:0px;}
50%  {background:blue; left:200px; top:200px;}
75%  {background:green; left:0px; top:200px;}
100% {background:red; left:0px; top:0px;}
}

@-moz-keyframes myfirst /* Firefox */
{
0%   {background:red; left:0px; top:0px;}
25%  {background:yellow; left:200px; top:0px;}
50%  {background:blue; left:200px; top:200px;}
75%  {background:green; left:0px; top:200px;}
100% {background:red; left:0px; top:0px;}
}

@-webkit-keyframes myfirst /* Safari and Chrome */
{
0%   {background:red; left:0px; top:0px;}
25%  {background:yellow; left:200px; top:0px;}
50%  {background:blue; left:200px; top:200px;}
75%  {background:green; left:0px; top:200px;}
100% {background:red; left:0px; top:0px;}
}

@-o-keyframes myfirst /* Opera */
{
0%   {background:red; left:0px; top:0px;}
25%  {background:yellow; left:200px; top:0px;}
50%  {background:blue; left:200px; top:200px;}
75%  {background:green; left:0px; top:200px;}
100% {background:red; left:0px; top:0px;}
}
</style>
</head>
<body>

<p><b>注释：</b>本例在 Internet Explorer 中无效。</p>

<div></div>

</body>
</html>
2.过渡 transition
div
{
width:100px;
height:100px;
background:yellow;
transition:width 2s;
-moz-transition:width 2s; /* Firefox 4 */
-webkit-transition:width 2s; /* Safari and Chrome */
-o-transition:width 2s; /* Opera */
}

div:hover
{
width:300px;
}
2. 2D变换 translate
