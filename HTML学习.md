## HTMl学习(https://www.bilibili.com/video/BV14J4114768/)

### 简介

网页：网站中的“一页”，构成网站的基本元素，通常由图片、文字、链接、声音等元素组成，通常是.html或.htm文件(统称html文件)。

html：Hyper Text Markup Language，超文本标记语言。不是编程语言，是标记语言，即一套标记标签。

常用Web浏览器：IE、Edge、firefox、Safari、Chrome、Opera

### HTML标签

标签成对出现，需要闭合。

一个html文件所含标签大致如下图：

![img](https://www.runoob.com/wp-content/uploads/2013/06/02A7DD95-22B4-4FB9-B994-DDB5393F7F03.jpg)

```html
//文档类型声明，作用是告诉浏览器使用哪种HTML版本来显示网页
<!DOCTYPE html>
```

```html
//完整HTML页面；属性lang是当前文档显示语言(en,zh-CN,fr)——但是en仍然可以显示中文、zh-CN可显示中文
<html lang = "en">...</html>
```

```html
//头部元素；包含了元(meta)数据，如<meta charset="utf-8">定义html文档使用的字符编码(GB2312,BIG5,GBK,UTF-8)
<head></head></head>
//页面主体：
<body></body>
```

```html
//标题标签；重要性递减，字体大小和粗细度递减
<h1></h1>......<h6></h6>
//段落标签：把HTML文档中的文字分成若干段落，段落间有较大缝隙
<p></p>
//换行标签：强制将文字换行，行间无缝隙
<br/>
//文字加粗标签：
<strong></strong>或<b></b>
//文字倾斜标签：
<em></em>或<i></i>
//文字删除线标签：
<del></del>或<s></s>
//文字下划线标签：
<ins></ins>或<u></u>
//盒子标签：装内容的区域，无语义，div独占一行)（大盒子），span一行可以多个（小盒子）
<div></div>和<span></span>
//图像标签：src属性是img标签的必须属性，指定图像文件的路径和文件名；alt属性是图片不能显示时的文字替换；title属性是鼠标放在图片上的文字提示；width和height属性是图片尺寸；border属性是图片边框
<img src="图像url" />
//超链接标签：href属性是链接url地址；target属性是链接打开方式，有_self(默认)当前窗口打开，_blank新窗口打开，_parent父窗口打开
<a href="https://www.baidu.com"></a>
```

HTML的部分特殊字符代码如下图（重点记s忆空格符小于号大于号，其余符号需要时再查询即可）：

![HTML特殊字符](https://pic.imgdb.cn/item/63b7ce45be43e0d30e4ae044.png)

```html
<!--表格标签：<table></table>定义表格，<thead></thead>包括表格头部区域，<tbody></tbody>包括表格主体区域，<tr></tr>定义表格的行，必须嵌套在<table></table>中，<td></td>定义表格的单元格（<th></th>定义表格的表头单元格），必须嵌套在<tr></tr>中，其属性有align、border、cellpadding、cellspacing、width-->
<table>
    <thead>
        <tr>
            <th></th>
            <th></th>
            <th></th>
        </tr>
    </thead>
	<tbody>
        <tr>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
        </tr>
    </tbody>
</table>
//合并单元格：跨行合并代码写在需要合并的单元格中最上侧的单元格，跨列合并代码写在需要合并的单元格中最左侧的单元格，之后要删除多余的单元格
<td rowspan="合并单元格个数"></td>
<td colspan="合并单元格个数"></td>
```

```html
//无序列表：无顺序级别，ul标签之间只能嵌套li标签，li标签之间可嵌套所有元素（相当于一个容器）
<ul>
    <li><p></p></li>
    <li><a></a></li>
    <li><img src="图片.jpg"></li>
</ul>
//有序列表：有排列顺序，ol标签之间只能嵌套li标签，li标签之间可嵌套所有元素
<ol>
    <li><p></p></li>
    <li><a></a></li>
    <li><img src="图片.jpg"></li>
</ol>
//自定义列表：一个dt通常对应多个dd，可以有多个dt
<dl>
    <dt>加入我们</dt>
    <dd>社会招聘</dd>
    <dd>校园招聘</dd>
    <dd>国际招聘</dd>
</dl>
```

```html
//表单：表单域、表单控件（表单元素）、提示信息；<form></form>定义表单域，其范围内的表单信息被提交给服务器，action属性接收并处理表单的服务器程序URL地址，method属性设置表单提交方式（GET/POST），name属性置顶表单名称以区分同一页面的多个表单域
<form action="test.php" method="post" name="formtest">
</form>
//表单元素：input的type属性中，text是明文文本框，password是密码框，radio是单选按钮，checkbox是复选框，submit是提交按钮，button是按钮，file是文件上传按钮，reset是表单重置按钮；name属性定义input元素名称，同类单选按钮name必须相同，所有元素都要有name和value。type是input元素类型，name是input元素名称，value是input元素值，checked规定此input元素首次加载时应被选中，maxlength是输入字段最大长度
<input type="" name="" value="">
//标注标签：绑定一个表单元素，当点击label标签内的文本，会选中对应的表单元素，增加用户体验。
<input type="radio" name="gender" id="nan">
<label for="nan">男</label>
//下拉菜单标签：<select></select>中至少包含一对<option>标签，定义有selected="selected"的option标签，是默认选中项。
<select>
    <option>初中</option>
    <option>高中（中专）毕业</option>
    <option>专科</option>
    <option>本科</option>
    <option>硕士</option>
    <option>博士及以上</option>
</select>
//文本域标签：定义多行文本输入，适用于用户输入内容较多的情况
<textarea>   
</textarea>
```
