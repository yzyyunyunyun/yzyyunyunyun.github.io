# 3.14学习的代码
## a元素--超链接

```html
<a href="https://www.4399.com">打开4399</a>
<!--链接网站需要加网络协议，https或http-->
<a href="secret of my heart.html">secret of my heart</a>
<!--本地文件-->
```
## img元素--插入图片
```html
<img src="我是废物.jpg" alt="我是废物">
<!--同个文件夹里直接输入名称插入即可-->
<img src="https://img.alicdn.com/imgextra/i1/6000000007589/O1CN01WjCw1I25voYm3q3s1_!!6000000007589-0-octopus.jpg" alt="淘宝图片">
<!-- 如何用图片超链接 -->
```
## 用图片进行超链接
```html
<a href="https://4399.com"><img src="建筑平面图.png" alt="建筑平面图"></a>
```
## 快速多个嵌套
header>nav>a*3{内容}
## 语义化
```html
<body>
	<header>
		<P>头部</p>
	</header>
	<nav>
		<a href="https://www.4399.com">导航</a>
	</nav>
	<article>
		<p>左边的主体文章</p>
		<section>块</section>
	</article>
	<aside>
		<p>侧边栏</p>
		<div>块<div>
	</aside>
	<footer>
		<p>尾部</p>
	</footer>
</body>
```