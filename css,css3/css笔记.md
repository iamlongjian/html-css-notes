#### CSS的定义：CSS全称为“层叠样式表 (Cascading Style Sheets)”，它主要是用于定义HTML内容在浏览器内的显示样式，如文字大小、颜色、字体加粗等。

- 三种方式及它的优先级：内联式（在标签内）> 嵌入式（在文档头部）> 外部式（引入css文件）
 [![F9fJts.png](https://s1.ax1x.com/2018/11/21/F9fJts.png)](https://imgchr.com/i/F9fJts)
选择器=选择符（上图）：
标签选择器：p{`css样式代码` },h1{`css样式代码` },h2{`ss样式代码 `}……
类选择器:：.类名{`css样式代码`}
ID选择器：#ID名称{`css样式代码`}
类选择器和ID选择器的差别：类选择器可以使用多次，ID选择器整个文档中只能使用一次。
通用选择器：*{ `css样式代码`} 匹配html中所有标签元素

- 子选择器
选择器子选择器，即大于符号(>),用于选择指定标签元素的第一代子元素：
`.first>span{
	color:red;
}`
以上例子：first类下的span字体为红色。

#### 伪类选择器
1. :hover 鼠标经过
2. :link 鼠标没点击过
3. :visited 鼠标点击过
4.  :active鼠标点击的一瞬间
5.  :focus鼠标聚焦时
#### 伪元素选择器
- `::after{}` 元素之前 `::before{}`元素之后
- `div p::frist-child{}`div下的第一个p元素，`div p::last-child{}`div下的最后一个p元素，`div p::nth-child{3}`div下的第3个p元素
- 想要一段话的第一个字母字号变大：
```
HTML
    <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. </p>
```
```
CSS伪类选择器::first-letter
        <style>
        p::first-letter{
           font-size: 50px;
        }
	    </style>
```

- 分组选择符：当你想为两个类设置同一种样式
`h1,p{css}
.first,.second>span{css}`

- CSS继承：
其CSS样式不仅仅用于其本身，也可用在其后代
如:`<p>321<span>123132</span>123</p>` 如果为p标签设置css，则span标签样式也将改变，单独设置p标签和span标签才可独立。
标签的权值为1，类选择符的权值为10，ID选择符的权值最高为100。

- 层叠：[![F9f37Q.png](https://s1.ax1x.com/2018/11/21/F9f37Q.png)](https://imgchr.com/i/F9f37Q)  该P标签将会设置为绿色。
重要性： [![F9flnS.png](https://s1.ax1x.com/2018/11/21/F9flnS.png)](https://imgchr.com/i/F9flnS)加入`!important `  该P标签将会设置为红色。

- 文字排版
字体：
一般使用 `font-family:“Microsoft Yahei”;`
字号：`font-size:`
字体颜色：`color:`
字体粗度：`font-weight:bold`
斜体：`font-style:italic（斜体）`
下划线：`text-decoration:underline; `去除下划线:`text-decoration:none;`
删除线：`text-decoration:line-through; ` [![F9fGkj.png](https://s1.ax1x.com/2018/11/21/F9fGkj.png)](https://imgchr.com/i/F9fGkj)
缩进`：p{text-indent:2em} `p标签内元素首航缩进2em(文字的两倍大小)
行间距(行高)：`p{line-height:2em} `行间距为2em;
字(字母)间距：`p{letter-sapcing:2em} `字间距为2em;
对齐方式: `text-align:center`(居中对齐)  `text- align:right`(右对齐)  `text- align:left`(左对齐)
px最常用，1em=14px;
- 元素分类display
**块状元素：`div,section,p,h1-h6,ol,ul,dl,table,address,blockquote,form`** 
独占一行，可设置宽高和边距，宽度不设置则占父容器的100%。
**内联元素（行内元素）:`a,span,br,i,em,strong,label,q,var,code……`**
和其他元素共存一行，不可设置宽高边距，宽度即为文字或者图片的实际宽度。
**内联块状元素：`input,img`**
和其他元素共存一行，可设置宽高和边距。
**内联转换为块级的方式:`display:block;`**
**块级转换为内联的方式:`display:inline;`**
**内联块级元素:`display:inline-block;`**


- 盒子模型
![FCCOx0.png](https://s1.ax1x.com/2018/11/21/FCCOx0.png)
`Margin`外边距，`padding`内边距，`border`边框，
计算一个元素的实际占位： `margin+border+padding+width;`
块级元素都具备盒子模型的特性。

- 边框:border
粗细，样式，颜色：p{border：2px solid red};
样式可以有dashed虚线 solid实线 dotted点线
单独设置边框：`border-top`,`border-bottom`,`border-right`,`border-left`
舍去某个边框: `border-top:none;`

- 内边距:padding                外边距：margin
padding{上 右 下 左}			margin{上 右 下 左}

- css布局模型
流动模型（Flow）浮动模型（Float）层模型（Layer）

1. 流动模型为网页默认的布局样式。（块级元素独占一行，内联元素按宽度来决定）
2. 浮动模型为：`float:left/right；`（可以让两个块级元素并排显示）
3. 层模型为3种：
- 绝对定位：`position:absolute;`（这条语句将元素从文档流中拖出来，然后使用left,right,top.bottom对于其最接近的一个具有定位属性的父包含块进行绝对定位。）
```
    div{
    	position:absolute;
    	left:200px; 左边空出200px
    	top:20px; 上边空出20px
    }
```
- 相对定位：position:relative;（没有从文档流中脱离出来，占据着一定位置，使用left,right,top.bottom对其定位。）
```
    .div1{
    	position:absolute;
    	left:200px; 左边空出200px
    	top:20px; 上边空出20px
    }
```
固定定位：position:fixed;（它与绝对定位相似，只是它的相对移动的坐标是整个“视图窗口”，不会随着滚动条的滚动而改变位置，使用left,right,top.bottom对其定位。）
```
    .div1{
    	position:fixed;
    	left:200px; 左边空出200px
    	top:20px; 上边空出20px
    }
```
#### 相对定位与绝对定位一般组合使用：
1.	相对定位属性一定要是绝对定位属性的前辈级元素
2.	绝对定位属性要加`position:absolute;`
3.	即可对绝对定位属性使用left,right,top.bottom对其定位
 [![F9f10g.png](https://s1.ax1x.com/2018/11/21/F9f10g.png)](https://imgchr.com/i/F9f10g)
[![F9facV.png](https://s1.ax1x.com/2018/11/21/F9facV.png)](https://imgchr.com/i/F9facV)

效果： [![F9fYhn.png](https://s1.ax1x.com/2018/11/21/F9fYhn.png)](https://imgchr.com/i/F9fYhn)


[![F9fNpq.png](https://s1.ax1x.com/2018/11/21/F9fNpq.png)](https://imgchr.com/i/F9fNpq)
[![F9fU10.png](https://s1.ax1x.com/2018/11/21/F9fU10.png)](https://imgchr.com/i/F9fU10)
 
水平居中

- 行内元素水平居中方法:先给行内元素设置一个class，然后给其class定义属性：`text-align：center;`
块级元素水平居中方法:直接给块级元素设置属性：`margin{20px auto};`上下外边距随意，左右外边距设置为自动。
不定宽块状元素水平居中方法：
1.	在其外部加上table标签，使得变成块级元素，然后使用`margin{20px auto};`
2.	把不定宽块级元素设置为行内元素，再使用`text-align：center;`
3.	把不定宽块级元素的父元素设置`position:relative ; float:left ; left:50% ;`其本身设置为：`position:relative; left:-50% ;`
垂直居中
插入table标签，包括tbody，tr，td，并且使得td标签拥有height属性。


- 隐性改变display属性
当你为元素设置：`position：absolute`或者`float：left/right`时，该元素就会变为**inline-block**，自然拥有内联块状元素的所有属性（可设置宽高）。

 - 脱离文档流的属性
float和absolute
----------
1. 三列布局的方式
自适应的话直接将左中右三块宽度设置为：33.33%

2. 两边固定，中间自适应方法如下：
左右设置为`position:absolute;left:0`或者`right:0；top:0`；
中间设置`margin{0 右边固定宽度 0 左边固定宽度}`；
-----------