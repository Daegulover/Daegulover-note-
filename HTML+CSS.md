# Day 1--HTML

## 常用标签

h1-h6     标题标签

p             段落标签

div          段落标签

span       段落标签

### a              超链接

#### 超链接标签

作用：点击跳转到其他页面

标签名：**`<a href="链接">显示文字</a>`**

`target` 属性赋值 `"_blank"` 可实现新窗口跳转页面

例如：`<a href="https://lufangqian.top" target="_blank">陆方七安的导航</a>`

本示例意为在新窗口打开指向`lufangqian.top`网站的名叫陆方七安的导航的超链接

> 开发初期，不知道超链接的跳转地址，href属性值写#，表示空链接，不会跳转

a标签还可以跳转到特定位置，可以给要跳转到的位置的标签添加一个id，在a标签中给hef的值设置为#id名

```
<a href="#top">返回顶部</a>

<!-- 在页面的顶部放置一个id为top的元素 -->
<div id="top"></div>
```

去除超链接默认样式

```
a {
    color: inherit; /* 使用父元素的颜色 */
    text-decoration: none;
}
```



dl            定义列表

dt           

dd

<!DOCTYPE html> <html>  <body>    <dl>     <dt>苹果</dt>     <dd>一种常见的水果，通常为红色或绿色，富含维生素和纤维素。</dd>     <dt>香蕉</dt>     <dd>一种热带水果，呈弯曲的长条形，外皮为黄色，果肉柔软，富含钾元素。<!DOCTYPE html>
<html>
<body>

  <dl>
    <dt>苹果</dt>
    <dd>一种常见的水果，通常为红色或绿色，富含维生素和纤维素。</dd>
    <dt>香蕉</dt>
    <dd>一种热带水果，呈弯曲的长条形，外皮为黄色，果肉柔软，富含钾元素。</dd>
    <dt>橙子</dt>
    <dd>一种柑橘类水果，通常为圆形，外皮为橙色，果肉多汁，富含维生素C。</dd>
  </dl>

</body>

</html></dd>     <dt>橙子</dt>     <dd>一种柑橘类水果，通常为圆形，外皮为橙色，果肉多汁，富含维生素C。</dd>   </dl>  </body>  </html>





ul             无序列表

ol             列表中有特殊的顺序

li              列表中的每一个具体的项目





### input

​        text                  默认值。单行的文本字段，输入值中的换行会被自动去除。

​        password        一般是输入密码

​        button              按钮

​                            button 是普通按钮  不会跳转

​                            submit 是提交按钮  会跳转 

​	radio 	       单选按钮，允许在多个拥有相同 [`name`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/input#name) 值的选项中选中其中一个。

​	checkbox         复选框

​	color                 用于指定颜色的控件；在支持的浏览器中，激活时会打开取色器。

​	email		用于写邮箱

​	date		  写日期

​	file		    让用户选择文件的控件。使用 [`accept`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/input#accept) 属性规定控件能选择的文件类型。

​	image 	      插入图片

​	number	   用于输入数字的控件。如果支持的话，会显示滚动按钮并提供缺省验证（即只能输入数字）。拥有动态键盘的设备上会显示数字键盘

​	reset	         重置

#### input标签

input 标签 比较特殊 Type属性值不同，则功能不同

标签名：

```html
<input type="……">
```



| Type 属性值 | 说明                     |
| ----------- | ------------------------ |
| text        | 文本框，用于输入单行文本 |
| password    | 密码框                   |
| radio       | 单选框                   |
| checkbox    | 多选框                   |
| file        | 上传文件                 |



占位文本：提示信息

> 当有多个文本输入框时，占位文本可以提示输入，此属性可用于文本框与密码框

在input标签中添加属性 `placeholder`

```html
<input type="……" placeholder="提示信息">
```

 取消type在css的那个线条



##### 单选框 radio

常用属性：

| 属性名  | 作用     | 特殊说明                             |
| ------- | -------- | ------------------------------------ |
| name    | 控件名称 | 控件分组，同组只能选中一个(单选功能) |
| checked | 默认选中 | 属性名和属性值相同，简写为一个单词   |

> name属性相同将划分为一组，同组的单选框只能有一个被选中



##### 上传文件 file

使用 `multiple` 属性可以实现文件多选



##### 多选框 checkbox

多选框也叫复选框

默认选中：checked

```html
<input type="checkbox" checked>
```



#### 下拉菜单

使用例子：用户注册时选择城市时可以使用下拉菜单选择城市

标签名：`select` 嵌套 `option`, `select`是下拉菜单的整体，`option`是下拉菜单的每一项

标签名：

```html
<select>
    <option>北京</option>
    <option>上海</option>
    <option>深圳</option>
    <option>广州</option>
    <option>武汉</option>
    <option selected>下北泽</option>
</select>
```

> selected属性为默认选项



#### 文本域

作用：多行输入文本的表单控件

标签名：`textarea` 双标签

> 提示文字在双标签里，或者使用 placeholder



#### Label标签

作用：网页中，某个标签的说明文本

tips：用 `Lable` 标签绑定文字和表单控件的关系，增大表单控件的点击范围

实现此功能有两个写法

实现方法：

- 写法一

label 标签只包裹内容，不包过表单控件

这只 label 标签的 for 属性值 和 表单控件的 id 属性值相同

```html
<input type="radio" id ="man">
<label for="man">男</label>
```



- 写法二

label 标签中包含 input 标签，此时则不需要属性

```html
<label><input type="radio">男</label>
```

> 方法一中两个标签为并列的关系，方法二是label标签为父级，input为子级，属于包含关系



tips：支持 label 标签增大点击范围的表单控件有

- 文本框
- 密码框
- 上传文件
- 单选框
- 多选框
- 下拉菜单
- 文本域
- ……



#### 按钮标签

作用：与用户进行交互的重要对象，通常用于提交，选择等场景

标签名：

```html
<button type="">
    按钮
</button>
```

| Type属性值 | 说明                                             |
| ---------- | ------------------------------------------------ |
| submit     | 提交按钮，点击后可以提交数据到后台(默认选项)     |
| reset      | 重置按钮，点击后将表单控件恢复默认值             |
| button     | 普通按钮，默认没有功能，一般配合 JavaScript 使用 |



### 字符实体

作用：在网页中显示预留字符

| 显示结果 | 描述   | 实体名称 |
| -------- | ------ | -------- |
|          | 空格   | `&nbsp;` |
| <        | 小于号 | `&lt;`   |
| >        | 大于号 | `&gt;`   |



​	        



img		插入图片

br		   换行

hr		   下划线

tr		     表格行（table row）标签，用于定义表格中的一行



#### 表格

##### 表格标签

标签名：table > tr > td / th

| 标签名 | 说明       |
| ------ | ---------- |
| table  | 表格       |
| tr     | 行         |
| th     | 表头单元格 |
| td     | 内容单元格 |

注释：在网页中，表格默认没有边框线，使用border属性可以添加边框线

案例：

 <table border="1">
        <tr>
            <th>表头1</th>
            <th>表头2</th>
            <th>表头3</th>
        </tr>
        <tr>
            <td>第二行第一格</td>
            <td>第二行第二格</td>
            <td>第二行第三格</td>
        </tr>



##### 表格结构标签

作用：用表格结构标签把内容划分区域，让表格结构更清晰，语义更清晰

| 标签名 | 含义     | 特殊说明     |
| ------ | -------- | ------------ |
| thead  | 表格头部 | 表格头部内容 |
| tbody  | 表格主题 | 主要内容区域 |
| tfoot  | 表格底部 | 汇总信息区域 |





table	       表格标签

tbody	      主要用于将表格的主体内容进行分组

tfoot 	       创建表脚，通常包含表格的汇总信息、合计数据或其他与表格整体相关的注释性内容

label		为表单控件（如输入框、复选框、单选按钮等）提供关联文本，增强表单的可用性和可访问性

textarea	  创建一个多行文本输入框，用户可以在其中输入大量的文本内容

form		各种表单元素

select	       用于创建下拉列表或选择框

option	     下拉列表中选项的标签，它必须嵌套在<select>标签内使用，用来提供具体的可选项

nav		   跟div标签差不多的

...



#### 合并单元格

作用：将多个单元格合并成一个单元格，以合并同类信息

其中，跨行合并与跨列合并不同

合并时会保留**最左**、**最上**单元格中的内容

属性：

- 跨行合并，保留最上单元格，添加属性 `rowspan`
- 跨列合并，保留最左单元格，添加属性 `colspan`

> 本属性应用于<td>、<th>等子级标签

rowspan		上下 纵向 行合并

colspan		  左右 横向 列合并





# Day 2--CSS

## **优先级**

特点：优先级也叫权重，当一个标签使用了多种选择器时，基于不同种类的选择器的匹配规则

规则：选择器指向性越强，其优先级越高优先生效

排列：

通配符选择器 < 标签选择器 < 类选择器 < id选择器 < 行内样式 < !impotant

## **属性名** 

| color            | 文字颜色 |
| ---------------- | -------- |
| font-size        | 字体大小 |
| width            | 宽度     |
| height           | 高度     |
| background-color | 背景色   |

## 字体属性

| 名称         | 属性名          | 说明              |
| ------------ | --------------- | ----------------- |
| 字体大小     | font-size       | 修改文字大小      |
| 字体粗细     | font-weight     | 修改文字粗细      |
| 字体倾斜     | font-style      | 使文字倾斜        |
| 行高         | font-height     | 修改行高          |
| 字体族       | font-family     | 修改字体 如：楷体 |
| 字体复合属性 | font            | 复合属性          |
| 文本缩进     | text-indent     | 修改前后缩进      |
| 文本对齐     | text-align      | 修改文本对齐方式  |
| 修饰线       | text-decoration | 上中下贯文本的线  |
| 字体颜色     | color           | 修改文字颜色      |

## 文本修饰线

属性名：

| 属性值       | 效果   |
| ------------ | ------ |
| none         | 无     |
| underline    | 下划线 |
| line-through | 删除线 |
| overline     | 上划线 |

## 颜色样式

| 表示方式        | 说明                                                | 属性值               |
| --------------- | --------------------------------------------------- | -------------------- |
| 普通 color      | 输入单独的颜色就行                                  | 英文单词             |
| 带#000000或#000 | 更加精确的颜色                                      | #000000              |
| rgb表示模式     | r表示红色 g表示绿色 b表示蓝色                       | rgb（0，0，0）       |
| rgba表示模式    | rgb如上 a代表的透明度 取值在0-1之间 越靠近1颜色越纯 | rgba（0，0，0，0.3） |

## **背景属性**

**背景图**

属性名：background-image(bgi)

属性值：url(背景图的 URL)

在网页中，使用背景图实现 **装饰性** 的图片效果

## 背景平铺方式

属性名：background-repeat (bgr)

*no-repeat：只有一张图片，显示在容器的左上角不会扩展

*repeat：复制图片填满容器

*repeat-x：只有横向复制图片

*repeat-y：只有竖向复制图片





vh：视窗高度

vw:视窗宽度









## 链接样式 css伪类选择器

不同的链接可以有不同的样式。

链接的样式，可以用任何CSS属性（如颜色，字体，背景等）。

特别的链接，可以有不同的样式，这取决于他们是什么状态。

这四个链接状态是：

> a:link - 正常，未访问过的链接
>
> a:visited - 用户已访问过的链接
>
> a:hover - 当用户鼠标**放在**链接上时
>
> ​             鼠标移动上去，会变大
>
> a:active - 链接被点击的那一刻





## 分组选择器

h1
{
    color:green;
}
h2
{
    color:green;
}
p
{
    color:green;
}





## 交集选择器

p.marked{ }



## 后代选择器

后代选择器用于选取某元素的后代元素。

```css
div p {
    background-color:yellow; /*选择div的所有后代p元素*/
}  
```



### 子元素选择器

与后代选择器相比，子元素选择器（Child selectors）只能选择作为某元素子元素的元素。

```css
div>p {
    background-color:yellow; /*选择div的所有子元素p元素*/
}
```



### 相邻兄弟选择器

相邻兄弟选择器（Adjacent sibling selector）可选择紧接在另一元素后的元素，且二者有相同父元素。

如果需要选择紧接在另一个元素后的元素，而且二者有相同的父元素，可以使用相邻兄弟选择器（Adjacent sibling selector）。

```css
div+p {
    background-color:yellow; /*选择div之后紧邻的兄弟p元素*/
}
```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div+p{
            color: aqua;
        }
    </style>
</head>
<body>
    <div>一级div选择器</div>
    <p>p标签</p>
    <p>p2标签</p>
</body>
</html>



### 后续兄弟选择器

后续兄弟选择器选取所有指定元素之后的所有兄弟元素。

```css
div~p {
    background-color:yellow;
}
```

**案例**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    div~p{
      color: red;
    }
  </style>
</head>
<body>
  <div>d1</div>
  <p>2</p>
  <p>3</p>
</body>
</html>
```

## 

## CSS属性选择器

| 选择器           | 示例            | 示例说明                                   |
| ---------------- | --------------- | ------------------------------------------ |
| attribute        | [target]        | 选择所有带有target属性元素                 |
| attribute=value  | [target=_blank] | 选择所有使用target="-blank"的元素          |
| attribute~=value | [title~=flower] | 选择标题属性**包含单词**"flower"的所有元素 |

#### target=-blank 和 target=self 的区别

​	blank是在此网页中另外出来一个网页

​	self 不能

​	案例：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        [target]{
            color: aquamarine;
            width: 100px;
            height: 200px;
        }
        
        }
    </style>
</head>
<body>
    <a href="https://www.baidu.com" target="_blank">baidu</a><br>
    <a href="https://cn.bing.com/" title~=flower>biying</a><br>
    <a href="https://www.jd.com/" target="_self">jingdong</a>
</body>
</html>
```



#### title

​	title=“abb”  双引号后面可以接任意的

​	案例：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        [target]{
            color: aquamarine;
            width: 100px;
            height: 200px;
        }

        [title~=abb]{
            color: blue;
        }
    </style>
</head>
<body>
    <a href="https://www.baidu.com" target="_blank">baidu</a><br>
    <a href="https://cn.bing.com/" title~=flower>biying</a><br>
    <a href="https://www.jd.com/" target="_self">jingdong</a>

    <p title="abb">this is abb.</p>
    <p title="sam">im sam .hello .</p>
    <p title="abb">abb</p>
</body>
</html>
```





## CSS伪元素选择器(和元素内容有关)

::before 伪元素：会在所选元素的内容之前插入一个虚拟的子元素。这个伪元素默认是行内元素（display: inline）。
::after 伪元素：会在所选元素的内容之后插入一个虚拟的子元素，同样默认是行内元素。

| 选择器        | 示例           | 示例说明                                                     |
| ------------- | -------------- | ------------------------------------------------------------ |
| :first-letter | p:first-letter | 选择每一个```<P>```元素的第一个字母                          |
| :first-line   | p:first-line   | 选择每一个```<P>```元素的第一行                              |
| **:after**    | **p:after**    | **在每个```<p>```元素之后插入内容使用content 属性来指定要插入的内容。** |
| **:before**   | **p:before**   | **在每个```<p>```元素之前插入内容使用content 属性来指定要插入的内容。** |

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        a:after {
            content: " 🔗";
        }

        a:before {
            content: "🌐 ";
        }
    </style>
    <title>示例 3</title>
</head>

<body>
    <a href="https://www.example.com">示例网站</a>
    <a href="https://www.google.com">谷歌</a>
</body>

</html>
```







## CSS结构伪类选择器

概念：

伪类选择器是 CSS 中一种特殊的选择器，它用于选择处于特定状态的元素或元素的特定部分，这些状态并非是 HTML 文档结构中的固有属性，而是基于元素的行为、位置、状态等动态特征来进行选择。

| 选择器               | 示例                    | 示例说明                                                     |
| -------------------- | ----------------------- | ------------------------------------------------------------ |
| `:first-child`       | `p:first-child`         | 指定只有当 `<p>` 元素是其父级的第一个子级的样式。            |
| `:last-child`        | `div:last-child`        | 选择父元素的最后一个子元素（例如，如果 `div` 是最后一个子元素则应用样式）。 |
| `:nth-child(n)`      | `ul li:nth-child(2)`    | 选择父元素的第 `n` 个子元素（例如，选择 `ul` 中的第二个 `li` 元素）。 |
| `:nth-last-child(n)` | `div:nth-last-child(1)` | 从父元素的最后一个子元素开始计数，选择第 `n` 个子元素。      |
| `:only-child`        | `p:only-child`          | 选择父元素中唯一的子元素（例如，如果 `p` 是唯一的子元素则应用样式）。 |
| `:empty`             | `div:empty`             | 选择没有子元素的元素（包括没有文本内容的元素）。             |
| `:not`               | `:not(p)`               | 选择所有不是 `p` 元素的元素。                                |
| `:root`              | `:root`                 | 选择文档的根元素（通常是 `html` 元素）。                     |
| `:target`            | `#example:target`       | 选择当前活动的片段标识符（即 URL 中 `#` 后面的部分）。       |
| `::before`           | `p::before`             | 在元素的内容之前插入内容（通常与 `content` 属性一起使用）。  |
| `::after`            | `p::after`              | 在元素的内容之后插入内容（通常与 `content` 属性一起使用）。  |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        :root{
            --main-color:#887733;
        }
        ul li:nth-child(2){
            color: var(--main-color)
        }
    </style>
</head>
<body>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
    </ul>
</body>
</html>
```





## CSS Display

display属性设置一个元素应如何显示。

| 值           | 描述                                                 |
| ------------ | ---------------------------------------------------- |
| none         | 此元素不会被显示。                                   |
| block        | 此元素将显示为块级元素，此元素前后会带有换行符。     |
| inline       | 默认。此元素会被显示为内联元素，元素前后没有换行符。 |
| inline-block | 行内块元素。（CSS2.1 新增的值）                      |







## CSS Visibility

visibility属性指定一个元素应可见还是隐藏。

| 值      | 描述                   |
| ------- | ---------------------- |
| visible | 默认值。元素是可见的。 |
| hidden  | 元素是不可见的。       |

**display和visibility案例：**

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    .box {
      width: 200px;
      height: 100px;
      margin: 10px;
      background: lightblue;
      border: 2px solid blue;
    }

    .display-none {
      display: none; /* 完全隐藏且不占空间 */
    }

    .visibility-hidden {
      visibility: hidden; /* 隐藏但保留空间 */
    }

    /* 子元素可见性控制示例 */
    .parent {
      visibility: hidden;
      background: pink;
      padding: 20px;
    }
    .child {
      visibility: visible; /* 强制子元素可见 */
    }
  </style>
</head>
<body>
  <div class="box">正常元素</div>
  <div class="box display-none">display: none 的元素</div>
  <div class="box">display: none 的上方元素会顶上来</div>

  <div class="box visibility-hidden">visibility: hidden 的元素</div>
  <div class="box">visibility: hidden 的下方元素不会移动</div>

  <!-- 子元素可见性示例 -->
  <div class="parent">
    父元素被隐藏
    <div class="child">但子元素仍然可见</div>
  </div>
</body>
</html>
```





### css display 和 css visibility 有什么区别

visibility：主要用于控制元素的可见性，它可以使元素在页面上不可见，但元素仍然会占据页面布局中的空间。
display：用于定义元素在页面中的显示方式，不仅可以隐藏元素，还能改变元素的布局类型，隐藏元素时不占据页面布局空间。



## CSS鼠标样式

| 属性   | 说明                                                         |
| ------ | ------------------------------------------------------------ |
| cursor | 显示光标移动到指定的类型url    auto    crosshair    default    **pointer**    move    e-resize     ne-resize    nw-resize    n-resize    se-resize    sw-resize    s-resize    w-resize    text    wait    help |

**光标案例：**

```Html
css鼠标手型cursor中hand与pointer
Example：CSS鼠标手型效果 <a href="#" style="cursor:hand">CSS鼠标手型效果</a><br/>
Example：CSS鼠标手型效果 <a href="#" style="cursor:pointer">CSS鼠标手型效果</a><br/>
注：pointer也是小手鼠标，建议大家用pointer，因为它可以兼容多种浏览器。<br/>
Example：CSS鼠标由系统自动给出效果 <a href="#" style="cursor:auto">CSS鼠标由系统自动给出效果</a><br/>
Example：CSS鼠标十字型 效果 <a href="#" style="cursor:crosshair">CSS鼠标十字型 效果</a><br/>
Example：CSS鼠标I字型效果 <a href="#" style="cursor:text">CSS鼠标I字形效果</a><br/>
Example：CSS鼠标等待效果 <a href="#" style="cursor:wait">CSS鼠标等待效果</a><br/>
Example：CSS鼠标默认效果 <a href="#" style="cursor:default">CSS鼠标默认效果</a><br/>
Example：CSS鼠标向右的箭头效果 <a href="#" style="cursor:e-resize">CSS鼠标向右的箭头效果</a><br/>
Example：CSS鼠标向右上箭头效果 <a href="#" style="cursor:ne-resize">CSS鼠标向右上箭头效果</a><br/>
Example：CSS鼠标向上箭头效果 <a href="#" style="cursor:n-resize">CSS鼠标向上箭头效果</a><br/>
Example：CSS鼠标向左上箭头效果 <a href="#" style="cursor:nw-resize">CSS鼠标向左上箭头效果</a><br/>
Example：CSS鼠标向左箭头效果 <a href="#" style="cursor:w-resize">CSS鼠标向左箭头效果</a><br/>
Example：CSS鼠标向左下箭头效果 <a href="#" style="cursor:sw-resize">CSS鼠标向左下箭头效果</a><br/>
Example：CSS鼠标向下箭头效果 <a href="#" style="cursor:s-resize">CSS鼠标向下箭头效果</a><br/>
Example：CSS鼠标向右下箭头效果 <a href="#" style="cursor:se-resize">CSS鼠标向下箭头效果</a><br/>
```





## 盒模型相关样式

![image-20250306081921336](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250306081921336.png)

![image-20250306081954656](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250306081954656.png)

Margin(外边距)：清除边框外的区域，外边距是透明的。（盒子与盒子之间的距离）

Border(边框)：围绕在内边距和内容外的边框。

Padding(内边距)：清除内容周围的区域，内边距是透明的。

Content(内容区域)：盒子的内容，显示文本和图像。



## css边框

![image-20250306082046361](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250306082046361.png)

![image-20250306082101800](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250306082101800.png)

![image-20250306082114602](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250306082114602.png)

## CSS 轮廓

轮廓（outline）是绘制于元素周围的一条线，**位于边框边缘的外围**，可起到突出元素的作用。

轮廓（outline）属性指定元素轮廓的样式、颜色和宽度。

| 属性          | 描述                           |
| ------------- | ------------------------------ |
| outline       | 在一个声明中设置所有的轮廓属性 |
| outline-color | 设置轮廓的颜色                 |
| outline-style | 设置轮廓的样式                 |
| outline-width | 设置轮廓的宽度                 |



## CSS DIV样式

box-shadow 属性来给设置div阴影，只需要给div元素添加“box-shadow”属性，即可给DIV设置阴影

box-shadow 属性把一个或多个下拉阴影添加到框上。该属性是一个用逗号分隔阴影的列表，每个阴影由 2-4 个长度值、一个可选的颜色值和一个可选的 inset 关键字来规定。省略长度的值是 0。

| 值         | 说明                                         |
| ---------- | -------------------------------------------- |
| *h-shadow* | 必需的。水平阴影的位置。允许负值             |
| *v-shadow* | 必需的。垂直阴影的位置。允许负值             |
| *blur*     | 可选。模糊距离                               |
| *spread*   | 可选。阴影的大小                             |
| *color*    | 可选。阴影的颜色。                           |
| inset      | 可选。从外层的阴影（开始时）改变阴影内侧阴影 |

<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"> 
<style> 
div {
        width:300px;
        height:100px;
        background-color:yellow;
        box-shadow: 10px 10px 5px #888888;
    }
</style>
</head>
<body>
         <div></div>
</body>
</html>
## css定位

属性：position  指定元素的定位类型

子觉父相

![image-20250306095828193](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250306095828193.png)

![image-20250306100336959](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250306100336959.png)![image-20250306100501112](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250306100501112.png)

用相对定位 绝对定位和固定定位 固定top





### relative 相对定位

元素相对于原来的位置进行偏移

### ![image-20250306104251663](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250306104251663.png)





### absolute 绝对定位

绝对定位是相对祖先元素进行偏移

absolute 定位的元素和其他元素重叠               





### sticky 粘性定位

自己不会动，只有滚动页面的时候会动，滚动页面的时候到页面最顶端时，他就不动了

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>sticky 定位</title>
<style>
div.sticky {
    position: -webkit-sticky;
    position: sticky;
    top: 0;
    padding: 5px;
    background-color: #cae8ca;
    border: 2px solid #4CAF50;
}
</style>
</head>

<body>
    <p>尝试滚动页面。</p>
    <p>注意: IE/Edge 15 及更早 IE 版本不支持 sticky 属性。</p>

    <div class="sticky">我是粘性定位!</div>

    <div style="padding-bottom:2000px">
        <p>滚动我</p>
        <p>来回滚动我</p>
        <p>滚动我</p>
        <p>来回滚动我</p>
        <p>滚动我</p>
        <p>来回滚动我</p>
    </div>

</body>
</html>
```





### fixed    固定定位

跟浏览器的位置而动   就是滚动条在动，但是用固定定位定位的不会动

案例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=
    , initial-scale=1.0">
    <title>Document</title>
    <style>
        /* 绝对定位 */
        .abb{
            position: absolute;
            width: 100px;
            height: 300px;
            border: 2px solid #ccc;
        }
        .juedui{
            position: absolute;
            width: 34px;
            height: 55px;
            border: 4px solid #556;
            margin: 40px;
        }
        /* 相对定位 */
        .add{
            position: relative;
            width: 300px;
            height: 400px;
            box-shadow: 2px 2px 50px;
        }
        .xiangdui{
            position: relative;
            width: 79px;
            height: 49px;
            border: 2px solid #000;
            /* margin: 80px; */
            padding: 40px;
        }
        /* 粘性定位 */
        .bba{
            position: sticky;
            width: 90px;
            height: 40px;
            background-color: #689;
            border-left: 3px solid #000;
            line-height: 40px;
        }
        .nianxing{
            position: sticky;
            width: 40px;
            height: 50px;
            background-color: #700;
            line-height: 40px;
            /* top: 50px;
            right: 70px; */
        }
    </style>
</head>
<body>
    <div class="abb">
        <div class="juedui">绝对定位</div>
    </div>
    <div class="add">
        <div class="xiangdui">相对定位</div>
    </div>
    <div class="bba">
        <div class="nianxing">粘性定位</div>
    </div>
</body>
</html>
```





## CSS元素堆叠顺序

| **属性** | **说明**           |
| -------- | ------------------ |
| z-index  | 设置元素的堆叠顺序 |

拥有更高堆叠顺序的元素总是会处于堆叠顺序较低的元素的前面。

注释：元素可拥有负的 z-index 属性值。      

**z-index**  **仅能在定位元素上奏效(重点)**

案例代码：

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    /* 基础容器样式 */
    .container {
      position: relative;
      width: 300px;
      height: 300px;
      margin: 50px auto;
      background: #eee;
    }

    /* 通用方块样式 */
    .box {
      position: absolute;
      width: 200px;
      height: 200px;
      padding: 20px;
      border: 2px solid black;
    }

    /* 堆叠顺序演示 */
    .red {
      background: rgba(255, 0, 0, 0.8);
      top: 30px;
      left: 30px;
      z-index: 1;
    }

    .blue {
      background: rgba(0, 0, 255, 0.8);
      top: 60px;
      left: 60px;
      /* 未设置 z-index (默认为 auto) */
    }

    .green {
      background: rgba(0, 255, 0, 0.8);
      top: 90px;
      left: 90px;
      z-index: 2;
    }

  </style>
</head>
<body>
  <!-- 基础堆叠顺序演示 -->
  <div class="container">
    <div class="box red">z-index: 1</div>
    <div class="box blue">默认堆叠顺序</div>
    <div class="box green">z-index: 2</div>
  </div>

  
</body>
</html>
```





## CSS溢出处理

CSS overflow 属性用于控制内容溢出元素框时显示的方式。

| 属性       | 说明                                              |
| ---------- | ------------------------------------------------- |
| overflow   | 设置当元素的内容溢出其区域时发生的事情。          |
| overflow-y | 指定如何处理顶部/底部边缘的内容溢出元素的内容区域 |
| overflow-x | 指定如何处理右边/左边边缘的内容溢出元素的内容区域 |

如果元素中的内容超出了给定的宽度和高度属性，overflow 属性可以确定是否显示滚动条等行为。

这三个样式属性有四个共同的值:

​        **visible**​        默认值。内容不会被修剪，会呈现在元素框之外。



​        **hidden​**        内容会被修剪，并且**其余内容是不可见的**。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .abb{
            width: 200px;
            height: 40px;
            border: 2px solid #998;
            overflow: hidden;
        }
    </style>
</head>
<body>
    <div class="yichu">
        <div class="abb">niaho zheshi zhuoyueban youxingqulaima womemkeyidainiyiqiwan youxingquma </div>
    </div>
</body>
</html>
```



​        **scroll​**        内容会被修剪，但是浏览器会**显示滚动条**以便查看其余的内容。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .abb{
            width: 200px;
            height: 60px;
            border: 2px solid #998;
            overflow: scroll;
        }
    </style>
</head>
<body>
    <div class="yichu">
        <div class="abb">niaho zheshi zhuoyueban youxingqulaima womemkeyidainiyiqiwan youxingquma </div>
    </div>
</body>
</html>
```



​        **auto​**        如果内容被修剪，则浏览器会显示滚动条以便查看其余的内容。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .abb{
            width: 200px;
            height: 77px;
            border: 2px solid #998;
            overflow: auto;
        }
    </style>
</head>
<body>
    <div class="yichu">
        <div class="abb">niaho zheshi zhuoyueban youxingqulaima womemkeyidainiyiqiwan youxingquma </div>
    </div>
</body>
</html>
```







## CSS元素浮动

CSS 的 float（浮动），会使元素向左或向右移动，其周围的元素也会重新排列。

| 属性  | 说明                                                         |
| ----- | ------------------------------------------------------------ |
| float | 指定一个盒子（元素）是否可以浮动。left：元素向左浮动。right：元素向右浮动。none：默认值。元素不浮动，并会显示在其在文本中出现的位置 |

left：元素向左浮动。
right：元素向右浮动。
none：元素不浮动（默认值）。
inherit：元素继承其父元素的 float 属性值。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .class{
            width: 40px;
            height: 40px;
            background-color: #822;
            float: right;
        }
    </style>
</head>
<body>
    <div class="class"></div>
</body>
</html>
```





## CSS清除浮动

| 属性  | 说明                                                         |
| ----- | ------------------------------------------------------------ |
| clear | 指定不允许元素周围有浮动元素。left：在左侧不允许浮动元素。right：在右侧不允许浮动元素。both： 在左右两侧均不允许浮动元素。None  默认值。允许浮动元素出现在两侧。 |

clear其只会影响自身，不会对其他相邻元素造成影响

元素盒子的边不能和前面的浮动元素相邻，那么就是自己下移

![image-20250306195115896](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250306195115896.png)



![image-20250307095747102](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250307095747102.png)

![image-20250307100339760](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250307100339760.png)

### 元素居中对齐

要水平居中对齐一个元素(如 ```<div>```), 可以使用 margin: auto;或margin:0 auto。

设置到元素的宽度将防止它溢出到容器的边缘。

元素通过指定宽度，并将两边的空外边距平均分配：

```css
.center {
    margin: auto;
    width: 50%;
    border: 3px solid green;
    padding: 10px;
}
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .abb{
            width: 500px;
            height: 400px;
            background-color: #129;
            margin: auto;
        }
    </style>
</head>
<body>
    <div class="abb"></div>
</body>
</html>
```





### 文本居中对齐

如果仅仅是为了文本在元素内居中对齐，可以使用 text-align: center;

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .class{
            width: 300px;
            height: 500px; 
             border: 1px solid #000;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="class">nihaoya woshi wangjiamin yuanyiheworenshiyxiama</div>
</body>
</html>
```





### 左右对齐 - 使用定位方式

我们可以使用 position: absolute; 属性来对齐元素:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .abb{
            width: 400px;
            height: 20px;
            border: 5px solid #000;
            position: absolute;
            right: opx;
            padding: 23px;
        }
    </style>
</head>
<body>
    <div class="abb">xianghewozuopengyouma wohenhaoxiangchude woxianghenizuopengyouma wohenaini</div>
</body>
</html>
```





### 左右对齐 - 使用 float 方式

我们也可以使用 float 属性来对齐元素:

```css
.right {
    float: right;
    width: 300px;
    border: 3px solid #73AD21;
    padding: 10px;
}
```

当像这样对齐元素时，对 ```<body>``` 元素的外边距和内边距进行预定义是一个好主意。这样可以避免在不同的浏览器中出现可见的差异。

![image-20250307095619911](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250307095619911.png)

### 文本垂直居中对齐 - 使用 padding

CSS 中有很多方式可以实现垂直居中对齐。 一个简单的方式就是头部底部使用 padding:

```css
.center {
    padding: 70px 0;
    border: 3px solid green;
}
```

如果要水平和垂直都居中，可以使用 padding 和 text-align: center:





### 文本垂直居中 - 使用 line-height

line-height和height保持一致即可；

```css
.center {
    line-height: 200px;
    height: 200px;
    border: 3px solid green;
    text-align: center;
}
/* 如果文本有多行，添加以下代码: */
.center p {
    line-height: 1.5;
    display: inline-block;
    vertical-align: middle;
}
```



# CSS精灵截图技术

**其实就是通过将多个图片融合到一张图里面，然后通过CSS background背景定位技术技巧布局网页背景**。这样做的好处也是显而易见的，**因为图片多的话，会增加http的请求，会促使了网站性能的减低，特别是图片特别多的网站，如果能用css sprites降低图片数量，带来的将是速度的提升**。

属性：background-position: -50px -100px

用于设置背景图像的位置，通过设置具体的坐标值，可以精确地显示精灵图中的某个特定图标或图像部分



### 伪元素

::before 和 ::after
作用：这两个伪元素允许在选定元素的内容之前或之后插入额外的内容。通常用于添加装饰性元素、图标或一些辅助性的文本信息等。
示例：可以利用 ::before 或 ::after 伪元素来创建一个带箭头的提示框。在 HTML 中有一个类名为 tooltip 的元素，通过 CSS 设置 ::before 伪元素的 content 属性为一个空字符串，然后利用 border 属性来绘制一个三角形，作为提示框的箭头。





# css3新增选择器

## css3属性选择器

| 选择器           | 示例             | 实例说明                                          |
| ---------------- | ---------------- | ------------------------------------------------- |
| attribute^=value | a[src^="https"]  | 选择每一个src属性的值以"https"开头的元素          |
| attribute$=value | a[src$=".pdf"]   | 选择每一个src属性的值以".pdf"结尾的元素           |
| attribute*=value | a[src*="runoob"] | 选择每一个src属性的值包含子字符串"runoob"的元元素 |





## css3结构伪类选择器

| 选择器               | 示例                  | 实例说明                                                  |
| -------------------- | --------------------- | --------------------------------------------------------- |
| :first-of-type       | p:first-of-type       | 选择每个p元素是其父级的第一个p元素                        |
| :last-of-type        | p:last-of-type        | 选择每个p元素是其元素的最后一个p元素                      |
| :only-of-type        | p:only-of-type        | 选择每个p元素是其父级的唯一p元素                          |
| :only-child          | p:only-child          | 选择每个p元素是其父级的唯一子元素                         |
| :nth-child           | p:nth-child           | 选择每个p元素是其父级的第二个子元素                       |
| :nth-child(n)        | p:nth-child(2)        | 选择每个p元素的是其父级的第二个子元素，从最后一项开始计数 |
| :nth-last-child(n)   | p:nth-last-child(2)   | 选择每个p元素是其父级的第二个p元素                        |
| :nth-last-of-type(n) | p:nth-last-of-type(2) | 选择每个p元素的是其父级的第二个p元素，从最后一个计数      |
| :last-child          | p:last-child          | 选择每个p元素是其父级的最后一个子级。                     |





## css3伪元素选择器

| 选择器      | 示例        | 实例说明                                 |
| ----------- | ----------- | ---------------------------------------- |
| ::selection | ::selection | 匹配元素中被用户选中或处于高亮状态的部分 |





## CSS3表单选择器

| 选择器      | 示例          | 实例说明                                                     |
| ----------- | ------------- | ------------------------------------------------------------ |
| :enable     | input:enable  | 选择每一个已经启用的输入元素                                 |
| :disable    | input:disable | 选择每一个已经禁用的输入元素                                 |
| :checked    | input:disable | 选择每个选中的输入元素                                       |
| :read-write | :read-write   | 每个匹配可读及可写的元素:read-write选择器选取没有设置"readonly"属性的元素 |
| :read-only  | :read-only    | 用于匹配设置 "readonly"（只读） 属性的元素:read-only选择器选取设置 "readonly" 属性的元素。 |
| :optional   | :optional     | 用于匹配可选的输入元素用于匹配没有设置了 "required" 属性的元素 |
| :required   | :required     | 用于匹配设置了 "required" 属性的元素                         |





## css3其他的选择器

| 选择器         | 示例        | 实例说明                                          |
| -------------- | ----------- | ------------------------------------------------- |
| :root          | :root       | 选择文档的根元素                                  |
| :empty         | p:empty     | 选择每个没有任何子级的p元素（包括文本节点）       |
| :target        | #new:target | 选择当前活动的#new元素（包含该锚点名称的点击URL） |
| :not(selector) | :not(p)     | 选择每个并非p元素的元素                           |





# css颜色表示方法 

##### 1.RGBA方三原色配色方式

在RGB模式上新增了Alpha透明度。

 alpha 参数是介于 0.0（完全透明）与 1.0（完全不透明）的数字



##### 2.HSL模式

语法:HSL(H,S,L)，HSL分别表示色调，饱和度，亮度

 H:0(或360)表示红色，120表示绿色，240表示蓝色，也可取其他数值来指定颜色。取值为：0 - 360

 S:(饱和度)。取值为：0.0% - 100.0%

 L:(亮度)。取值为：0.0% - 100.0%



##### 3.HSLA模式

 HSL模式上新增了Alpha透明度



##### 4.transparent

transparent是全透明黑色(black)的速记法，即一个类似rgba(0,0,0,0)这样的值。

在CSS3中，transparent被延伸到任何一个有color值的属性上。IE8及以下，color属性值为transparent

时，文本显示为黑色。





## CSS3边框（重要）



### css3边框圆角

在 CSS2 中添加圆角棘手。我们不得不在每个角落使用不同的图像。

在 CSS3 中，很容易创建圆角。

在 CSS3 中 border-radius 属性被用于创建圆角：使用 CSS3 border-radius 属性，你可以给任何元素制作 "圆角"。

如果你在 border-radius 属性中只指定一个值，那么将生成 4 个 圆角。但是，如果你要在四个角上一一指定，可以使用以下规则：

##### 四个值：

从左到右是：左上 右上 右下 左下

##### 三个值：

从左到右是：左上 右上左下 右下

##### 两个值：

从左到右是：左上右下 右上左下

##### 一个值：

从左到右是：四个圆角相同

![image-20250309181538956](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309181538956.png)





### css3边框阴影（盒子阴影）

**属性：box-shadow**

box-shadow属性可以设置一个或多个下拉阴影的框。

box-shadow: h-shadow v-shadow blur spread color inset;

boxShadow 属性把一个或多个下拉阴影添加到框上。该属性是一个用逗号分隔阴影的列表，每个阴影由 2-4 个长度值、一个可选的颜色值和一个可选的 inset 关键字来规定。省略长度的值是 0。

| 值       | 说明                                                         |
| -------- | ------------------------------------------------------------ |
| h-shadow | 必需的，水平阴影的位置。允许负值                             |
| v-shadow | 必需的，垂直阴影的位置。允许负值                             |
| blur     | 可选，模糊距离                                               |
| spread   | 可选，阴影外延伸的大小                                       |
| color    | 可选，阴影的颜色，在CSS颜色值寻找颜色值的完整列表            |
| inset    | 可选，从外层的阴影（开始时）改变阴影内侧阴影，（默认值为outset） |

![image-20250309182445021](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309182445021.png)





### css3图片边框

![image-20250309183037136](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309183037136.png)

##### border-image-source:

边框背景图片，格式：url（“...”)

##### border-image-slice:

图片边框向内偏移的距离。格式：border-image-slice：top right bottom left。分别指切割背景图片的四条线距离上右下左的距离。 如下图所示：

![image-20250309183242008](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309183242008.png)

该距离接受数值，百分数。默认数值的单位是px,但是不能在数值后面加px，否则这句css将不被浏览器解析。

用法和margin，padding类似。这里以数值举例，百分数同理。

border-image-slice: 10; /距离上下左右均为*10px;*/

border-image-slice: 10 30; /距离上下*10px,*左右*30px;*/

border-image-slice: 10 30 20; /距离上*10px,*下*20px,*左右*30px;*/

border-image-slice: 10 30 20 40; /距离上*10px,*右*30px,*下*20px,*左*40px;*/

四条线将背景图分割成了9个部分，其中1,2,3,4,6,7,8,9这八个区域将会被切割，作为图片边框，如果除了设置数值或者百分数，还加了一个“fill”，那么区域5就会作为背景填充进元素content，如：

border-image-slice: 25 11 fill;

注意：slice不接受负值；如果slice切割的左右距离之和大于背景图的宽，则上下边框不显示。如果slice切割的上下距离之和大于背景图的高，则左右边框不显示。

##### border-image-width:

图片边框的宽度。只接受数值，且不能加单位。

##### border-image-repeat:

图像边框是否应平铺(repeat)、铺满(rounded)或拉伸(stretch)。而无论怎样铺，四个角，即区域1,3,7,9是不会重复铺，只会被相应拉伸。下面以最为经典的图为例吧：

![image-20250309183434848](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309183434848.png)

stretch（默认值）:

```html
.box{
	width: 50px;
	height: 50px;
	border: 40px solid transparent;
	border-image-source: url("img/border.png");
	border-image-slice: 27 fill;
	border-image-repeat: stretch;
}
<div class="box"></div>
```



![image-20250309183632036](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309183632036.png)

可以看到每个区域都被横向和纵向拉伸了

repeat:

```html
.box{
	width: 100px;
	height: 100px;
	border: 40px solid transparent;
	border-image-source: url("img/border.png");
	border-image-slice: 27 fill;
	border-image-repeat: repeat;
•}
<div class="box"></div>
```

![image-20250309183742895](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309183742895.png)

可以看到背景在以原形状等比例缩放以后，持续平铺，容易出现断层。



round:

```html
.box{
	width: 100px;
	height: 100px;
	border: 40px solid transparent;
	border-image-source: url("img/border.png");
	border-image-slice: 27 fill;
	border-image-repeat: round;
• }
<div class="box"></div>
```

![image-20250309183925613](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309183925613.png)

同样是重复平铺，但是round会处理得更平滑，不会出现断层情况，因此round通常比repeat更常用。

##### border-image-outset:

边框图像区域超出边框的量。格式：border-image-outset : length | number。length是数值加单位“px”，number指的是相对于边框宽度增加的倍数。

![image-20250309184202320](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309184202320.png)





## css3背景

### css3 background-image 属性

```html
#example1 {
	background-image: url(img_flwr.gif), url(paper.gif);
	background-position: right bottom, left top;
	background-repeat: no-repeat, repeat;
}
```

也可以通过复合属性来实现;

```html
#example1 {
	background: url(img_flwr.gif) right bottom no-repeat, url(paper.gif) left top repeat;
}
```



### css3 background-size属性

background-size指定背景图像的大小。CSS3以前，背景图像大小由图像的实际大小决定。

CSS3中可以指定背景图片，让我们重新在不同的环境中指定背景图片的大小。您可以指定像素或百分比大小。

你指定的大小是相对于父元素的宽度和高度的百分比的大小。

![image-20250309184618119](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309184618119.png)

##### 改变背景图片大小

![image-20250309184647200](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309184647200.png)

##### 伸展背景图片完全填充内容区域：

![image-20250309184723205](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309184723205.png)





### css3的background-origin属性

指定了背景图像的位置区域

![image-20250309184908563](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309184908563.png)

在 content-box 中定位背景图片：

```css
div {
	background:url(img_flwr.gif);
	background-repeat:no-repeat;
	background-size:100% 100%;
	background-origin:content-box;
}
```





### css3 background-cilp属性

CSS3中background-clip背景剪裁属性是从指定位置开始绘制。

![image-20250309185114019](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250309185114019.png)

```css
#example1 {
	border: 10px dotted black;
	padding: 35px;
	background: yellow;
	background-clip: content-box;
}
```









## CSS3渐变

### 概述

##### 属性：background-image

CSS3 渐变（gradients）可以让你在两个或多个指定的颜色之间显示平稳的过渡。

以前，你必须使用图像来实现这些效果。但是，通过使用 CSS3 渐变（gradients），你可以减少下载的时间和宽带的使用。此外，渐变效果的元素在放大时看起来效果更好，因为渐变（gradient）是由浏览器生成的。

CSS3 定义了两种类型的渐变（gradients）：

线性渐变（Linear Gradients）- 向下/向上/向左/向右/对角方向,沿着一条执行渐变

径向渐变（Radial Gradients）- 由它们的中心定义,从一点向四周渐变

渐变相关属性：background-image。



### css3线性渐变

为了创建一个线性渐变，你必须至少定义两种颜色结点。颜色结点即你想要呈现平稳过渡的颜色。同时，你也可以设置一个起点和一个方向（或一个角度）。

语法：

background-image: linear-gradient(direction/degree ,color-stop1, color-stop2, ...);

direction方向：渐变的方向位置，属性值可以为(to)left、right、top、bottom(可组合使用)

角度：渐变终止方向的角度，角度以deg表示

起始颜色......

终止颜色...... (颜色可以是多个)



#### 线性渐变-从上到下（默认情况）

下面的实例演示了从顶部开始的线性渐变。起点是红色，慢慢过渡到蓝色:

```css
#grad {
	background-image: linear-gradient(#e66465, #9198e5);
}
```





### 线性渐变-从左到右

```css
#grad { height: 200px; background-image: linear-gradient(to right, red ,
yellow); }
```





### 线性渐变-对角

```css
#grad { height: 200px; background-image: linear-gradient(to bottom right, red,yellow); }
```





### 使用角度

如果你想要在渐变的方向上做更多的控制，你可以定义一个角度，而不用预定义方向（to bottom、to top、to right、to left、to bottom right，等等）。

角度是指水平线和渐变线之间的角度，逆时针方向计算。换句话说，0deg 将创建一个从下到上的渐变，90deg 将创建一个从左到右的渐变。

![image-20250310213139678](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250310213139678.png)

```css
#grad { background-image: linear-gradient(-90deg, red, yellow); }
```



## CSS3 2D 转换

**新转换属性:**

| **Property** | **描述**               |
| ------------ | ---------------------- |
| transform    | 适用于2D或3D转换的元素 |

**2D 转换方法:**

| 函数(transform样式值)           | 描述                                                         |
| ------------------------------- | ------------------------------------------------------------ |
| matrix(*n*,*n*,*n*,*n*,*n*,*n*) | 定义 2D 转换，使用六个值的矩阵。                             |
| translate(*x*,*y*)              | 定义 2D 转换，沿着 X 和 Y 轴移动元素。x和y是像素值;可以是正数值,也可以是负数值 |
| translateX(*n*)                 | 定义 2D 转换，沿着 X 轴移动元素。                            |
| translateY(*n*)                 | 定义 2D 转换，沿着 Y 轴移动元素。                            |
| scale(*x*,*y*)                  | 定义 2D 缩放转换，改变元素的宽度和高度。x和y是数值,表示放大或缩小的倍数; |
| scaleX(*n*)                     | 定义 2D 缩放转换，改变元素的宽度。                           |
| scaleY(*n*)                     | 定义 2D 缩放转换，改变元素的高度。                           |
| rotate(*angle*)                 | 定义 2D 旋转，在参数中规定角度。                             |
| skew(*x-angle*,*y-angle*)       | 定义 2D 倾斜转换，沿着 X 和 Y 轴。                           |
| skewX(*angle*)                  | 定义 2D 倾斜转换，沿着 X 轴。                                |
| skewY(*angle*)                  | 定义 2D 倾斜转换，沿着 Y 轴。                                |





## 过渡

#### 属性：transition

CSS3 过渡是元素从一种样式逐渐改变为另一种的效果。

| 属性                       | 描述                                                         |
| -------------------------- | ------------------------------------------------------------ |
| transition                 | 简写属性，用于在一个属性中设置四个过渡属性。                 |
| transition-property        | 规定应用过渡的 CSS 属性的名称。                              |
| transition-duration        | 定义过渡效果花费的时间。默认是 0。（以秒或毫秒计）           |
| transition-timing-function | 规定过渡效果的时间曲线。默认是 "ease"。linear：规定以相同速度开始至结束的过渡效果。ease:规定慢速开始，然后变快，然后慢速结束的过渡效果。ease-in：规定以慢速开始的过渡效果。ease-out：规定以慢速结束的过渡效果。ease-in-out：规定以慢速开始和结束的过渡效果。 |
| transition-delay           | 规定过渡效果何时开始。默认是 0。                             |



## 动画

属性值：@keyframes

| **属性**                  | **描述**                                                     |
| ------------------------- | ------------------------------------------------------------ |
| @keyframes                | 规定动画。                                                   |
| animation                 | 所有动画属性的简写属性，除了 animation-play-state 属性。     |
| animation-name            | 规定 @keyframes 动画的名称。                                 |
| animation-duration        | 规定动画完成一个周期所花费的秒或毫秒。默认是 0。             |
| animation-timing-function | 规定动画的速度曲线。默认是 "ease"。linear：动画从头到尾的速度是相同的。ease：默认。动画以低速开始，然后加快，在结束前变慢。ease-in：动画以低速开始。ease-out：动画以低速结束。ease-in-out：动画以低速开始和结束。 |
| animation-fill-mode       | 规定当动画不播放时（当动画完成时，或当动画有一个延迟未开始播放时），要应用到元素的样式(不设置)。 |
| animation-delay           | 规定动画何时开始。默认是 0。定义动画开始前等待的时间，以秒或毫秒计。 |
| animation-iteration-count | 规定动画被播放的次数。默认是 1。n：一个数字，定义应该播放多少次动画。infinite    指定动画应该播放无限次（永远） |
| animation-direction       | 规定动画是否在下一周期逆向地播放。默认是 "normal"。normal    默认值。动画按正常播放。reverse    动画反向播放。    **alternate**    **动画在奇数次（1、3、5...）正向播放，在偶数次（2、4、6...）反向播放。**    alternate-reverse    动画在奇数次（1、3、5...）反向播放，在偶数次（2、4、6...）正向播放。 |
| animation-play-state      | 规定动画是否正在运行或暂停。默认是 "running"。               |

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .abb{
            width: 300px;
            height: 300px;
            background-color: #875;
            position: relative;
            animation:abb 4s;
        }
        @keyframes abb {
            0%{
                background-color: #789;
                left: 0px;
                top: 0px;
            }
            25%{
                background-color: #665;
                left: 20px;
                top: 20px;
            }
            50%{
                background-color: #330;
                left: 40px;
                top: 40px;
            }
            100%{
                background-color: #907;
                left: 60px;
                top: 60px;
            }
        }
    </style>
</head>
<body>
    <div class="abb">

    </div>
</body>
</html>
```





## flex属性（弹性）

#### 容器属性：

**flex-direction**：调整主轴方向

**flex-wrap**：换行

**flex-flow**

**justify-content**

**align-items**

**align-content**



### flex-direction属性

决定主轴的方向（项目排列方向）

它可能有4个值。

**row**（默认值）：主轴为水平方向，起点在左端。

**row-reverse**：主轴为水平方向，起点在右端。

**column**：主轴为垂直方向，起点在上沿。

**column-reverse**：主轴为垂直方向，起点在下沿。

![image-20250312163127890](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250312163127890.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        *{
            padding: 0;
            margin: 0;
        }
        .class{
            width: 100vw;
            height: 100vh;
            background-color: #8b8787;
            /* flex布局 */
            display: flex;
            /* 调整主轴方向 */
            flex-direction: row;
            /* 调整换行 */
            flex-wrap: wrap;
            justify-content: center;
            align-items: center;
        }
        .abb{
            width: 200px;
            height: 200px;
            border: 2px solid #903;
            /* flex: 1; */
            /* margin: 30px; */
        }
        .abb1{
            background-color: #288;
        }
        /* .abb2{
            background-color: #933;
        }
        .abb3{
            background-color: #561;
        } */
    </style>
</head>
<body>
    <div class="class">
        <div class="abb abb1">1</div>
        <!-- <div class="abb abb1">2</div>
        <div class="abb abb3">3</div> -->
    </div>
</body>
</html>
```





### flex-wrap属性

默认情况下，项目都排在一条线（又称"轴线"）上。flex-wrap属性定义，如果一条轴线排不下，如何换行。

![image-20250314082418383](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250314082418383.png)

（1）nowrap（默认）：不换行。

![img](C:\Users\32473\Desktop\4. CSS高级01\4. CSS高级\3_CSS高级_image\wps15.jpg)

（2）wrap：换行，第一行在上方。

![img](C:\Users\32473\Desktop\4. CSS高级01\4. CSS高级\3_CSS高级_image\wps16.jpg)

（3）wrap-reverse：换行，第一行在下方。

![image-20250314082504526](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250314082504526.png)





### flex-flow

flex-flow属性是flex-direction属性和flex-wrap属性的简写形式，默认值为row nowrap。

.box {  flex-flow: flex-direction || flex-wrap;}



### justify-content属性

justify-content属性定义了项目在**主轴**上的对齐方式。

![image-20250314082935397](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250314082935397.png)

flex-start（默认值）：左对齐

flex-end：右对齐

center： 居中

space-between：两端对齐，项目之间的间隔都相等。

space-around：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。





### align-items属性

align-items属性定义项目在**交叉轴**上如何对齐。

.box {  align-items: flex-start | flex-end | center | baseline | stretch;}

![img](C:\Users\32473\Desktop\4. CSS高级01\4. CSS高级\3_CSS高级_image\wps19.jpg)

它可能取5个值。具体的对齐方式与交叉轴的方向有关，下面假设交叉轴从上到下。

flex-start：交叉轴的起点对齐。

flex-end：交叉轴的终点对齐。

center：交叉轴的中点对齐。

baseline: 项目的第一行文字的基线对齐。

stretch（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。





### align-content属性

align-content属性定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用。

.box {  align-content: flex-start | flex-end | center | space-between | space-around | stretch;}

![img](C:\Users\32473\Desktop\4. CSS高级01\4. CSS高级\3_CSS高级_image\wps20.jpg)

该属性可能取6个值。

flex-start：与交叉轴的起点对齐。

flex-end：与交叉轴的终点对齐。

center：与交叉轴的中点对齐。

space-between：与交叉轴两端对齐，轴线之间的间隔平均分布。

space-around：每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。

stretch（默认值）：轴线占满整个交叉轴。





## 项目样式属性

以下6个属性设置在项目上。

order

flex-grow

flex-shrink

flex-basis

Flex

align-self



### order属性

order属性定义项目的排列顺序。数值越小，排列越靠前，默认为0。

.item {  order: integer;}

![img](C:\Users\32473\Desktop\4. CSS高级01\4. CSS高级\3_CSS高级_image\wps21.jpg)





### flex-grow属性

flex-grow属性定义项目的放大比例，默认为0，即如果存在剩余空间，也不放大。

.item {  flex-grow: number; /* default 0 */}

![img](C:\Users\32473\Desktop\4. CSS高级01\4. CSS高级\3_CSS高级_image\wps22.jpg)

如果所有项目的flex-grow属性都为1，则它们将等分剩余空间（如果有的话）。如果一个项目的flex-grow属性为2，其他项目都为1，则前者占据的剩余空间将比其他项多一倍。





### flex-shrink属性

flex-shrink属性定义了项目的缩小比例，默认为1，即如果空间不足，该项目将缩小。

.item {  flex-shrink: number; /* default 1 */}

![img](C:\Users\32473\Desktop\4. CSS高级01\4. CSS高级\3_CSS高级_image\wps23.jpg)

如果所有项目的flex-shrink属性都为1，当空间不足时，都将等比例缩小。如果一个项目的flex-shrink属性为0，其他项目都为1，则空间不足时，前者不缩小。

负值对该属性无效。



### flex-basis属性

flex-basis属性定义了在分配多余空间之前，项目占据的主轴空间（main size）。浏览器根据这个属性，计算主轴是否有多余空间。它的默认值为auto，即项目的本来大小。

.item {  flex-basis: length | auto; /* default auto */}

它可以设为跟width或height属性一样的值（比如350px），则项目将占据固定空间。





### align-self属性

align-self属性允许单个项目有与其他项目不一样的对齐方式，可覆盖align-items属性。默认值为auto，表示继承父元素的align-items属性，如果没有父元素，则等同于stretch。

.item {  align-self: auto | flex-start | flex-end | center | baseline | stretch;}

![img](C:\Users\32473\Desktop\4. CSS高级01\4. CSS高级\3_CSS高级_image\wps24.jpg)

该属性可能取6个值，除了auto，其他都与align-items属性完全一致。  





## 其他样式

### box-sizing

**`box-sizing`** 属性定义了应该如何计算一个元素的总宽度和总高度。





## 透明度设定

IE9, Firefox, Chrome, Opera 和 Safari 使用属性 opacity 来设定透明度。

opacity 属性能够设置的值从 0.0 到 1.0。值越小，越透明。

opacity与通过rgba()设定透明度的区别：

前者同时作用于元素及其标签内容，后者只是作用于元素本身
