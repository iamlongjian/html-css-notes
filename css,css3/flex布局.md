### 基于display:flex;
### Flex布局是什么
- Flex是Flexible Box的缩写，意为”弹性布局”，用来为盒状模型提供最大的灵活性。
任何一个容器都可以指定为Flex布局。
**注意，设为Flex布局以后，子元素的float、clear和vertical-align属性将失效。**
![FPwhJU.png](https://s1.ax1x.com/2018/11/22/FPwhJU.png)
#### 容器(父元素)属性
1. flex-direction属性(四个值)
`flex-direction`决定了item的排列方向(direction)。
```
(默认值)flex-direction:row; 		主轴为水平方向，起点在左端。
flex-direction:row-reverse; 		主轴为水平方向，起点在右端。
flex-direction:column; 					主轴为垂直方向，起点在上沿。
flex-direction:column-reverse; 		主轴为垂直方向，起点在下沿。
```
2. flex-wrap属性(三个值)
`flex-wrap`属性定义：如果一条轴线拍不下所有item时,该如何换行。
```
flex-wrap:wrap;      					 换行，不影响元素width。
flex-wrap:no-wrap; 					不换行，元素width被挤压。
flex-wrap:wrap-reverse; 			换行，第一行在最下面。第二行从左边起。
```
3. flex-flow属性(定义flex-direction和flex-wrap的简写)
`flex-flow: row  wrap;`
4. justify-content属性(六个值)
`justify-content`定义了item在主轴上的对齐方式
```
justify-content:flex-start; 			item左对齐
justify-content:flex-end; 				item右对齐
justify-content:center;					 item居中显示
justify-content:space-between; 		两端对齐，项目之间的间隔都相等。
jusiify-content:space-around;			 每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。
jusiify-content:space-evenly; 				项目之间的间隔与项目与边框的间隔 **相同** ;
```
5. align-items属性()
`align-items`定义了item在交叉轴上如何对齐
```
align-items:flex-start;             交叉轴的起点对齐。
align-items:flex-end;               交叉轴的终点对齐。
align-items:center;                 交叉轴的终点对齐。
align-items:baseline;               item中第一行文字基线对齐。
align-items:stretch;(默认值)        如果项目未设置高度或设为auto，将占满整个容器的高度。
```
.align-content属性()
`align-content`定义了item在多条交叉轴的对齐方式，如果只有一条则不起作用。
```
align-content:flex-start;           与交叉轴的起点对齐。
align-content:flex-end;             与交叉轴的终点对齐。
align-content:center;               与交叉轴的中点对齐。
align-content:space-between;        与交叉轴两端对齐，轴线之间的间隔平均分布。
align-content:space-around;         每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
align-content:stretch（默认值）;     轴线占满整个交叉轴。
```
#### 项目(子元素)属性
1. order属性
`order:整数`        当数字越小时(默认为0)，优先级就越高，越排在前面。
2. flex-grow属性
`flex-grow:数字`    属性定义项目的放大比例，默认为`0`，即如果存在剩余空间，也不放大。 
3. flex-shrink属性
`flex-shrink:数字`  属性定义了项目的缩小比例，默认为`1`，即如果空间不足，该项目将缩小。
4. flex-basis属性
`flex-basis:<length> | auto;`    属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。
5. flex属性
`flex:`              属性是flex-grow, flex-shrink 和 flex-basis的简写，默认值为0 1 auto。后两个属性可选。
6. align-self属性
`align-self:auto | flex-start | flex-end | center | baseline | stretch;`       属性允许单个项目有与其他项目不一样的对齐方式，可覆盖`align-items`属性。默认值为`auto`，表示继承父元素的`align-items`属性，如果没有父元素，则等同于`stretch`。