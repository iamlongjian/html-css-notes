## HTML基本标签用法
- `<em>`，`<strong>`强调标签
- `<q>`短文本引用标签（浏览器会自动为引用文本加上””）
- `<blockquote>`标签，长文本引用(浏览器会自动缩进)
[![F95g9s.png](https://s1.ax1x.com/2018/11/21/F95g9s.png)](https://imgchr.com/i/F95g9s)
- `<br />`换行标签
- `&nbsp` 空格标记
- `<hr>`标签，添加水平横线 
- `<address>`为网页加入地址信息（渲染效果为斜体，可后期通过css改变样式）
- `<code>`加入代码
- `<pre>`使用此标签为网页中加入大量代码
- 无序列表：`<ul><li>`使用列表标签为网页添加新闻信息列表
  [![F95sAg.png](https://s1.ax1x.com/2018/11/21/F95sAg.png)](https://imgchr.com/i/F95sAg)
- 有序列表：`<ol><li>`列表前将会展示其索引

#### div的作用
- `<div>`标签的作用就相当于一个容器，每一个独立的板块都可以用div包裹住（h5建议用`section`）
- id属性（唯一），class属性（可复用）

#### 表格（table）
- 整个表格以`<table>`标记开始、`</table>`标记结束。
tr=table row 表格行
th=table head 表格标题
td=table data 表格列（数据）
[![F956hj.png](https://s1.ax1x.com/2018/11/21/F956hj.png)](https://imgchr.com/i/F956hj)
`<caption>`标签为表格添加标题
#### a标签
- `<a>`标签：`<a  href="目标网址"  title="鼠标滑过显示的文本"  target=“_blank“(在新窗口打开)>链接显示的文本</a>`
- 可以使用mailto在网页中连接email地址，方法如下：
如果mailto后面同时有多个参数的话，第一个参数必须以“?”开头，后面的参数每一个都以“&”分隔。
 [![F95yNQ.md.png](https://s1.ax1x.com/2018/11/21/F95yNQ.md.png)](https://imgchr.com/i/F95yNQ)
#### img标签
- `<img src="图片地址" alt="下载失败时替换的文本" title="提示文本">`
#### 使用表单(form)标签，与用户交互：
- `<form   method="传送方式(get/post)"   action="服务器文件(save.php)"></form>`
表单控件
输入框：`<input  type=”text(文本)/password(密码)/reset(重置)/ submit(提交)” value=”输入框的默认值” name=”输入框的名称” placeholder=“想要用户输入的值“ />`
- label标签(主要为了增大用户的点击区域):
`<label for=”指向控件的ID” />标签的 for 属性中的值应当与相关控件的 id 属性值一定要相同。 `
[![F95DHS.png](https://s1.ax1x.com/2018/11/21/F95DHS.png)](https://imgchr.com/i/F95DHS)
- 文本域:
`<textarea rows=”文本域的行数” col=”文本域的列数”></textarea>`
- 单选框，复选框：
`<input type=”radio/checkbox” value=”值” name=”单选所有选项要一致，复选所有选项不一致”>`
radio单选框 
checkbox复选框
- 下拉列表(select)：
```
<select multiple(此属性 为 多选)>
	<option value=”向服务器发送的值” >显示1</option>
	<option value=”向服务器发送的值” >显示2</option>
    <option value=”向服务器发送的值” selected(默认选中)>显示3</option>
	<option value=”向服务器发送的值” >显示4</option>
</select>
```

