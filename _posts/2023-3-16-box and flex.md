# 2023-3-16-box and flex
## 盒模型
### padding
#### 四个方向
一定要记得每个方向之间是空格隔开！
```css
.box{padding:150px 100px 50px 0px;}
```
顺时针 上 右 下 左
```css
.box{padding:100px 50px 100px;}
```
上 左右 下 
...以此类推
#### 单一方向
```css
.box{padding:0 0 100px 0;}
```
意思为上右左全为0px，而下端为100px
```css
.box{padding-top/right/bottom/left:100px;}
```
### margin
与padding类似
```css
.box{margin:atuo;}
```
使整个盒子水平居中，但不能控制垂直居中
### 盒子大小的计算
#### 真实大小
不计算margin
#### 元素所占的大小
加上margin
### 盒的分类
#### W3C盒（标准盒）
padding和border会改变盒的真实大小
```css
.box{box-sizing:content-box;}
```
#### IE盒
padding和border不会改变盒的真实大小，但会使content变小
```css
.box{box-sizing:border-box;}
```
## Flex弹性布局
```css
.box{display:flex;}
```
针对某个（父）元素【容器】添加 display:flex;所有的子元素（项目）在一行显示。
```html
<section>
    <div class="box1">块1</div>
    <div class="box2">块2</div>
    <div class="box3">块3</div>
    <div class="box4">块4</div>
    <div class="box5">块5</div>
  </section
```
```css
section{
  width: 500px;
  height: 400px;
  border: 10px solid red;
  margin:100px auto;
}
section>div{
  width: 60px;
  height: 60px;
}
.box1{ background-color: rgb(121, 121, 239);}
.box2{ background-color: rgb(199, 228, 11);}
.box3{ background-color: rgb(42, 241, 28);}
.box4{ background-color: rgb(203, 56, 236);}
.box5{ background-color: rgb(0, 242, 255);}
```
section叫做容器  div是他的项目
### 换行
```css
.box{flex-wrap: wrap;}
/*换行*/
.box{flex-wrap: wrap-reverse;}
/*换行，且在第一行最下方*/
.box{flex-wrap: nowrap;}
/*不换行*/
```
### 主轴对齐
justify-content：主轴对齐方式：项目在主轴（ x 轴）上的对齐方式
取值：
flex-start：【默认】主轴的起点对齐（左对齐）
flex-end：主轴的终点对齐（右对齐）
center：主轴的中间点对齐（中间对齐）
space-between：项目和容器之间的距离 = 项目和项目之间的距离 * 0
space-around：项目和容器之间的距离 = 项目和项目之间的距离 * 0.5
space-evenly：项目和容器之间的距离 = 项目和项目之间的距离 * 1
### 交叉轴对齐
align-items：交叉轴对齐方式：项目在交叉轴（ y 轴）上的对齐方式
取值：
flex-start：交叉轴的起点对齐。
flex-end：交叉轴的终点对齐。
center：交叉轴的中点对齐。
baseline: 项目的第一行文字的基线对齐。
stretch（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。