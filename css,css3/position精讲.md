### Position的五个状态：
1. static（默认排列方式）
2. relative（仍然处于文档流，但可以用t r b l来改变元素的位置→相对于元素本身）
3. absolute（脱离文档流，可以用t r b l来改变元素的位置→相对于窗口来改变位置）
4. fixed（脱离文档流，可以用t r b l来改变元素的位置→相对于窗口来改变位置（不受滚轮影响））
5. inherit（继承父级元素的浮动属性）
#### Position的层级关系：
- 每个带有定位属性的元素都是有层级的，先写的会被后写的所覆盖。
 >>z-index（只作用于带有定位属性的元素）的层级关系：
 [![F9fATH.md.png](https://s1.ax1x.com/2018/11/21/F9fATH.md.png)](https://imgchr.com/i/F9fATH)
Z-index属性追随其父元素的z-index，如果父元素的值大，则子元素无论设置多小，都会继承父级的值。

- 水平垂直居中的代码(test2相对于test1水平垂直居中)：
[![F9fk0e.png](https://s1.ax1x.com/2018/11/21/F9fk0e.png)](https://imgchr.com/i/F9fk0e)