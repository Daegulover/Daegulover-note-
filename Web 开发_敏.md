# Web 开发 ‼️

[TOC]

## 开发工具

### 大前端

* 网页

* 小程序

* 数据可视化

* 服务器

* 客户端

### 应用软件

* **C / S 架构**：

客户端服务器

可安装 可不安装的

利弊：需要安装/偶尔更新/不跨平台

​			但是大型专业应用，安全性要求较高的应用需要采用

* **B / S 架构**：  需要打开网站的

浏览器服务器

利弊：无需安装/无需更新/可跨平台

### 浏览器

* 五大主流浏览器

​		chrome	Safari	IE	Firefox	Opera

* 浏览器的内核

  内核是浏览器的核心，用于处理浏览器所得到的各种资源

  服务器 ---代码--->浏览器（处理）----->页面

* 五大浏览器 四大内核

 	 chrome ：早期使用 webkit 内核，现在用 Blink 内核
 	
 	Safari ：使用webkit 内核

​		IE：使用 Trident内核

​		Firefox：使用 Gecko 内核

​		Opera ：早期使用Presto内核（已放弃） ，现在使用 Blink 内核

### VS Code

**Visual Studio Code**（简称 **VS Code**）是一款由[微软](https://zh.wikipedia.org/wiki/微软)开发且跨平台的[免费](https://zh.wikipedia.org/wiki/免費軟體)[源代码编辑器](https://zh.wikipedia.org/wiki/集成开发环境)[[7\]](https://zh.wikipedia.org/wiki/Visual_S						l0pp0 tudio_Code#cite_note-TechCrunch-7)。该软件以扩展的方式支持[语法高亮](https://zh.wikipedia.org/wiki/語法高亮)、代码自动补全（又称 [IntelliSense](https://zh.wikipedia.org/w/index.php?title=IntelliSense&action=edit&redlink=1)）、[代码重构](https://zh.wikipedia.org/wiki/代码重构)功能，并且内置了[命令行](https://zh.wikipedia.org/wiki/命令行)工具和 [Git](https://zh.wikipedia.org/wiki/Git) 版本控制系统[[8\]](https://zh.wikipedia.org/wiki/Visual_Studio_Code#cite_note-8)。用户可以更改主题和键盘快捷方式实现个性化设置，也可以通过内置的[扩展程序](https://zh.wikipedia.org/wiki/插件)商店安装其他扩展以拓展软件功能。



#### 常用开发插件&设置

- 软件汉化插件：Chinese
- 打开网页插件：Open in browser
- 实时刷新插件：Live server
- 彩色缩进插件：Indent-rainbow
- 英语翻译插件：Code translate
- 格式化程序设置：Format on save
- 自动同步修改标签插件：Auto Rename Tag







## HTML

### 常用标签



#### 无语义布局标签

作用：布局网页，划分网页区域，摆放内容

- `div` :独占一行，大盒子
- `span` :不换行，小盒子

> 两个标签都是双标签，其中包裹的内容可以是任何内容



####  语义化标签

简单来说

头部用 **header**

页脚用 **footer**

导航用 **nav**

侧边栏用 **aside**

独立成段类似文章 帖子 评论用 **article**

文章中的各个次级段落用 **section**

解释一下 一个**article**中有多个**section**，甚至由**section**组成

**section**强调分段或分块或分成自然段

**article**比section**更加强调独立性**，一块内容是独立的、完整的，应当使用**article**

***大概article是文章 section是章节***



| **标签名称**   | **用途描述**                                         | **示例用法**                                                 | **优点/特点**                                        |
| -------------- | ---------------------------------------------------- | ------------------------------------------------------------ | ---------------------------------------------------- |
| `<header>`     | 定义文档或节的页眉，通常包含标题、导航等。           | ```html<br><header><h1>网站标题</h1><nav>导航链接</nav></header>``` | 提高页面结构清晰度，增强SEO和可访问性。              |
| `<footer>`     | 定义文档或节的页脚，通常包含版权信息、联系方式等。   | ```html<br><footer>© 2025 公司名称</footer>```               | 明确页面底部内容，便于屏幕阅读器解析。               |
| `<nav>`        | 定义导航链接部分，如主导航菜单。                     | ```html<br><nav><a href="#home">首页</a></nav>```            | 标识核心导航区域，提升用户体验和SEO。                |
| `<section>`    | 定义文档中的独立区域，通常带有标题。                 | ```html<br><section><h2>章节标题</h2><p>章节内容</p></section>``` | 结构化内容分段，便于组织和样式设计。                 |
| `<article>`    | 定义独立、完整的内容块（如博客文章、新闻）。         | ```html<br><article><h2>文章标题</h2><p>文章内容</p></article>``` | 独立内容模块化，利于内容重用和SEO优化。              |
| `<aside>`      | 定义与主内容相关但不直接关联的辅助内容（如侧边栏）。 | ```html<br><aside><h3>相关链接</h3><ul>链接列表</ul></aside>``` | 区分主次内容，提升页面可读性和可访问性。             |
| `<main>`       | 定义文档的主要内容区域（页面只能有一个）。           | ```html<br><main><article>核心内容</article></main>```       | 标识核心内容，便于屏幕阅读器和搜索引擎快速定位重点。 |
| `<figure>`     | 定义独立的流内容（如图片、图表、代码片段）。         | ```html<br><figure><img src="image.jpg"><figcaption>图片说明</figcaption></figure>``` | 将视觉元素与其描述绑定，提升内容的语义化。           |
| `<figcaption>` | 为`<figure>`元素提供标题或描述。                     | ```html<br><figcaption>图1: 示例图片</figcaption>```         | 增强`<figure>`内容的可访问性和上下文信息。           |
| `<mark>`       | 高亮显示文本内容（默认黄色背景）。                   | ```html<br><mark>关键词</mark>```                            | 突出显示重要信息，适用于搜索结果高亮。               |
| `<time>`       | 定义日期或时间（通过`datetime`属性机器可读）。       | ```html<br><time datetime="2025-05-09">2025年5月9日</time>``` | 提供结构化的日期时间数据，便于机器解析。             |
| `<details>`    | 定义可折叠的用户可切换内容块（如FAQ）。              | ```html<br><details><summary>点击展开</summary>详细内容</details>``` | 实现交互式内容折叠，减少页面冗余。                   |
| `<summary>`    | 为`<details>`元素提供标题或摘要。                    | ```html<br><summary>标题</summary>```                        | 与`<details>`配合使用，提升用户交互体验。            |
| `<dialog>`     | 定义对话框或模态窗口（如弹窗）。                     | ```html<br><dialog open>这是一个对话框</dialog>```           | 简化对话框实现，支持原生交互功能。                   |
| `<progress>`   | 表示任务的进度（如文件上传进度）。                   | ```html<br><progress value="70" max="100">70%</progress>```  | 可视化进度状态，提升用户反馈体验。                   |
| `<meter>`      | 表示标量值或分数（如磁盘使用率）。                   | ```html<br><meter value="0.6" min="0" max="1">60%</meter>``` | 直观展示数值范围，适用于数据可视化场景。             |



#### 图像标签

作用：在网页中插入图片

标签名：`<img src = "图片的URL">`

**`src 属性`**  用于指定图像的位置和名称，是  **`<img>`**  的必须属性

> 图片与代码文件放至同一文件夹即可使用 `./` 命令快捷添加，这种方法是 `相对路径`

**常见属性表**

| 属性   | 作用       | 说明                               |
| ------ | ---------- | ---------------------------------- |
| alt    | 替换文本   | 图片无法显示的时候显示的文字       |
| title  | 提示文本   | 鼠标悬停在图片上面的时候现实的文字 |
| width  | 图片的宽度 | 值为数字，没有单位                 |
| height | 图片的高度 | 值为数字，没有单位                 |

> img标签 中的 alt属性 适用于可能加载失败，进行解释并提示
>
> 分别使用 width属性 与 height属性 浏览器默认是***等比缩放***



#### 音频标签

标签名：`<audio src="音频的URL"></audio>`

**常见属性表**

| 属性                | 作用             | 特殊说明                 |
| ------------------- | ---------------- | ------------------------ |
| **src（必须属性）** | 音频URL          | 支持格式：MP3、Ogg、Wav  |
| controls            | 显示音频控制面板 |                          |
| loop                | 循环播放         |                          |
| autoplay            | 自动播放         | 浏览器一般会禁用自动播放 |

> 在HTML5中，如果属性名与属性值完全一样，则可简写为一个单词



#### 视频标签

标签名：`<video src="视频的URL"></video>`

**常见属性表**

| 属性                | 作用             | 特殊说明                         |
| ------------------- | ---------------- | -------------------------------- |
| **src（必须属性）** | 视频URL          | 支持格式：MP4、WebM、Ogg         |
| controls            | 显示视频控制面板 |                                  |
| loop                | 循环播放         |                                  |
| muted               | 静音播放         |                                  |
| autoplay            | 自动播放         | 浏览器支持在**静音状态**自动播放 |

> 在HTML5中，如果属性名与属性值完全一样，则可简写为一个单词



#### 超链接标签

作用：点击跳转到其他页面

标签名：**`<a href="链接">显示文字</a>`**

`target` 属性赋值 `"_blank"` 可实现新窗口跳转页面

`target` 属性赋值 `"_self"` 可实现当前窗口跳转页面，不用写，默认就是在当前窗口跳转页面

例如：`<a href="https://lufangqian.top" target="_blank">陆方七安的导航</a>`

本示例意为在新窗口打开指向`lufangqian.top`网站的名叫陆方七安的导航的超链接

> 开发初期，不知道超链接的跳转地址，href属性值写#，表示空链接，不会跳转,  可以回到顶部
>
> 如果 href 属性值是空的 ， 表示 刷新页面
>
> 如果 href 属性值是  javascript : js的内容 ;  ， 可以进行进行 js 的操作 
>
> 
>
> 在代码中，敲不管多少的空格，都只显示一个空格
>
> a 标签内，不准再写 a 标签



##### 锚点链接

a标签还可以跳转到特定位置，可以给要跳转到的位置的标签添加一个id，在a标签中给hef的值设置为#id名

```html
<a href="#top">返回顶部</a>

<!-- 在页面的顶部放置一个id为top的元素 -->
<div id="top"></div>
```

去除超链接默认样式

```css
a {
    color: inherit; /* 使用父元素的颜色 */
    text-decoration: none;
}
```

##### 跳转锚点

```html
<!-- 跳转到test1锚点 -->
<a href="#test1">去test1锚点</a>

<!-- 跳到本页面顶部 -->
<a href="#">回到顶部</a>

<!-- 跳转到其他页面锚点 -->
<a href="demo.html#test1">去demo.html页面的test1锚点</a>

<!-- 刷新本页面 -->
<a href="">刷新本页面</a>

<!-- 执行一段js, 如果还不知道执行什么，可以留空，javascript:; -->
<a href="javascript:alert(1);">点我弹窗</a>
```



##### 清楚默认样式

✅ 1. 去除下划线（最常见）

css

深色版本



```
a {
    text-decoration: none; /* 关键：去除下划线 */
}
```

------

✅ 2. 重置颜色

浏览器默认给链接设置颜色（如蓝色、访问后变紫色），可以统一设置：

css

深色版本



```
a {
    color: black;           /* 设置你想要的颜色 */
    color: inherit;         /* 或继承父元素颜色 */
}
```

------

✅ 3. 清除所有状态的默认样式（推荐）

链接有多种状态：未访问、已访问、悬停、点击中。建议统一控制：

css

深色版本



```
a {
    text-decoration: none;  /* 去掉下划线 */
    color: inherit;         /* 颜色继承父元素 */
    outline: none;          /* 去掉点击时的轮廓（谨慎使用） */
    /* outline: none 可能影响可访问性，建议保留或自定义 */
}

/* 可选：自定义悬停效果 */
a:hover {
    text-decoration: none;
    color: #007acc;
    /* 可加其他效果，如背景色 */
}
```

------

✅ 4. 完整“清除样式”示例

css

深色版本



```
a,
a:link,
a:visited,
a:hover,
a:active,
a:focus {
    text-decoration: none;
    color: inherit;
    outline: none;
    border: none;
    background: none;
}
```

> ⚠️ 注意：
>
> - `outline: none` 会移除键盘导航的焦点框，**影响无障碍访问**，不建议完全移除。
> - 更好的做法是自定义 `:focus` 样式：

css

深色版本



```
a:focus {
    outline: 2px solid #007acc;
    outline-offset: 2px;
}
```

------

✅ 5. 如果用于按钮或菜单中的链接

css

深色版本



```
.nav-link {
    text-decoration: none;
    color: white;
    padding: 10px 15px;
    display: inline-block;
}

.nav-link:hover {
    background-color: #007acc;
    border-radius: 4px;
}
```

------

✅ 总结：最常用写法

css

深色版本



```
a {
    text-decoration: none;
    color: inherit;
}

a:hover {
    text-decoration: none; /* 防止某些浏览器恢复下划线 */
}
```

------

🚫 不推荐的做法

- 使用 `underline` 或奇怪颜色不处理
- 完全移除 `outline` 而不提供替代焦点样式（对残障用户不友好）

------

✅ **最佳实践**：
 清除默认样式是为了美观，但要保留**可访问性**和**用户体验**。建议：

- 去掉下划线 ✅
- 统一颜色 ✅
- 自定义 `:hover` 和 `:focus` 效果 ✅





#### 全局标签属性

| 属性名 | 含义                                                         |
| ------ | ------------------------------------------------------------ |
| id     | 给标签指定唯一标识，注意：id 是不能重复的。<br>作用：可以让 label 标签与表单控件相关联；也可以与 CSS、JavaScript 配合使用。<br>注意：不能在以下 HTML 元素中使用：<br>`<head>`、`<html>`、`<meta>`、`<script>`、`<style>`、`<title>`。 |
| class  | 给标签指定类名，随后通过 CSS 就可以给标签设置样式。          |
| style  | 给标签设置 CSS 样式。                                        |
| dir    | 内容的方向，值: ltr、rtl。<br>注意：不能在以下 HTML 元素中使用：<br>`<head>`、`<html>`、`<meta>`、`<script>`、`<style>`、`<title>`。 |
| title  | 给标签设置一个文字提示，一般超链接和图片用得比较多。         |
| lang   | 给标签指定语言，具体规范和可选值请参考【10. HTML 设置语言】。<br>注意：不能在以下 HTML 元素中使用：<br>`<head>`、`<html>`、`<meta>`、`<script>`、`<style>`、`<title>`。 |

标签属性的作用是给标签提供一些附加信息

**注意！！！！！！！！！！重复写同一个属性，后写的属性将覆盖前面的同一属性**

每个标签都有属性 常见的为 class 与 id，经常被用在设置css样式与js行为中



还有三个较为常见且大部分标签皆可使用的属性

**title**(鼠标悬浮文字提示)    **lang**(给指定标签设置语言)   **dir**(内容显示方向，值为**ltr rtl**)



有一些标签有其特殊的属性

例如资源引用相关

- `src`

  （Source）：指定外部资源的路径，用于加载图片、脚本、视频等。

  - 用途：浏览器会直接加载该资源。
  - 示例：`<img src="image.jpg">`、`<script src="script.js"></script>`

- `href`

  （Hypertext Reference）：指定超链接的目标地址。

  - 用途：点击后跳转到其他页面或资源。
  - 示例：`<a href="https://example.com">点击访问</a>`

表单元素相关（如 `<input>`、`<textarea>`）常用属性：

- - **`name`**：提交表单时字段的名称（服务器端用于接收数据）。
  - **`value`**：输入框的默认值或用户输入的内容。
  - **`placeholder`**：输入框的提示文字（未输入时显示）。
  - **`required`**：表示该字段为必填项。



#### 标题标签

一般用于新闻标题、文章标题、网页区域名称、产品名称等等

标签名：`h1 ~ h6`

> 由大到小，h1标题为主标题，标题等级随着数字增大而减小

**注意事项**

- h1 标签在一个网页中建议只使用一次，用来放新闻标题或者网站的logo
- h2 ~ h6 没有使用次数的限制

> 以上两点为规范要求，并非语法要求，如要重复使用，也没啥事

注意，**标题标签之间不可嵌套**



#### 段落标签

一般用在新闻段落、文章段落、产品描述信息等等

标签名：**`p`**

段落标签内的文字会自动换行



#### 换行与水平线标签

换行： `<br>`

浏览器不识别代码中的Enter换行

水平线：`<hr>`

| 属性名 | 含义     | 属性值                               |
| ------ | -------- | ------------------------------------ |
| align  | 对齐方式 | 可选择 left right center ,默认center |
| size   | 粗细     | px，默认为2                          |
| color  | 颜色     | 颜色                                 |
| width  | 宽度     | 可以是确定的px，也可以是百分比数值   |

> 此标签为单标签



#### 文本标签

作用：为文本添加特殊格式，以突出重点

常见的格式有：加粗、倾斜、下划线、删除线

**标签名**

加粗：`<strong>`  or  `<b>`

倾斜：`<em>`  or  `<i>`

下划线： `<ins>`  or  `<u>`

删除线：`<del>`  or  `<s>`

高亮标记：`<mark>被标记内容</mark>`

文本标记：

> 为了代码的可读性，通常使用左侧语义明显的标签，并且本标签允许嵌套



##### 文本注音

标签名: `<ruby>` 与 `<rt>`

```html
<ruby>
  <span>彳亍</span>
  <rt>xing</rt>
</ruby>
```

**注意！一定是内容在上，rt注音标签在下**



#### 框架标签

**作用**  

在当前页面中嵌入另一个 HTML 文档（如网页、视频、地图等），实现内容复用或外部资源整合。

**标签名**  

**`<iframe src="链接" width="像素值" height="像素值"></iframe>`**  

**核心属性**  

| **属性**         | **作用**                                               |
| ---------------- | ------------------------------------------------------ |
| `src`            | 指定嵌入内容的 URL（如 `https://www.toutiao.com`）。   |
| `width`/`height` | 设置框架的尺寸（如 `width="900"` 和 `height="300"`）。 |
| `name`           | 为框架命名，可用于表单提交或链接目标。                 |
| `sandbox`        | 限制框架内容的功能（如禁用脚本、表单提交等）。         |
| `allow`          | 指定允许使用的功能（如摄像头、麦克风）。               |

---

##### 举个栗子

```html
<iframe src="https://www.toutiao.com" width="900" height="300"></iframe>
```

- **效果**：在网页中嵌入头条网站的内容，尺寸为 900x300 像素。

利用 iframe 嵌入一个普通网页

```html
<iframe src="https://www.toutiao.com" width="900" height="300" frameborder="0"></iframe>
```

 利用 iframe 嵌入一个广告

 利用 iframe 嵌入其他内容

与超链接的 target 属性配合使用

```html
<a href="https://www.toutiao.com" target="tt">点我看新闻</a>
<a href="https://www.taobao.com" target="tt">点我看淘宝</a><br>
<iframe name="tt" frameborder="0" width="900" height="300"></iframe>
```

 与表单的 target 属性配合使用

  ```html
<!-- 写表单的target属性配合使用 -->
<form action="https://so.toutiao.com/search" target="container">
    <input type="text" name="keyword">
    <input type="submit" value="搜索">
</form>
  ```



### 列表标签

* 不管什么列表，都要注意结构

作用：布局内容排列整齐的区域

分类：无序、有序、定义列表



#### 无序列表

用的比较多

作用：布局排列整齐的不需要规定顺序的区域

标签名：`<ul>父级 <li>子级`

> ul是无序列表，只能包裹li标签；li是列表条目，可以包裹任何标签

```html
<ul>
    <li>第一项</li>
    <li>第二项</li>
    <li>第三项</li>
    …………
</ul>
```

这是无序列表的一个嵌套 ul --> li --> span --> ul --> li

#### 有序列表

作用：布局排列整齐的需要规定**顺序**的区域

标签名：`<ol>父级 <li>子级`

> ol 是有序列表，只能包裹 li 标签；li 是列表条目，可以**包裹**任何标签
>
> 尽量不要让 li 单独出现 

```html
<ol>
    <li>第一项</li>
    <li>第二项</li>
    <li>第三项</li>
    …………
</ol>
```



#### 定义列表

* 术语名称，对术语的描述 

* 一个术语名称可以有还几个描述

标签名：`<dl>父级 <dt>子级-列表标题 <dd>子级-列表详情`

```html
<dl>
    <dt>列表标题</dt>    //术语名称
    <dd>列表详情</dd>    //对术语的描述
    …………
</dl>
```



### 表格

#### 表格标签

作用：网页中的表格与Excel表格类似，用来展示数据

标签名：`table 嵌套 tr  tr嵌套td/th`

| 标签名  | 说明       |
| ------- | ---------- |
| table   | 表格       |
| caption | 表格标题   |
| tr      | 行         |
| th      | 表头单元格 |
| td      | 内容单元格 |

> 在网页中，表格默认没有边框线，使用 **border** 属性可以添加边框线，若 border 里面的值大于 1 ， 他显示的就只是外边框
>
> 控制表格的宽度 **width**
>
> 控制表格高度 **height** ， 表头 和 脚注 高度不会变
>
> 表格和表格之间的间距 **cellspacing** （并不是没有边框，而是，边框之间的距离为0）
>
> 整个单元格的水平居中 **align**，左对齐 left , 右对齐 right , 居中 center ； align = "left";
>
> 垂直方向对齐 **valign** , 居中 middle ,  底部 bottom , 顶部 top  ; valign = "top";

```html
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
```



#### 表格结构标签

作用：用表格结构标签把内容划分区域，让表格结构更清晰，语义更清晰

> 可以不写

| 标签名     | 含义     | 特殊说明                                                     |
| ---------- | -------- | ------------------------------------------------------------ |
| thead      | 表格头部 | 表格头部内容（只能写 height ，不能写 border,width,cellspacing这些属性） |
| tbody      | 表格主体 | 主要内容区域                                                 |
| tfoot (td) | 表格底部 | 汇总信息区域                                                 |



#### 合并单元格 

作用：将多个单元格合并成一个单元格，以合并同类信息

其中，跨行合并与跨列合并不同

合并时会保留**最左**、**最上**单元格中的内容

属性：

rowspan	跨行

colspan	跨列

- 跨**行**合并，保留最上单元格，添加属性 `rowspan `  rowspan = ''5''
- 跨**列**合并，保留最左单元格，添加属性 `colspan`  colspan = "2";

> 本属性应用于<td>、<th>等子级标签



### 表单

**表单是网页中用于与用户交互、收集信息并提交给服务器处理的结构化区域。**

作用：收集信息

例如：登录页面、注册页面、搜素页面

将多个标签放置在同一表单中，使用 `form` 标签

提交数据需要使用 `form` 标签中的 `action` 属性，属性值为**提交数据的地址** ，表单的网址后面的 s 是 search ，是必须要写的

```html
<form action = "https://www.baidu.com/s">
```



#### 禁用表单控件

```html
<input disabled>
```

最好不要既写 disabled 又写 checked ，又禁用又选用，容易出笑话





#### input标签

input 标签 比较特殊 Type属性值不同，则功能不同>

标签名：

```html
<input type="……" name = "" value= "" maxlenght = "">    //这些都很重要，基本上都要写
```

百度的 name 是 wd

京东的 name 是 keyword

| Type 属性值 | 说明                     |
| ----------- | ------------------------ |
| text        | 文本框，用于输入单行文本 |
| password    | 密码框                   |
| radio       | 单选框                   |
| checkbox    | 多选框 / 复选框          |
| file        | 上传文件                 |



占位文本：提示信息

> 当有多个文本输入框时，占位文本可以提示输入，此属性可用于文本框与密码框

在input标签中添加属性 `placeholder`

```html
<input type="……" placeholder="提示信息">
```

在input标签中添加属性 `onclik`

```html
<input type="……" oncli="提示信息">
```

清除选中时的边框

```css
input:focus {
    outline: none; /* 移除默认的聚焦边框 */
}
```

清除默认边框

```css
input{
    border: none;
    background-color: #F5F5F5;   /*文本框中的背景颜色*/ 
    border-radius: 3px;
}
```



##### 单选框 radio

常用属性：

| 属性名  | 作用     | 特殊说明                                 |
| ------- | -------- | ---------------------------------------- |
| name    | 控件名称 | 控件分组，同组只能选中一个(**单选功能**) |
| checked | 默认选中 | 属性名和属性值相同，简写为一个单词       |

> name属性相同将划分为一组，同组的单选框只能有一个被选中

```html
<input type="radio" name="gender" value="male">男
<input type="radio" name="gender" value="female">女
```





##### 上传文件 file

使用 `multiple` 属性可以实现文件多选



##### 多选框 checkbox

多选框也叫复选框

默认选中：checked

```html
<input type="checkbox" checked>
```



#### 隐藏域

可以简单的防止批量注册

```html
<input type="hidden">
```

再加上   name  value  





#### 下拉菜单

使用例子：用户注册时选择城市时可以使用下拉菜单选择城市

标签名：`select ` 嵌套  `option `,  `select `是下拉菜单的整体，`option`是下拉菜单的每一项

标签名：

```html
<select name="place">
    <option value="北京">北京</option>
    <option value="上海">上海</option>
    <option value="深圳">深圳</option>
    <option value="广州">广州</option>
    <option value="武汉">武汉</option>
    <option value="下北泽" selected>下北泽</option>
</select>
```

> **selected**属性为**默认选项**
>
> 最好在 option 里面写 value 值 , 这样 select 的place 就可以找到



#### 文本域

作用：多行输入文本的表单控件

标签名：`textarea` 双标签

> 提示文字在双标签里，或者使用 placeholder

```html
<texterea name="other" cols="25" rows="10"></texterea>
```

texterea 这个是不可以写 type 这个属性的



#### Label标签

作用：网页中，某个标签的说明文本

​			用于关联文本和表单控件

​			在 input 中，不仅点击 框框 能获取焦点，还要点击前面的文字也可以获取焦点 

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

| Type属性值 | 说明                                                         |
| ---------- | ------------------------------------------------------------ |
| submit     | **提交**按钮，点击后可以提交数据到后台(默认选项)   //不可以写 name 的属性 |
| reset      | **重置**按钮，点击后将表单控件恢复默认值                     |
| button     | **普通**按钮，默认没有功能，一般配合 JavaScript 使用         |

可以在 input 去写，也可以直接用 button 去写



##### 清除按钮默认样式：

使用 CSS 重置属性

这是最直接的方法，通过设置关键的 CSS 属性来清除默认样式。

```css
button {
    /* 清除边框和背景 */
    border: none;
    background: none;
    
    /* 清除内边距和外边距 */
    padding: 0;
    margin: 0;
    
    /* 重置字体样式，使其继承父元素 */
    font: inherit;
    color: inherit;
    
    /* 去除点击时的轮廓（可选，注意可访问性） */
    outline: none;
    
    /* 去除默认的鼠标样式（可选） */
    cursor: pointer;
}
```



#### 逻辑分组控件



##### fieldset 分组

**功能**：将表单中的控件逻辑分组，通过视觉边框（默认样式）增强表单结构的清晰度。

核心属性：

- `disabled`：禁用 `<fieldset>` 内所有子控件。
- `form`：指定所属表单（用于不在 `<form>` 内部的 `<fieldset>`）。
- `name`：为分组命名，便于 JavaScript 操作。

- **适用场景**：适用于需要将相关表单元素（如输入框、单选按钮等）分组展示的场景。



##### legend 标题

- **功能**：为 `<fieldset>` 分组提供标题或描述，提升表单的可读性和可访问性。
- 使用规则：
  - **必须是 `<fieldset>` 的第一个子元素**。
  - 属于 `<fieldset>` 的一部分，不能单独使用。
- **作用**：帮助用户（包括屏幕阅读器用户）快速理解分组内容的用途。

食用方法：

```html
<form>
  <fieldset>
    <legend>个人信息</legend>
    <label for="name">姓名:</label>
    <input type="text" id="name" name="name"><br><br>
    <label for="email">邮箱:</label>
    <input type="email" id="email" name="email">
  </fieldset>
</form>
```



#### 表单总结

| 标签名 | 标签语义 | 常用属性                                                     |
| ------ | -------- | ------------------------------------------------------------ |
| form   | 表单     | action 属性：表单要提交的地址。<br>target 属性：跳转的新地址的打开方式；值：_self、_blank<br>method 属性：请求方式，可选值：get、post |

| input    | 多种形式的表单控件 | type 属性：指定表单控件的类型。<br>可选值：text、password、radio、checkbox、hidden、submit、reset、button 等。<br>name 属性：指定数据名称<br>value 属性：<br>对于输入框：指定默认输入的值；<br>对于单选和复选框：实际提交的数据；<br>对于按钮：显示按钮文字。<br>disabled 属性：设置表单控件不可用。<br>maxlength 属性：用于输入框，设置最大可输入长度。<br>checked 属性：用于单选按钮和复选框，默认选中 |
| -------- | ------------------ | ------------------------------------------------------------ |
| textarea | 文本域             | name 属性：指定数据名称<br>rows 属性：指定默认显示的行数，影响文本域的高度。<br>cols 属性：指定默认显示的列数，影响文本域的宽度。<br>disabled 属性：设置表单控件不可用。 |
| select   | 下拉框             | name 属性：指定数据名称<br>disabled 属性：设置整个下拉框不可用。 |
| option   | 下拉框的选项       | disabled 属性：设置拉下选项不可用。<br>value 属性：该选项事件提交的数据（不指定 value，会把标签中的内容作为提交数据）<br>selected 属性：默认选中。 |
| button   | 按钮               | disabled 属性：设置按钮不可用。<br>type 属性：设置按钮的类型，值：submit（默认）、reset、button |
| label    | 与表单控件做关联   | for 属性：值与要关联的表单控件的ID值相同。                   |
| fieldset | 表单控件分组       | -                                                            |
| legend   | 分组名称           | -                                                            |



### 字符实体

作用：在网页中显示预留字符



| **实体名称** | **实体编号** | **字符** | **说明**                       |
| ------------ | ------------ | -------- | ------------------------------ |
| `&amp;`      | `&#38;`      | `&`      | 和号（必须转义的字符）         |
| `&lt;`       | `&#60;`      | `<`      | 小于号（HTML 标签的开始符号）  |
| `&gt;`       | `&#62;`      | `>`      | 大于号（HTML 标签的结束符号）  |
| `&quot;`     | `&#34;`      | `"`      | 双引号（属性值分隔符）         |
| `&apos;`     | `&#39;`      | `'`      | 单引号（HTML5 支持）           |
| `&nbsp;`     | `&#160;`     | ` `      | 非间断空格（多个连续空格显示） |
| `&copy;`     | `&#169;`     | `©`      | 版权符号                       |
| `&reg;`      | `&#174;`     | `®`      | 注册商标符号                   |
| `&trade;`    | `&#8482;`    | `™`      | 商标符号                       |
| `&euro;`     | `&#8364;`    | `€`      | 欧元符号                       |
| `&yen;`      | `&#165;`     | `¥`      | 日元符号                       |
| `&pound;`    | `&#163;`     | `£`      | 英镑符号                       |
| `&deg;`      | `&#176;`     | `°`      | 度数符号（如 30°C）            |
| `&times;`    | `&#215;`     | `×`      | 乘号                           |
| `&divide;`   | `&#247;`     | `÷`      | 除号                           |
| `&ndash;`    | `&#8211;`    | `–`      | 短破折号（en dash）            |
| `&mdash;`    | `&#8212;`    | `—`      | 长破折号（em dash）            |
| `&hellip;`   | `&#8230;`    | `…`      | 省略号（三个点）               |
| `&laquo;`    | `&#171;`     | `«`      | 左引号（法语等语言）           |
| `&raquo;`    | `&#187;`     | `»`      | 右引号（法语等语言）           |
| `&lsquo;`    | `&#8216;`    | `‘`      | 左单引号                       |
| `&rsquo;`    | `&#8217;`    | `’`      | 右单引号                       |
| `&ldquo;`    | `&#8220;`    | `“`      | 左双引号                       |
| `&rdquo;`    | `&#8221;`    | `”`      | 右双引号                       |



### 注释

HTML的注释方式为  **`<!--内容-->`**

VS Code 中，添加/删除注释的快捷键是 **`Ctrl + /`**

注释的里面内容就不能再写注释了，注释不可以嵌套

也可以临时让某一行或某一段代码注释掉



### 路径

定义：路径指的是查找文件时，从起点到终点经历的路线

分类：

- 相对路径：从当前文件位置出发查找目标文件
- 绝对路径：从盘符出发查找目标文件

#### 相对路径

从当前文件位置出发查找目标文件

- **`/`** 表示进入某个文件夹里面 ，下一级
- **`.`** 表示当前文件所在文件夹
- **`./`** 为当前目录   **`../`**为上一级路径   **`../../`**为上上一级路径  以此类推

#### 绝对路径 

从 根目录 出发 ，C 盘 / D盘 / E盘

* 本地绝对路径
  * 从 盘符 出发 " C : / 打开的文件夹 / xxx.jpg "
  * 用的特别少

* 网络绝对路径

  * http / https 开头

  * 注意：网址不可以写错
  * 若服务器开启了防盗链，会造成如片引入失败



Windows电脑从 盘符 出发

Mac电脑从根 目录(/) 出发



### meta元信息

**配制字符编码**

```html
<meta charset="UTF-8">
```

**针对IE浏览器的一个兼容性设置**

```html
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

**针对移动端的一个配置**

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

**配置网页关键字**

```html
<meta name="keywords" content="8-12个以英文逗号隔开的单词/词语">
```

**配置网页描述信息**

```html
<meta name="description" content="80字以内的一段话，与网站内容相关">
```

**针对搜索引擎爬虫配置**：

```html
<meta name="robots" content="此处可选值见下表">
```

**配置选项表**

| 值        | 描述                               |
| --------- | ---------------------------------- |
| index     | 允许搜索爬虫索引此页面。           |
| noindex   | 要求搜索爬虫不索引此页面。         |
| follow    | 允许搜索爬虫跟随此页面上的链接。   |
| nofollow  | 要求搜索爬虫不跟随此页面上的链接。 |
| all       | 与 index, follow 等价              |
| none      | 与 noindex, nofollow 等价          |
| noarchive | 要求搜索引擎不缓存页面内容。       |
| nocache   | noarchive 的替代名称。             |

**自动刷新**

```html
<meta http-equiv="refresh" content="3">   //原地刷新
```

```html
<meta http-equiv="refresh" content="10;url=http://www.baidu.com">
```





## H5

### 简介

#### 1. 什么是HTML5？

- HTML5 是新一代的 HTML 标准，2014年10月由万维网联盟（W3C）完成标准制定。
- 官网地址：
  - W3C 提供：https://www.w3.org/TR/html/index.html
  - WHATWG 提供：https://whatwg-cn.github.io/html/multipage
- HTML5 在狭义上是指新一代的 HTML 标准，在广义上是指：整个前端。 

#### 2. HTML5 优势

1. 针对 JavaScript，新增了很多可操作的接口。
2. 新增了一些语义化标签、全局属性。
3. 新增了多媒体标签，可以很好地替代 flash。
4. 更加侧重语义化，对于 SEO 更友好。
5. 可移植性好，可以大量应用在移动设备上。

#### 3. HTML5兼容性

- 支持：Chrome、Safari、Opera、Firefox 等主流浏览器。
- IE 浏览器必须是 9 及以上版本才支持 HTML5，且 IE9 仅支持部分 HTML5 新特性。

这段内容说明了HTML5在不同浏览器中的兼容性情况，特别是对Internet Explorer（IE）浏览器的版本要求和限制。



### H5新增语义化标签

**优点**：  

- 提升 SEO（搜索引擎友好）  
- 提高可访问性（屏幕阅读器可识别）  
- 代码结构清晰，便于团队协作和维护

#### 新增布局标签 

| 标签名  | 语义                                                         | 单/双标签 |
| ------- | ------------------------------------------------------------ | --------- |
| header  | 整个页面，或部分区域的头部                                   | 双        |
| footer  | 整个页面，或部分区域的底部                                   | 双        |
| nav     | 导航                                                         | 双        |
| article | 文章、帖子、杂志、新闻、博客、评论等。                       | 双        |
| section | 页面中的某段文字，或文章中的某段文字（里面文字通常里面会包含标题）。 | 双        |
| aside   | 侧边栏                                                       | 双        |
| main    | 文档的主要内容 (WHATWG 没有语义，IE 不支持)，几乎不用。      | 双        |
| hgroup  | 包裹连续的标题，如文章主标题、副标题的组合（W3C 将其删除）   | 双        |

**关于 `article` 和 `section`：**

* `article` 里面可以有多个 `section`。
* `section` 强调的是分段或分块，如果你想将一块内容分成几段的时候，可使用 `section` 元素。
* article` 比 `section` 更强调独立性，一块内容如果比较独立、比较完整，应该使用 `article` 元素。



#### 新增状态标签

**手机电量**	**meter标签**

max 最大；min 最小；value 现在； low 最低； high 最高； optimum 最适（会出现颜色变化）

```html
<meter max="100" min="0" value="10" low="20" high="80" optimum="90"></meter>
```

![image-20250906172200538](./笔记/笔记/web-img/image-20250906172200538.png)

**当前进度**	**progress标签**

```html
<progress max="100" value="40"></progress>
```

![image-20250906172239618](./笔记/笔记/web-img/image-20250906172239618.png)



#### 新增列表标签

| 标签名   | 语义                                        | 单/双标签 |
| -------- | ------------------------------------------- | --------- |
| datalist | 用于搜索框的关键字提示                      | 双        |
| details  | 用于展示问题和答案，或对专有名词进行解释    | 双        |
| summary  | 写在 details 的里面，用于指定问题或专有名词 | 双        |

```html
<input type="text" list="mydata">
<datalist id="mydata">
    <option value="周冬雨">周冬雨</option>
    <option value="周杰伦">周杰伦</option>
    <option value="温兆伦">温兆伦</option>
    <option value="马冬梅">马冬梅</option>
</datalist>

<details>
    <summary>如何走上人生巅峰？</summary>
    <p>一步一步走呗</p>
</details>
```

#### 新增文本标签

##### 4.1 文本注音

| 标签名 | 语义                            | 单/双标签 |
| ------ | ------------------------------- | --------- |
| ruby   | 包裹需要注音的文字              | 双        |
| rt     | 写注音，rt 标签写在 ruby 的里面 | 双        |

```html
<ruby>
    <span>魑魅魍魉</span>
    <rt>chī mèi wǎng liǎng </rt>
</ruby>
```

##### 4.2 文本标记

| 标签名 | 语义 | 单/双标签 |
| ------ | ---- | --------- |
| mark   | 标记 | 双        |

注意：W3C 建议 mark 用于标记搜索结果中的关键字。

#### 新增的表单控件属性

| 属性名       | 功能                                                         |
| ------------ | ------------------------------------------------------------ |
| placeholder  | 提示文字（注意：不是默认值，value 是默认值），适用于文字输入类的表单控件。 |
| required     | 表示该输入项**必填**，适用于除按钮外其他表单控件。           |
| autofocus    | 自动获取焦点，适用于所有表单控件。                           |
| autocomplete | 自动完成，可以设置为 on 或 off，适用于文字输入类的表单控件。<br>注意：密码输入框、多行输入框不可用。 |
| pattern      | 填写正则表达式，适用于文本输入类表单控件。<br>注意：多行输入不可用，且空的输入框不会验证，往往与 required 配合。 |

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <form action="">
        账号：<input type="text" name="account" placeholder="请输入账号" required autofocus autocomplete="on" pattern="\w{6}">
        <br>
        密码：<input type="password" name="pwd" placeholder="请输入密码" required pattern="\w{6}">
        <br>
        性别：
        <input type="radio" value="male" name="gender" required>男
        <input type="radio" value="female" name="gender" required>女
        <br>
        <button>提交</button>
    </form>
</body>

</html>
```

#### input新增的type属性值

```html
    <form action="">
        邮箱：<input type="email">
        url: <input type="url" name="url">
        num: <input type="number" name="num" step="2" max="10" min="0">
        search: <input type="search" name="keyword">
        电话: <input type="tel" name="phone"> <!-- 在手机端可以-->
        光照强度： <input type="range" name="range" max="100" min="0" value="0">
        颜色： <input type="color" name="color">
        日期： <input type="date" name="date">
        月份：<input type="month" name="month">
        周：<input type="week" name="week">
        时间: <input type="time" name="time">
        日期+时间： <input type="datetime-local" name="time2">

        <br>
        <button>提交</button>
    </form>
```

#### 新增视频标签

标签名：`<video src="视频的URL"></video>`

###### 常见属性表

| 属性     | 值                     | 描述                                                         |
| -------- | ---------------------- | ------------------------------------------------------------ |
| src      | URL地址                | 视频地址                                                     |
| width    | 像素值                 | 设置视频播放器的宽度                                         |
| height   | 像素值                 | 设置视频播放器的高度                                         |
| controls | -                      | 向用户显示视频控件（比如播放/暂停按钮）                      |
| muted    | -                      | 视频静音                                                     |
| autoplay | -                      | 视频自动播放                                                 |
| loop     | -                      | 循环播放                                                     |
| poster   | URL地址                | 视频封面                                                     |
| preload  | auto / metadata / none | 视频预加载，如果使用 autoplay，则忽略该属性。<br>• none: 不预加载视频。<br>• metadata: 仅预先获取视频的元数据（例如长度）。<br>• auto: 下载整个视频文件，即使用户不希望使用它。 |

> 在HTML5中，如果属性名与属性值完全一样，则可简写为一个单词

#### 新增音频标签

标签名：`<audio src="音频的URL"></audio>`

###### 常见属性表

| 属性     | 值                     | 描述                                                         |
| -------- | ---------------------- | ------------------------------------------------------------ |
| src      | URL地址                | 音频地址                                                     |
| controls | -                      | 向用户显示音频控件（比如播放/暂停按钮）                      |
| autoplay | -                      | 音频自动播放                                                 |
| muted    | -                      | 音频静音                                                     |
| loop     | -                      | 循环播放                                                     |
| preload  | auto / metadata / none | 音频预加载，如果使用 autoplay，则忽略该属性。<br>• none: 不预加载音频。<br>• metadata: 仅预先获取音频的元数据（例如长度）。<br>• auto: 可以下载整个音频文件，即使用户不希望使用它。 |

> 在HTML5中，如果属性名与属性值完全一样，则可简写为一个单词

#### 新增全局属性

| 属性名          | 功能                                                         |
| --------------- | ------------------------------------------------------------ |
| contenteditable | 表示元素是否可被用户编辑，可选值如下：<br>• true : 可编辑<br>• false : 不可编辑 |
| draggable       | 表示元素可以被拖动，可选值如下：<br>• true : 可拖动<br>• false : 不可拖动 |
| hidden          | 隐藏元素                                                     |
| spellcheck      | 规定是否对元素进行拼写和语法检查，可选值如下：<br>• true : 检查<br>• false : 不检查 |
| contextmenu     | 规定元素的上下文菜单，在用户鼠标右键点击元素时显示。         |
| data-*          | 用于存储页面的私有定制数据。                                 |

```html
    <div class="contenteditable" contenteditable="true">nihao tianqizhenhao</div>
    <div class="draggable" draggable="true" hidden data-a="1" data-b="2">nihao tianqizhenhao</div>
```





### H5兼容性问题

让IE浏览器处于一个 最优的渲染模式

```html
<!--设置IE总是使用最新的文档模式进行渲染-->
<meta http-equiv="X-UA-Compatible" content="IE=Edge">

<!--优先使用 webkit ( Chromium ) 内核进行渲染, 针对360等壳浏览器-->
<meta name="renderer" content="webkit">
```

使用 html5shiv 让低版本浏览器认识 H5 的语义化标签。

```html
<!--[if lt IE 9]>
<script src="../sources/js/html5shiv.js"></script>
<![endif]-->
```

**扩展**

- `lt` 小于
- `lte` 小于等于
- `gt` 大于
- `gte` 大于等于
- `!` 逻辑非

```html
<!--[if IE 8]>仅IE8可见<![endif]-->
<!--[if gt IE 8]>仅IE8以上可见<![endif]-->
<!--[if lt IE 8]>仅IE8以下可见<![endif]-->
<!--[if gte IE 8]>IE8及以上可见<![endif]-->
<!--[if lte IE 8]>IE8及以下可见<![endif]-->
<!--[if !IE 8]>非IE8的IE可见<![endif]-->
```



#### 1. 添加元信息，确保浏览器最优渲染

##### **1.1 设置IE使用最新文档模式**

- **代码**：

  ```html
  <meta http-equiv="X-UA-Compatible" content="IE=Edge">
  ```

- **作用**：  
  强制IE浏览器（如IE8/9/10/11）使用最新版本的文档模式进行渲染，避免因旧版模式导致的兼容性问题（如HTML/CSS解析差异）。

##### **1.2 优先使用 WebKit 内核（针对双核浏览器）**

- **代码**：

  ```html
  <meta name="renderer" content="webkit">
  ```

- **作用**：  
  指示双核浏览器（如360、QQ浏览器）优先采用WebKit内核（Chromium）进行页面渲染，提升HTML5/CSS3支持度和渲染效果。

---

#### 2. 使用 `html5shiv` 兼容低版本浏览器

- **代码**：

  ```html
  <!--[if lt IE 9]>
  <script src="../sources/js/html5shiv.js"></script>
  <![endif]-->
  ```

- **作用**：  

  - **兼容HTML5语义标签**：让IE9及以下版本识别 `<header>`、`<footer>`、`<article>` 等HTML5标签。  
  - **样式支持**：通过JavaScript动态创建标签，使其可被CSS样式控制。  

- **适用场景**：  
  针对仍需支持IE8及以下版本的项目，确保HTML5结构在旧版浏览器中正常显示。

---

#### 3. 条件注释的运算符

- **常见运算符**：

  | 运算符 | 含义     | 示例                  |
  | ------ | -------- | --------------------- |
  | `lt`   | 小于     | `<!--[if lt IE 9]>`   |
  | `lte`  | 小于等于 | `<!--[if lte IE 8]>`  |
  | `gt`   | 大于     | `<!--[if gt IE 7]>`   |
  | `gte`  | 大于等于 | `<!--[if gte IE 10]>` |
  | `!`    | 逻辑非   | `<!--[if !IE]>`       |

- **作用**：  
  针对IE不同版本加载特定代码（如脚本、样式），实现精细化兼容性处理。

---

##### **总结**

1. **渲染优化**：通过 `meta` 标签强制浏览器使用最优内核（如IE最新模式、WebKit），提升HTML5/CSS3兼容性。  
2. **HTML5标签兼容**：`html5shiv` 解决IE9及以下版本不支持HTML5语义标签的问题。  
3. **条件注释**：利用IE特有语法，按版本加载特定资源，实现差异化兼容策略。  
4. **适用性**：适用于需兼容旧版浏览器（如IE8/9）的项目，确保现代网页在老旧环境中稳定运行。





## CSS

### CSS特性

CSS特性：化简代码/定位问题，并解决问题

- 继承性
- 层叠性
- 优先级

#### 继承性

特点：子级默认继承父级的文字控制属性

比如在body标签设置文字控制属性，body内的文字都将默认跟随body设置

如果标签有自己的样式则生效自己的样式，不继承

- **概念**：元素会自动拥有其父元素、或其祖先元素上所设置的某些样式。
- **规则**：优先继承离得近的。
- 常见的可继承属性
  - `text-??`, `font-??`, `line-??`, `color` .....
- **备注**：参照MDN网站，可查询属性是否可被继承。



#### 层叠性

如果发生了样式冲突，那就会根据一定的规则（选择器优先级），进行样式的层叠（覆盖）

特点：

- 相同的属性会覆盖：后面的CSS属性会覆盖前面的CSS属性
- 不同的属性会叠加：不同的CSS属性都能生效



#### 优先级

- **简单聊**：`!important > 内联样式 > ID > 类 = 属性选择器 = 伪类 > 标签 > 通配符/伪元素`

- 详细聊

  ：需要计算权重。

  - 计算权重时需要注意：并集选择器的每一个部分是分开算的！

特点：优先级也叫权重，当一个标签使用了多种选择器时，基于不同种类的选择器的匹配规则

规则：选择器指向性越强，其优先级越高优先生效

> 总的来说 选中标签的范围越大，优先级越低 !important最优先

举个栗子

```html
<style>
    div{
        color: red;
    }

    .box{
        color；green;
    }
</style>

<div class="box">
    此时 div标签 内容为绿色
</div>
```

##### **详细描述**

###### 1. 计算方式：每个选择器，都可计算出一组权重，格式为：(a, b, c)

- **a**：ID 选择器的个数。
- **b**：类、伪类、属性选择器的个数。
- **c**：元素、伪元素选择器的个数。

**例如：**

| 选择器                   | 权重      |
| ------------------------ | --------- |
| ul > li                  | (0, 0, 2) |
| div ul > li p a span     | (0, 0, 6) |
| #atguigu .slogan         | (1, 1, 0) |
| #atguigu .slogan a       | (1, 1, 1) |
| #atguigu .slogan a:hover | (1, 2, 1) |

###### 2. 比较规则：按照从左到右的顺序，依次比较大小，当前位胜出后，后面的不再对比。例如：

- (1, 0, 0) > (0, 2, 2)
- (1, 1, 0) > (1, 0, 3)
- (1, 1, 3) > (1, 1, 2)

###### 3. 特殊规则：

1. 行内样式权重大于所有选择器。
2. !important 的权重，大于行内样式，大于所有选择器，权重最高！



### CSS语法

##### CSS 语法由两部分构成：

- **选择器**：找到要添加样式的元素。
- **声明块**：设置具体的样式（声明块是由一个或多个声明组成的），声明的格式为：属性名: 属性值；

###### 备注：

1. 最后一个声明后的分号理论上能省略，但最好还是写上。
2. 选择器与声明块之间，属性名与属性值之间，均有一个空格，理论上能省略，但最好还是写上。



##### 叠加计算规则

特点：如果是复合选择器，则需要权重叠加计算

公式：行内样式 > id选择器个数 > 类选择器个数 > 标签选择器个数

规则：

- 从左向右 一次比较选择器个数，同一级个数多的优先级高；个数相同，则向后比较
- `!important` 权重最高
- 继承权重最低

###### 优先级规则：行内样式 > 内部样式 = 外部样 式

1. 内部样式、外部样式，这二者的优先级相同，且：后面的会覆盖前面的（简记：“后来者居上”）。
2. 同一个样式表中，优先级也和编写顺序有关，且：后面的会覆盖前面的（简记：“后来者居上”）。

| 分类     | 优点                                                         | 缺点                                                      | 使用频率 | 作用范围 |
| -------- | ------------------------------------------------------------ | --------------------------------------------------------- | -------- | -------- |
| 行内样式 | 优先级最高                                                   | 1. 结构与样式未分离<br>2. 代码结构混乱<br>3. 样式不能复用 | 很低     | 当前标签 |
| 内部样式 | 1. 样式可复用<br>2. 代码结构清晰                             | 1. 结构与样式未彻底分离<br>2. 样式不能多页面复用          | 一般     | 当前页面 |
| 外部样式 | 1. 样式可多页面复用<br>2. 代码结构清晰<br>3. 可触发浏览器的缓存机制<br>4. 结构与样式彻底分离 | 需要引入才能使用                                          | 最高     | 多个页面 |



### CSS引入方式

#### 内部 式表

CSS代码写在 style 标签里面

1. 写在 html 页面内部，将所有的 CSS 代码提取出来，单独放在 `<style>` 标签中。
2. 语法：

```css
<style>
  h1 {
    color: red;
    font-size: 40px;
  }
</style>
```

3. 注意点：
   * `<style>` 标签理论上可以放在 HTML 文档的任何地方，但一般都放在 `<head>` 标签中。
   * 此种写法：样式可以复用、代码结构清晰。

4. 存在的问题：
   * 并没有实现：结构与样式完全分离。
   * 多个 HTML 页面无法复用样式。

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS测试场</title>
    <style>
		/*此处书写CSS代码*/
        /*选择器*/
        p{
            /*CSS属性*/
            color:red;
            font-size:30px;
            
        }
    </style>
</head>
	<body>
	<p>Hello World</p>
	</body>
</html>
```



#### 外部样式表

首先，CSS 代码写在单独的 CSS 文件中（.css）

其次，在 HTML 使用 link 标签引入

```html
<link rel="stylesheet" href="CSS文件路径">
```

**写在单独的 .css 文件中，随后在 HTML 文件中引入使用。**

1. 语法：
   * 新建一个扩展名为 .css 的样式文件，把所有 CSS 代码都放入此文件中。

```css
h1 {
  color: red;
  font-size: 40px;
}
```

2. 在 HTML 文件中引入 .css 文件。

```
<link rel="stylesheet" href="./xxx.css">
```

3. 注意点：
   * `<link>` 标签要写在 `<head>` 标签中。

```
<link>
```

 

标签属性说明：

- `href`：引入的文档来自于哪里。
- `rel`：（relation：关系）说明引入的文档与当前文档之间的关系。

1. 外部样式的优势：样式可以复用、结构清晰、可触发浏览器的缓存机制，提高访问速度，实现了结构与样式的完全分离。
2. 实际开发中，几乎都使用外部样式，这是最推荐的使用方式！



#### 行内样式表(不推荐)

通常配合 JavaScript 使用

CSS 写在标签的 style 属性值里

```html
<div style="color:red;font-size:20px">这是 CSS 行内样式</div>
```

1. 写在标签的 `style` 属性中，（又称：内联样式）。
2. 语法：

```html
<h1 style="color:red;font-size:60px;">欢迎来到尚硅谷学习</h1>
```

3. 注意点：
   * `style` 属性的值不能随便写，写要符合 CSS 语法规范，是 名:值; 的形式。
   * 行内样式表，只能控制当前标签的样式，对其他标签无效。

4. 存在的问题： 书写繁琐、样式不能复用、并且没有体现：出结构与样式分离的思想，不推荐大量使用，只有对当前元素添加简单样式时，才偶尔使用。



### CSS3私有前缀

##### **什么是私有前缀**

如下代码中的 `-webkit-` 就是私有前缀。

```css
div {
    width: 400px;
    height: 400px;
    -webkit-border-radius: 20px;
}
```

#####  **为什么要有私有前缀**

- W3C 标准所提出的某个 CSS 特性，在被浏览器正式支持之前，浏览器厂商会根据浏览器的内核，使用私有前缀来测试该 CSS 特性，在浏览器正式支持该 CSS 特性后，就不需要私有前缀了。
- 举个例子：

```css
-webkit-border-radius: 20px;
-moz-border-radius: 20px;
-ms-border-radius: 20px;
-o-border-radius: 20px;
border-radius: 20px;
```

- 查询 CSS3 兼容性的网站：https://caniuse.com/

#####  **常见浏览器私有前缀**

- Chrome 浏览器: `-webkit-`
- Safari 浏览器: `-webkit-`
- Firefox 浏览器: `-moz-`
- Edge 浏览器: `-webkit-`
- ~~旧 Opera 浏览器: `-o-`~~
- ~~旧 IE 浏览器: `-ms-`~~

注意：

>我们在编码时，不用过于关注浏览器私有前缀，不用绞尽脑汁地去记忆，也不用每个都去查询，因为常用的 CSS3 新特性，主流浏览器都是支持的，即便是为了老浏览器而加前缀，我们也可以借助现代的构建工具，去帮我们添加私有前缀。







### 选择器

作用：查找标签，设置样式

#### 常用的选择器

- 标签选择器
- 类选择器
- id选择器
- 通配符选择器

| 基本选择器 | 特点                                                 | 用法                  |
| ---------- | ---------------------------------------------------- | --------------------- |
| 通配选择器 | 选中所有标签，一般用于清除样式。                     | `* {color:red}`       |
| 元素选择器 | 选中所有同种标签，但是不能差异化选择。               | `h1 {color:red}`      |
| 类选择器   | 选中所有特定类名（class 值）的元素 —— 使用频率很高。 | `.say {color:red}`    |
| ID 选择器  | 选中特定 id 值的那个元素（唯一的）。                 | `#earthy {color:red}` |

> 选择器优先级：

- `!important > 内联样式 > ID > 类 = 属性选择器 = 伪类 > 标签 > 通配符/伪元素`

#### 标签选择

标签选择器：使用标签名作为选择器，选中同名标签设置的相同样式

> 相同标签名的所有标签都会受到设置的相同样式

#### 元素选择器

###### 作用：为页面中某种元素统一设置样式。

- **语法**：

  ```css
  标签名 {
      属性名: 属性值;
  }
  ```

- **举例**：

  ```css
  /* 选中所有h1元素 */
  h1 {
      color: orange;
      font-size: 40px;
  }
  
  /* 选中所有p元素 */
  p {
      color: blue;
      font-size: 60px;
  }
  ```

- **备注**：元素选择器无法实现差异化设置，例如上面的代码中，所有的 p 元素效果都一样。



#### 类选择器

根据元素的 class 值，来选中某些元素

类选择器：查找标签，差异化设置标签的显示效果

实现步骤：

- 定义类选择器：`.类名`
- 使用类选择器：`标签添加 class="类名"`

```css
.red{
    color:red;
}
```



此时，要在目标标签中添加 `class` 属性

```html
<div class="red">
    此时，css中，类名为red的选择器将触发，同时内部的设置将被应用
</div>
```

**注意：**

- 类名自定义，不要用纯数字、数字开头或中文，尽量用英文命名
- 一个类选择器可以供多个标签使用
- 一个标签可以使用多个类名，类名之间用空格隔开
- 命名时如要使用多个单词，可以使用 `-` 连接



#### id选择器

根据元素的 id ，精准的选中某个元素

id选择器：查找标签，差异化设置标签的显示效果

场景：id选择器通常配合 JavaScript 使用，很少用来设置CSS样式

实现步骤：

- 定义 id选择器：`#id`
- 使用 id选择器：`标签添加属性 id="id名"`

 类似于类选择器，将 `.`换成`#` ， 将`class`属性 换成 `id`属性

**注意：**

* 一个标签不能使用多个id

* 不可以是数字开头，不要有空格



#### 通配符选择器

可以选中多有的 HTML 元素

但是，清楚样式的时候，会有很大的帮助

通配符选择器：查找页面所有标签，设置相同样式

使用方法：*，不需要调用，浏览器自动查找页面所有标签，设置相同的样式

```css
*{
    color:red;
}
```



#### 复合选择器

作用：由两个或多个基础选择器，通过不同的方式组合而成

复合选择器有多种，以下将逐步介绍



##### 交集选择器

**作用：选中同时符合多个条件的元素。**

- **交集有并且的含义**（通俗理解：即……又……的意思），例如：年轻且长得帅。

- **语法**：

  ```
  选择器1选择器2选择器3...选择器n {}
  ```

- **举例**：

  ```css
  /* 选中：类名为beauty的p元素，为此种写法用的非常多！！！！ */
  p.beauty {
      color: blue;
  }
  
  /* 选中：类名包含rich和beauty的元素 */
  .rich.beauty {
      color: green;
  }
  ```

- **注意**：

  1. 有标签名，标签名必须写在前面。
  2. id 选择器、理论上可以作为交集的条件，但实际应用中几乎不用 —— 因为没有意义。
  3. 交集选择器中不可能出现两个元素选择器，因为一个元素，不可能即是 p 元素又是 span 元素。
  4. 用的最多的交集选择器是：元素选择器配合类名选择器，例如：`p.beauty`。



##### 并集选择器

**作用：选中多个选择器对应的元素，又称：分组选择器。**

- **所谓并集就是或者的含义**（通俗理解：要么……要么……的意思），例如：给我转10万块钱或者我报警。

- **语法**：

  ```
  选择器1, 选择器2, 选择器3, ... 选择器n {}
  ```

  多个选择器通过逗号连接，此处逗号的含义就是：或。

- **举例**：

  ```css
  /* 选中id为peiqi，或类名为rich，或类名为beauty的元素 */
  #peiqi,
  .rich,
  .beauty {
      font-size: 40px;
      background-color: skyblue;
      width: 200px;
  }
  ```

- **注意**：

  1. 并集选择器，我们一般竖着写。
  2. 任何形式的选择器，都可以作为并集选择器的一部分。
  3. 并集选择器，通常用于集体声明，可以缩小样式表体积。



##### 后代选择器

* 选中指定元素中，符合要求的后代元素

* 语法：选择器1 选择器2 选择器3 ...... 选择器n {} （先写祖先，再写后代）
  * **选择器之间，用空格隔开，空格可以理解为："xxx 中的"，其实就是后代的意思。**
  * **选择器 1234 .... n，可以是我们之前学的任何一种选择器。**

举例：

```css
/* 选中ul中的所有li */
ul li {
    color: red;
}

/* 选中ul中所有li中的a */
ul li a {
    color: orange;
}

/* 选中类名为subject元素中的所有li */
.subject li {
    color: blue;
}

/* 选中类名为subject元素中的所有类名为front-end的li */
.subject li.front-end {
    color: blue;
}
```

注意：

1. 后代选择器，最终选择的是后代，不选中祖先。
2. 儿子、孙子、重孙子，都算是后代。
3. 结构一定要符合之前讲的 HTML 嵌套要求，例如：不能 p 中写 h1 ~ h6。



##### 子代选择器

- **作用**：选中指定元素中，符合要求的子元素（儿子元素）。（先写父，再写子）

  - 子代选择器又称：子元素选择器、子选择器。

- **语法**：

  ```
  选择器1 > 选择器2 > 选择器3 > ...... 选择器n {}
  ```

  - 选择器之间，用 `>` 隔开，`>` 可以理解为："xxx 的子代"，其实就是儿子的意思。
  - 选择器 1234 .... n，可以是我们之前学的任何一种选择器。

- **举例**：

  ```css
  /* div中的子代a元素 */
  div > a {
      color: red;
  }
  
  /* 类名为persons的元素中的子代a元素 */
  .persons > a {
      color: red;
  }
  ```

- **注意**：

  1. 子代选择器，最终选择的是子代，不是父级。
  2. 子、孙子、重孙子、重重孙子......统称后代！，子就是指儿子。



##### 相邻兄弟选择器

选中指定元素后，符合条件的相邻兄弟元素（紧挨着的下一个）

相邻兄弟选择器（Adjacent sibling selector）可选择紧接在另一元素后的元素，且二者有相同父元素。

如果需要选择紧接在另一个元素后的元素，而且二者有相同的父元素，可以使用相邻兄弟选择器（Adjacent sibling selector）。

```css
div+p {
    background-color:yellow; /*选择div之后紧邻的兄弟p元素*/
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
    div+p{
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



##### 后续兄弟选择器

后续兄弟选择器选取所有指定元素之后的**所有兄弟元素**。

选择器1 ~ 选择器2

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



#### 伪类选择器

很像类，但不是类，是元素特殊状态的一种描述

作用：伪类选择器表示元素状态，选中某个元素的某个状态设置样式

使用方法：`选择器` `:伪类` `{CSS属性}`

常用伪类有

- `:hover` - 当用户将鼠标指针悬停在元素上时应用的样式
- `:focus` - 当元素获得键盘焦点时应用的样式，例如通过Tab键导航到该元素

> 个人感觉，CSS伪类选择器的功能类似于面向对象编程中基于对象状态自动调用特定方法
>
> 其允许我们针对元素的不同状态定义和应用不同的样式规则，从而在不编写额外脚本的情况下实现元素外观的动态变化



##### 动态伪类



|  选择器  |             作用             |
| :------: | :--------------------------: |
|  :link   |         没有访问过的         |
| :visited |           访问过的           |
|  :hover  |           鼠标悬停           |
| :active  | 点击时(按下不动可以看到效果) |
|  :focus  |    元素被获取焦点时被选中    |

> 如果要给超链接同时设置上表中多个状态，需要按 LVHA 的顺序书写

去除超链接默认

```css
a {
    color: inherit; /* 使用父元素的颜色 */
    text-decoration: none;
}
```

**鼠标悬停，让隐藏的部分显示出来**

方法一：使用 `display` 属性（推荐用于完全隐藏/显示块级元素）

```
/* 默认隐藏 */
.hidden-content {
    display: none;
}

/* 父元素悬停时显示 */
.parent:hover .hidden-content {
    display: block; /* 或 inline-block, flex 等 */
}
```



```
<div class="parent">
    悬停我
    <div class="hidden-content">
        这是隐藏的内容
    </div>
</div>
```

> ⚠️ 注意：`display: none` 会完全从文档流中移除元素，不能直接用于过渡动画。

------

方法二：使用 `opacity` 和 `visibility`（支持过渡动画）

```
.hidden-content {
    opacity: 0;
    visibility: hidden;
    transition: opacity 0.3s ease, visibility 0.3s ease;
}

.parent:hover .hidden-content {
    opacity: 1;
    visibility: visible;
}
```



```
<div class="parent">
    悬停我
    <div class="hidden-content">
        这是隐藏的内容
    </div>
</div>
```

> ✅ 优点：可以添加平滑的淡入淡出效果。

------

方法三：使用 `transform` 实现滑动/缩放效果



```css
.hidden-content {
    opacity: 0;
    transform: translateY(-10px); /* 初始位置偏移 */
    visibility: hidden;
    transition: all 0.3s ease;
}

.parent:hover .hidden-content {
    opacity: 1;
    transform: translateY(0);
    visibility: visible;
}
```

> ✅ 优点：可以实现滑入、缩放等动效，用户体验更好。

------

方法四：结合 `overflow: hidden` 实现区域裁剪



```
.parent {
    overflow: hidden; /* 隐藏溢出内容 */
    height: 50px;
    transition: height 0.3s ease;
}

.parent:hover {
    height: 150px; /* 悬停时展开 */
}
```

> 适用于手风琴、展开面板等效果。

------

实际应用示例：下拉菜单

```
.menu {
    position: relative;
}

.dropdown {
    display: none;
    position: absolute;
    top: 100%;
    left: 0;
    background: #333;
    color: white;
    padding: 10px;
}

.menu:hover .dropdown {
    display: block;
}
```



##### 结构伪类

###### **常用的伪类选择器**

1. **:first-child**：所有兄弟元素中的第一个。
2. **:last-child**：所有兄弟元素中的最后一个。
3. **:nth-child(n)**：所有兄弟元素中的第 n 个。
4. **:first-of-type**：所有同类型兄弟元素中的第一个。
5. **:last-of-type**：所有同类型兄弟元素中的最后一个。
6. **:nth-of-type(n)**：所有同类型兄弟元素中的第 n 个。

**关于 n 的值：**

1. **0 或 不写**：什么都选不中——几乎不用。
2. **n**：选中所有子元素——几乎不用。
3. **1~正无穷的整数**：选中对应序号的子元素。
4. **2n 或 even**：选中序号为偶数的子元素。
5. **2n+1 或 odd**：选中序号为奇数的子元素。
6. **-n+3**：选中的是前 3 个。

**伪类选择器**

1. **:nth-last-child(n)**：所有兄弟元素中的倒数第 n 个。
2. **:nth-last-of-type(n)**：所有**同类型**兄弟元素中的倒数第 n 个。
3. **:only-child**：选择没有兄弟的元素（独生子女）。
4. **:only-of-type**：选择没有同类型兄弟的元素。
5. **:root**：根元素。
6. **:empty**：内容为空元素（空格也算内容）。



##### **否定伪类**

：not(选择器) 排除满足括号中条件的元素

```html
    <style>
        /* 选中的是div的儿子p元素，但是排除类名为fail的元素 */
        div>p:not([title^="加油"]) {
            color: #067234;
        }
    </style>
</head>

<body>
    <div>
        <span>ceshi</span>
        <p>测试2</p>
        <p>张三</p>
        <p>王五</p>
        <p>赵六</p>
        <p class="fail" title="加油">第一个</p>
        <p class="fail" title="加油">第二个</p>
        <p>第三个</p>
        <span>ceshi2</span>
    </div>
```



##### UI伪类

1. **:checked**：被选中的复选框或单选按钮。
2. **:enable**：可用的表单元素（没有 `disabled` 属性）。
3. **:disabled**：不可用的表单元素（有 `disabled` 属性）。

```html
    <style>
        input:checked {
            width: 100px;
            height: 100px;
        }

        input:enabled {
            background-color: green;
        }

        input:disabled {
            background-color: grey;
        }
    </style>
</head>

<body>
    <input type="checkbox">
    <input type="radio" name="gender">
    <input type="radio" name="gender">
    <input type="text">
    <input type="text" disabled>
</body>
```



##### 目标伪类

：target	选中锚点指向的元素

```html
    <style>
        div {
            background-color: #e55599;
            height: 300px;
        }

        div:target {
            background-color: #999999;
        }
    </style>
</head>

<body>
    <a href="#one">去看第一个</a>
    <a href="#two">去看第二个</a>
    <a href="#three">去看第三个</a>
    <a href="#four">去看第四个</a>
    <a href="#five">去看第五个</a>
    <br>
    <div id="one">第一个</div>
    <br>
    <div id="two">第二个</div>
    <br>
    <div id="three">第三个</div>
    <br>
    <div id="four">第四个</div>
    <br>
    <div id="five">第六个</div>
    <br>
</body>

```



##### 语言伪类

：lang（语言类型，例：en,zh-CN） 根据指定的语言选择元素（本质是看lang属性的本质）

```html
    <style>
        div:lang(en) {
            color: #889999;
        }

        div:lang(zh-CN) {
            color: blueviolet;
        }
    </style>
</head>

<body>
    <div>尚硅谷</div>
    <div lang="en">atguigu</div>
    <p>前端</p>
    <span>你好</span>
</body>
```



#### 属性选择器

| 选择器           | 示例            | 示例说明                                   |
| ---------------- | --------------- | ------------------------------------------ |
| attribute        | [target]        | 选择所有带有target属性元素                 |
| attribute=value  | [target=_blank] | 选择所有使用target="-blank"的元素          |
| attribute~=value | [title~=flower] | 选择标题属性**包含单词**"flower"的所有元素 |

**属性选择器**

1.  所有带target的元素
2.  选择具有特定target属性值的元素
3.  选中具有title属性，且属性值以字母 a 开头的元素
4.  选中具有title属性，且属性值以字母 u 结尾的元素
5.  选中具有title属性，且属性值包含字母 u 的元素

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    /* 所有带target的元素 */
    [target] {
      color: red;
    }

    /* 选择具有特定target属性值的元素 */
    [target="_blank"] {
      font-weight: bold;
    }

    /* 选择标题属性中包含特定单词的元素 */
    [title~=flower] {
      background-color: yellow;
    }
      
     /*险种具有title属性，且属性值以字母 a 开头的元素*/
     [title^="a"]{
          color:red;
     }
      
      /*选中具有title属性，且属性值以字母 u 结尾的元素*/
      [title$ = "u"]{
		color:red;
      }
      
      /*选中具有title属性，且属性值包含字母 u 的元素*/
      [title* = "u"]{
		color:red;
      }
  </style>
</head>

<body>
  <a href="https://www.example.com" target="_blank">Example 1</a>
  <a href="https://www.example2.com">Example 2</a>
  <a href="https://www.example3.com" target="_self">Example 3</a>

  <p title="flower garden">This is a flower garden.</p>
  <p title="flower pot">This is a flower pot.</p>
  <p title="garden">This is a garden.</p>
</body>

</html>
```



#### 伪元素选择器

很像元素，但不是元素，是元素中的一些特殊位置

- **作用**：选中元素中的一些特殊位置。
- **常用伪元素**：
  - `::first-letter` 选中元素中的**第一个**文字。
  - `::first-line` 选中元素中的**第一行**文字。
  - `::selection` 选中被**鼠标选中**的内容。
  - `::placeholder` 选中**输入框**的提示文字。
  - `::before` 在元素**最开始**的位置，创建一个子元素（必须用 `content` 属性指定内容）。
  - `::after` 在元素**最后**的位置，创建一个子元素（必须用 `content` 属性指定内容）。

**案例1：**

```html
    <style>
        /* 伪元素选择器 */
        /* 选中的是p元素最开始的位置，随后创建一个子元素 */
        p::before {
            content: "￥";
        }

        /* 选中的是p元素最最后的位置，随后创建一个子元素 */
        p::after {
            content: ".00";
        }
    </style>
</head>

<body>
    <!-- 伪元素选择器 -->
    <p>199</p>
    <p>446</p>
    <p>2345</p>
    <p>567</p>
    <p>245</p>
    <p>3568</p>

</body>
```

**案例2：**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>示例 2</title>
    <style>
      li:after {
          content: " ✔";
      }

      li:before {
          content: "👉 ";
      }
  </style>
</head>

<body>
    <ul>
        <li>苹果</li>
        <li>香蕉</li>
        <li>橙子</li>
    </ul>
</body>

</html>
```

**案例3：**

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

> 更多案例：https://juejin.cn/post/6854573204011221000?searchId=20250304161555AB9052027619DCBA5761

> E是指定的标签或选择器，本选择器相当于给父标签添加个子级元素，在标签内部添加装饰性的元素

注意点：

- 必须设置 content:"  " 属性，否则元素不生效，content用来设置 伪元素的内容，如果没有内容，引号留空即可
- 伪元素默认是行内显示模式（也就是说，无法手动设置宽高，除非使用display转换显示模式）
- 权重和标签选择器相同





### 属性

可以控制元素

#### 常用属性

键值对：通常，我们将属性名与属性值成对出现的属性叫键值对

| 属性名           | 说明     |
| ---------------- | -------- |
| color            | 文字颜色 |
| font-size        | 字体大小 |
| width            | 宽度     |
| height           | 高度     |
| background-color | 背景色   |
|                  |          |
|                  |          |
|                  |          |
|                  |          |







#### 字体属性

字体属性表

| 名称         | 属性名            | 说明               |
| ------------ | ----------------- | ------------------ |
| 字体大小     | font-size         | 修改文字大小       |
| 字体粗细     | font-weight       | 修改文字粗细       |
| 字体倾斜     | font-style        | 使文字倾斜         |
| 行高         | line-height       | 修改行高           |
| 字体族       | font-family       | 修改字体，如宋体   |
| 字体复合属性 | font              | 复合属性           |
| 文本缩进     | text-indent  (em) | 修改前后缩进       |
| 文本对齐     | text-align        | 修改文本对齐方式   |
| 修饰线       | text-decoration   | 上中下贯穿文本的线 |
| 颜色         | color             | 修改文字颜色       |

##### 引入自定义字体

属性名：`@font-face{ }`

引入字体后无需客户端安装，自动使用引入的字体

```css
@font-face {
    font-family:bbt;/*字体名叫bbt*/
    src: url(../btt.ttf);/*相对路径引入*/
}
```



##### 字体大小

属性名：font-size

属性值：文字尺寸，PC 端网页常用单位 `px`

> 通常来说，谷歌浏览器默认字体大小为16px



##### 字体粗细

属性名：font-weight

属性值：

- **数字**

正常为400，加粗为800

- **关键字**

正常：`normal` ，加粗：`bold`



##### 字体倾斜

属性名：font-style

属性值：不倾斜 `nomal`   倾斜 `italic`



##### 行高

作用：设置多行文本的间距

属性名：line-height

属性值：

- 数字 + px
- 数字（当前标签font-size属性值的倍数）



##### 字体族

属性名：font-family

属性值：字体名

font-family属性值可以书写多个字体名，各个字体名用 逗号 隔开，执行顺序从左到右依次查找

其最后一个属性可以设置一个字体族名，其作用为 当前面的字体皆未找到，将使用通用的字体族，比如 sans-seif 为无衬线字体

```css
font-family:楷体;

font-family:Microsoft YaHei,Heiti SC,tahoma,arial,Hiragino Sans GB,"\5B8B\4F53",sans-seif;
```



##### font复合属性

复合属性：属性的间歇方式，一个属性对应多个值的写法，各个属性之间用空格隔开

font： 是否倾斜 是否加粗 字号/行高 字体（必须按顺序书写）

注意：字号和字体值必须书写也必须按顺序书写，否则 font 属性不生效

就是把上面的属性合成一行，食用方法如下

```css
/*font：是否倾斜 是否加粗 字号/行高 字体;*/
font: italic 700 30px/2 楷体; 
```

```css
font-style         规定文本的字体样式。
font-weight        规定字体是否加粗
font-size          规定字体的大小，通常是以 px 为单位
font-family        规定文本的字体系列（字体族）
line-height        设置行高
 
 
font-style: italic;
font-weight: 400;
font-size: 20px;
line-height: 200px;
font-family: "宋体";
```



##### web字体

可以通过 `@font-face` 指定字体的具体地址，浏览器会自动下载该字体，这样就不依赖用户电脑上的字体了。

语法（简写方式）

```css
@font-face {
    font-family: "情书字体";
    src: url('./方正手迹.ttf');
}
```

语法（高兼容性写法）

```css
@font-face {
    font-family: "atguigu";
    font-display: swap;
    src: url('webfont.eot'); /* IE9 */
    src: url('webfont.eot?#iefix') format('embedded-opentype'), /* IE6-IE8 */
         url('webfont.woff2') format('woff2'),
         url('webfont.woff') format('woff'), /* chrome、firefox */
         url('webfont.ttf') format('truetype'), /* chrome、firefox、opera、Safari, Android*/
         url('webfont.svg#webfont') format('svg'); /* iOS 4.1- */
}
```

定制字体

- 中文的字体文件很大，使用完整的字体文件不现实，通常针对某几个文字进行单独定制。
- 可使用阿里 Web 字体定制工具： https://www.iconfont.cn/webfont



#### 文本属性

##### 文本缩进

属性名：text-indent

属性值：

- 数字 + px
- 数字 + em（1em = 当前标签的字号大小）

经常用来首行空两格，em就相当于一个字，会随字号更改，所以使用em更多



##### 文本对齐

作用：控制内容水平对齐方式

属性名：text-align

属性值：

| 属性值 | 效果           |
| ------ | -------------- |
| left   | 左对齐（默认） |
| center | 居中对齐       |
| right  | 右对齐         |

text-align本质使控制内容的对齐方式，属性要设置给内容的父级

举个栗子：让图片居中不能在 `<img>` 标签中使用属性，需要给其父标签添加属性



##### 文本间距

- **字母间距**：`letter-spacing`
- **单词间距**：`word-spacing`（通过**空格**识别词）
- **属性值为像素（px），正值让间距增大，负值让间距缩小。**



##### 文本阴影

在 CSS3 中，我们可以使用 `text-shadow` 属性给文本添加阴影。

语法：

```css
text-shadow: h-shadow v-shadow blur color;
```

| 值         | 描述                                   |
| ---------- | -------------------------------------- |
| `h-shadow` | 必需写，**水平**阴影的位置。允许负值。 |
| `v-shadow` | 必需写，**垂直**阴影的位置。允许负值。 |
| `blur`     | 可选，模糊的距离。                     |
| `color`    | 可选，阴影的颜色                       |

默认值：

- `text-shadow: none` 表示没有阴影。



##### 文本换行

在 CSS3 中，我们可以使用 `white-space` 属性设置文本换行方式。

常用值如下：

| 值         | 含义                                                         |
| ---------- | ------------------------------------------------------------ |
| `normal`   | 文本超出边界自动换行，文本中的换行被浏览器识别为一个空格。（默认值） |
| `pre`      | 原样输出，与 `<pre>` 标签的效果相同。                        |
| `pre-wrap` | 在 `pre` 效果的基础上，超出元素边界自动换行。                |
| `pre-line` | 在 `pre` 效果的基础上，超出元素边界自动换行，且只识别文本中的换行，空格会忽略。 |
| `nowrap`   | 强制不换行                                                   |



##### 文本溢出

在 CSS3 中，我们可以使用 `text-overflow` 属性设置文本内容溢出时的呈现模式。

常用值如下：

| 值         | 含义                                           |
| ---------- | ---------------------------------------------- |
| `clip`     | 当内联内容溢出时，将溢出部分裁切掉。（默认值） |
| `ellipsis` | 当内联内容溢出块容器时，将溢出部分替换为 ...   |

注意：

要使得 `text-overflow` 属性生效，块容器必须显式定义 `overflow` 为非 `visible` 值，`white-space` 为 `nowrap` 值。

```css
.text {
  width: 200px;
  white-space: nowrap;           /* 禁止换行 */
  overflow: hidden;              /* 隐藏溢出 */
  text-overflow: ellipsis;       /* 显示省略号 */
}
```



##### 文本修饰

CSS3 升级了 `text-decoration` 属性，让其变成了复合属性。

```css
text-decoration: text-decoration-line || text-decoration-style || text-decoration-color;
```

子属性及其含义：

- **`text-decoration-line`** 设置文本装饰线的位置
  - `none`：指定文字无装饰（默认值）
  - `underline`：指定文字的装饰是下划线
  - `overline`：指定文字的装饰是上划线
  - `line-through`：指定文字的装饰是贯穿线
- **`text-decoration-style`** 文本装饰线条的形状
  - `solid`：实线（默认）
  - `double`：双线
  - `dotted`：点状线条
  - `dashed`：虚线
  - `wavy`：波浪线
- **`text-decoration-color`** 文本装饰线条的颜色



##### 文本描边

注意：文字描边功能仅 **webkit** 内核浏览器支持。

- `-webkit-text-stroke-width`：设置文字描边的宽度，写长度值。
- `-webkit-text-stroke-color`：设置文字描边的颜色，写颜色值。
- `-webkit-text-stroke`：复合属性，设置文字描边宽度和颜色。





##### 行高

 属性名：`line-height`

- **可选值**：

  1. `normal`：由浏览器根据文字大小决定的一个默认值。
  2. 像素 (`px`)。
  3. 数字：参考自身 `font-size` 的倍数（很常用）。
  4. 百分比：参考自身 `font-size` 的百分比。

- **备注**：由于字体设计原因，文字在一行中，并不是绝对垂直居中，若一行中都是文字，不会太影响观感。

- **举例**：

  ```css
  div {
    line-height: 60px;
    line-height: 1.5;
    line-height: 150%;
  }
  ```

**注意事项**：

行高注意事项：

1. `line-height` 过小会怎样？—— 文字产生重叠，且最小值是 0，不能为负数。

2. `line-height` 是可以**继承的**，且为了能更好的呈现文字，最好写数值。

3. ```
   line-height
   ```

   和

   ```
   height
   ```

   是什么关系？

   - 设置了 `height`，那么高度就是 `height` 的值。
   - 不设置 `height` 的时候，会根据 `line-height` 计算高度。

应用场景：

1. 对于多行文字：控制行与行之间的距离。
2. 对于单行文字：让 `height` 等于 `line-height`，可以实现文字垂直居中。



**文本对齐_垂直**

1. **顶部**：无需任何属性，在垂直方向上，默认就是顶部对齐。

2. **居中**：对于单行文字，让 `height = line-height` 即可。

   - **问题**：多行文字垂直居中怎么办？——后面我们用定位去做。

3. **底部**：对于单行文字，目前一个临时的方式：

   - 让

     ```css
     line-height = (height × 2) - font-size - x
     ```

     - **备注**：`x` 是根据字体族，动态决定的一个值。

- **问题**：垂直方向上的底部对齐，更好的解决办法是什么？——后面我们用定位去做。



##### vertical-align	基线对齐

属性名：`vertical-align`

- **作用**：用于指定同一行元素之间，或表格单元格内文字的垂直对齐方式。
- **常用值**：
  1. `baseline`（默认值）：使元素的基线与父元素的基线对齐。
  2. `top`：使元素的顶部与其所在行的顶部对齐。
  3. `middle`：使元素的中部与父元素的基线加上父元素字母 x 的一半对齐。
  4. `bottom`：使元素的底部与其所在行的底部对齐。
- **特别注意**：`vertical-align` 不能控制块元素。



##### 文本修饰线

属性名：text-decoation
属性值：

| 属性值       | 效果   |
| ------------ | ------ |
| none         | 无     |
| underline    | 下划线 |
| line-through | 删除线 |
| overline     | 上划线 |



##### 文字颜色

属性名：color

属性值：

| 表示方法       | 属性值        | 说明                            |
| -------------- | ------------- | ------------------------------- |
| 颜色关键字     | 颜色英文单词  | red、green、blue                |
| rgb表示法      | rgb(r,g,b)    | r,g,b表示红绿蓝三原色           |
| rgba表示法     | rgba(r,g,b,a) | a表示透明度，取值0-1            |
| 十六进制表示法 | #RRGGBB       | #000000，#ffcc00 简写:#000,#fc0 |

###### 表示方式一：颜色名

- **编写方式**：直接使用颜色对应的英文单词，编写比较简单，例如：

  1. 红色: red
  2. 绿色: green
  3. 蓝色: blue
  4. 紫色: purple
  5. 橙色: orange
  6. 灰色: gray .......

- **说明**：

  1. 颜色名这种方式，表达的颜色比较单一，所以用的并不多。
  2. 具体颜色名参考 MDN 官方文档:
     - https://developer.mozilla.org/en-US/docs/Web/CSS/named-color

  

###### 表示方式二：rgb 或 rgba

- **编写方式**：使用红、黄、蓝这三种光的三原色进行组合。
  - r 表示红色
  - g 表示绿色
  - b 表示蓝色
  - a 表示透明度
- **举例**：

```css
/* 使用0~255之间的数字表示一种颜色 */
color: rgb(255, 0, 0); /* 红色 */
color: rgb(0, 255, 0); /* 绿色 */
color: rgb(0, 0, 255); /* 蓝色 */
color: rgb(0, 0, 0); /* 黑色 */
color: rgb(255, 255, 255); /* 白色 */

/* 混合出任意一种颜色 */
color: rgb(138, 43, 226); /* 紫罗兰色 */
color: rgba(255, 0, 0, 0.5); /* 半透明的红色 */

/* 也可以使用百分比表示一种颜色（用的少） */
color: rgb(100%, 0%, 0%); /* 红色 */
color: rgba(100%, 0%, 0%, 50%); /* 半透明的红色 */
```

- 小规律 
  1. 若三种颜色值相同，呈现的是灰色，值越大，灰色越浅。
  2. `rgb(0, 0, 0)` 是黑色，`rgb(255, 255, 255)` 是白色。
  3. 对于 `rgba` 来说，前三位的 `rgb` 形式要保持一致，要么都是 `0~255` 的数字，要么都是百分比。



###### 表示方式三：HEX 或 HEXA

**HEX 的原理同与 rgb 一样，依然是通过：红、绿、蓝色进行组合，只不过要用 6 个数字，分成 3 组来表达，格式为：#rrggbb**

- **每一位数字的取值范围是：0 ~ f ，即：（0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a, b, c, d, e, f）**
- **所以每一种光的最小值是：00，最大值是：ff**

```css
color: #ff0000; /* 红色 */
color: #00ff00; /* 绿色 */
color: #0000ff; /* 蓝色 */
color: #000000; /* 黑色 */
color: #ffffff; /* 白色 */

/* 如果每种颜色的两位都是相同的，就可以简写 */
color: #ff9988; /* 可简写为：#f98 */

/* 但要注意前三位简写了，那么透明度就也要简写 */
color: #ff998866; /* 可简写为：#f986 */
```

**注意点：IE 浏览器不支持 HEXA，但支持 HEX。**



######  表示方式四：HSL 或 HSLA

- **HSL 是通过： 色相、饱和度、亮度，来表示一个颜色的，格式为：hsl(色相, 饱和度, 亮度)**

  - **色相**

    ：取值范围是 0~360 度，具体度数对应的颜色如下图：

    - Red: 0°
    - Yellow: 60°
    - Green: 120°
    - Cyan: 180°
    - Blue: 240°
    - Magenta: 300°

  - **饱和度**：取值范围是 0%~100%。（向色相中对应颜色中添加灰色，0% 全灰，100% 没有灰）

  - **亮度**：取值范围是 0%~100%。（0% 亮度没了，所以就是黑色。100% 亮度太强，所以就是白色了）

- **HSLA 其实就是在 HSL 的基础上，添加了透明度。**



##### 不透明度opacity

`opacity` 属性能为整个元素添加透明效果，值是 0 到 1 之间的小数，0 是完全透明，1 表示完全不透明。

**`opacity` 与 `rgba` 的区别？**

- **`opacity`** 是一个属性，设置的是整个元素（包括元素里的内容）的不透明度。
- **`rgba`** 是颜色的设置方式，用于设置颜色，它的透明度，仅仅是调整颜色的透明度



#### 背景属性

##### 背景图

属性名：background-image(bgi)

属性值：url(背景图的 URL)

在网页中，使用背景图实现 **装饰性** 的图片效果



举个栗子

```css
div{
    width: 400px;
    height: 400px;
    
    background-image: url(./images/1.png);
    
}
```

为以上例子做解释，设置 div标签 样式为宽高400px，并且将背景图设置为相对路径的1.png



> 提示：在浏览器中，背景图默认是平铺的效果，也就是容器的尺寸大就会复制几张填充满；同时，因为是背景图，div标签中有文字将显示在图片之上



##### 背景图平铺方式

属性名：background-repeat (bgr)

属性值：

| 属性值    | 效果             |
| --------- | ---------------- |
| no-repeat | 不平铺           |
| repeat    | 平铺（默认效果） |
| repeat-x  | 水平方向平铺     |
| repeat-y  | 垂直方向平铺     |

以下是对各个属性值效果的描述：

- no-repeat：只有一张图片，显示在容器的左上角不会扩展
- repeat：复制图片填满容器
- repeat-x：只有横向复制图片
- repeat-y：只有竖向复制图片



##### 背景图位置

属性名：background-position (bgp)

属性值：水平方向位置 垂直方向位置

关键字：

| 关键字 | 位置 |
| ------ | ---- |
| left   | 左侧 |
| right  | 右侧 |
| center | 居中 |
| top    | 顶部 |
| bottom | 底部 |

坐标： 数字 + px  /  关键字

注意事项：

- 数字可以与关键字混用

- 数字正负皆可

- 数字是从容器左上角计算

- 水平方向正数向右移动，负数像左侧移动；

- 垂直方向正数向下移动，负数向上移动；

  * top: 50%;     /* 向下移动 50% 的父元素高度 */

  * left: 50%;      /* 向右移动 50% 的父元素宽度 */

- 超出容器的部分会被裁切

**特殊提醒：**

- 关键字取值方式写法，可以颠倒取值顺序
- 可以只写一个关键字，另一个方向默认居中；数字只写一个值表示水平方向，垂直方向为居中



##### 背景图缩放

属性名：background-size (bgz)

作用：设置背景图大小

常用属性值：

- 关键字

​	cover：等比例缩放背景图片以**完全覆盖背景区**，可能背景图部分看不见

​	contain：等比例缩放背景图片以完全装入背景区，可能背景区部分空白

- 百分比：根据容器尺寸计算图片大小，注意：100%表示图片的宽度跟容器的宽度一样，图片的高度按照图片比例等比例缩放
- 数字 + 单位（例如：px）



##### 背景图固定

属性名：background-attachment (bga)

属性值：fixed

作用：背景不会随着元素的内容滚动



##### 背景图原点

background-origin

它用于**定义背景图像（`background-image`）的定位起点（即坐标原点 `(0,0)` 的位置）**。

- **作用**：设置背景图的原点。
- **语法**
  1. `padding-box`：从 padding 区域开始显示背景图像。--- 默认值
  2. `border-box`：从 border 区域开始显示背景图像。
  3. `content-box`：从 content 区域开始显示背景图像。



##### background-clip

它控制**背景（包括背景图和背景色）的绘制区域**，即“裁剪”到哪个盒子。

- `background-clip: border-box`(默认)
  - 背景绘制到边框区域下。
- `background-clip: padding-box`
  - 背景绘制到内边距区域，不绘制在边框下。
- `background-clip: content-box`
  - 背景只绘制在内容区域。

> ✅ **注意**：`background-clip` 是向“内”裁剪，即决定背景能画到哪个区域为止，而不是“向外裁剪”。

- **作用**：设置背景图的向外裁剪的区域。
- **语法**
  1. `border-box`：从 border 区域开始向外裁剪背景。--- 默认值
  2. `padding-box`：从 padding 区域开始向外裁剪背景。
  3. `content-box`：从 content 区域开始向外裁剪背景。
  4. `text`：背景图只呈现在文字上。
- **注意**：若值为 `text`，那么 `background-clip` 要加上 `-webkit-` 前缀。



#####  背景图尺寸

background-size

- **作用**：设置背景图的尺寸。

- **语法**

  1. **用长度值指定背景图片大小，不允许负值。**

     ```css
     background-size: 300px 200px;
     ```

  2. **用百分比指定背景图片大小，不允许负值。**

     ```css
     background-size: 100% 100%;
     ```

  3. **`auto`**：背景图片的真实大小。--- 默认值

  4. **`contain`**：将背景图片等比缩放，使背景图片的宽或高，与容器的宽或高相等，再将完整背景图片包含在容器内，但要注意：可能会造成容器里部分区域没有背景图片。

     ```css
     background-size: contain;
     ```

  5. **`cover`**：将背景图片等比缩放，直到**完全覆盖容器**，图片会尽可能全的显示在元素上，但要注意：背**景图片有可能显示不完整**。--- 相对比较好的选择

     ```css
     background-size: cover;
     ```





##### 背景复合属性

属性名：background (bg)

属性值：背景色 背景图 背景图平铺方式 背景图位置/背景图缩放 背景图固定（空格隔开各个属性值，不区分顺序）

> 类似于字体复合属性值，就是一条写出整个背景图的属性

```css
div()
{
    width: 400px;
    height: 400px;
    
    background: pink url(./images/1.png) no-repeat right center/cover;
}
```

> 翻一下就是背景粉色，图片为1.png，不平铺，水平靠右侧，垂直居中，等比例缩放完全覆盖容器，可能有截取

语法：

```css
background: color url repeat position / size origin clip
```

注意：

1. `origin` 和 `clip` 的值如果一样，如果只写一个值，则 `origin` 和 `clip` 都设置；如果设置了两个值，前面的是 `origin`，后面的 `clip`。
2. `size` 的值必须写在 `position` 值的后面，并且用 `/` 分开。



##### 多背景图

background-repeat

允许元素设置多个背景图片

语法如下：

```css
background-repeat: repeat-x | repeat-y | repeat | no-repeat | space | round | [ <repeat-style> ]#
```

- **`repeat`**：默认值。背景图像在水平和垂直方向上都重复。
- **`repeat-x`**：仅在水平方向上重复。
- **`repeat-y`**：仅在垂直方向上重复。
- **`no-repeat`**：背景图像不重复。
- **`space`**：尽可能多地重复背景图像，然后在剩余空间内**均匀分布**（不会裁剪图像）。
- **`round`**：尽可能多地重复背景图像，并根据需要缩放图像以**填满元素。**

对于多背景图的情况，你可以这样指定不同的重复方式：

```css
.element {
  background-image: url(image1.png), url(image2.png);
  background-repeat: repeat, no-repeat;
}
```

在这个例子中，`image1.png` 将会在两个方向上重复 (`repeat`)，而 `image2.png` 将不会重复 (`no-repeat`)。

**注意事项**

- 如果你为 `background-repeat` 提供的值少于背景图的数量，最后一个值会被应用到所有的剩余背景图上。
- 同样地，如果只提供了一个值，那么这个设置将应用于所有背景图。

**实例**

假设我们有如下CSS代码：

```css
div {
  background-image: url('img1.png'), url('img/XMLSchema.png');
  background-repeat: no-repeat, repeat-y;
}
```

这里，`img1.png` 不会重复 (`no-repeat`)，而 `img/XMLSchema.png` 只在垂直方向上重复 (`repeat-y`)。

这种方式使你可以非常灵活地控制不同背景图的行为，以实现所需的视觉效果。





#### 列表属性

| CSS 属性名          | 功能               | 属性值                                                       |
| ------------------- | ------------------ | ------------------------------------------------------------ |
| list-style-type     | 设置列表符号       | - `none`：不显示标识<br> - `square`：实心方块<br> - `disc`：圆形<br> - `decimal`：数字<br> - `lower-roman`：小写罗马字<br> - `upper-roman`：大写罗马字<br> - `lower-alpha`：小写字母<br> - `upper-alpha`：大写字母 |
| list-style-position | 设置列表符号的位置 | - `inside`：在 li 内部<br> - `outside`：在 li 外部           |
| list-style-image    | 自定义列表符号     | `url(图片地址)`                                              |
| list-style          | 复合属性（简写）   | 同时设置 `list-style-type`、`list-style-position`、`list-style-image`（无顺序要求） |

**解释**

1. **list-style-type**

   - 控制列表项符号类型（如 `disc`、`decimal` 等），`none` 可隐藏符号。

2. **list-style-position**

   - `inside`：符号嵌入文本行内；`outside`：符号独立于文本左侧。

3. **list-style-image**

   - 通过 URL 替换默认符号为自定义图片（需确保图片路径有效）。

4. **list-style**

   - 简写属性，支持同时设置三种属性，顺序无关，如：

     ```css
     list-style: square inside url(icon.png);
     ```



#### 边框属性（其他元素也能用）

| CSS 属性名    | 功能         | 属性值                                                       |
| :------------ | ------------ | ------------------------------------------------------------ |
| border-width  | 边框宽度     | CSS 中可用的长度值                                           |
| border-color  | 边框颜色     | CSS 中可用的颜色值                                           |
| border-style  | 边框风格     | - `none` 默认值<br> - `solid` 实线<br> - `dashed` 虚线<br> - `dotted` 点线<br> - `double` 双实线 |
| border        | 边框复合属性 | 没有数量、顺序的要求                                         |
| border-radius | 边框圆角     |                                                              |
| outline       | 边框外轮廓   |                                                              |

注意：

1. 以上 4 个边框相关的属性，其他元素也可以用，这是我们第一次遇见它们。
2. 在后面的盒子模型中，我们会详细讲解边框相关的知识。



#### 表格独有属性

| CSS 属性名      | 功能                            | 属性值                                                       |
| --------------- | ------------------------------- | ------------------------------------------------------------ |
| table-layout    | 设置列宽度                      | - `auto`：自动，列宽根据内容计算（默认值）。<br> - `fixed`：固定列宽，平均分配。 |
| border-spacing  | 单元格间距                      | - CSS 长度值（如 `10px`）。<br> - 生效前提：单元格边框不合并。 |
| border-collapse | 合并单元格边框                  | - `collapse`：合并。<br> - `separate`：不合并（默认值）。    |
| empty-cells     | 控制空单元格显示                | - `show`：显示（默认值）。<br> - `hide`：隐藏。<br> - 生效前提：单元格不合并。 |
| caption-side    | 设置表格标题 (`<caption>`) 位置 | - `top`：标题在表格上方（默认值）。<br> - `bottom`：标题在表格下方。 |





#### 布局属性

------

##### 容器大小最值

**最小 `min-height` 属性**

- **定义**：指定一个元素的最小高度。即使内容较少，元素的高度也不会低于这个值。

- **语法**：

  ```css
  min-height: <length> | <percentage>;
  ```

  - `<length>`：可以使用绝对单位如`px`、`cm`等；也可以使用相对单位如`em`、`rem`。
  - `<percentage>`：相对于包含块的高度百分比。

- **示例**：

  ```css
  .container {
      min-height: 200px;
  }
  ```

  这个例子确保了`.container`类至少有200px的高度，但如果内容更多，则会自动扩展。

**应用场景**

- 确保容器有足够的空间来容纳其内容。
- 在响应式设计中，为不同屏幕尺寸提供一致的最低高度。

---

**最大`max-height` 属性**

- **定义**：指定一个元素的最大高度。如果内容超出这个高度，通常会触发滚动条（需结合`overflow`属性使用），或者内容被隐藏（取决于其他样式设置）。

- **语法**：

  ```css
  max-height: <length> | <percentage>;
  ```

  类似于`min-height`，但这里是设置最大值。

- **示例**：

  ```css
  .content-box {
      max-height: 400px;
      overflow-y: auto; /* 超出部分显示垂直滚动条 */
  }
  ```

  此示例限制了`.content-box`的高度不超过400px，超出部分可通过滚动查看。

**应用场景**

- 控制图片或文本区域的最大尺寸，防止页面布局因内容过多而破坏。
- 结合`overflow`属性实现优雅的内容溢出处理方案。

---

**组合使用**

- 使用`min-height`和`max-height`组合可以创建更灵活的高度范围：

  ```css
  .flexible-container {
      min-height: 150px;
      max-height: 500px;
      overflow-y: auto;
  }
  ```

  这样，`.flexible-container`将至少有150px高，并且最多不会超过500px，超出部分可通过滚动查看。

**注意事项**

- 当使用百分比作为`min-height`或`max-height`的值时，需要确保父元素有一个明确的高度，否则百分比可能无法正确计算。
- 在某些情况下，特别是对于表格单元格（`td`或`th`），这些属性可能不起作用或行为有所不同，因为表格布局有自己的规则。

通过合理使用`min-height`和`max-height`，可以极大地增强网页布局的灵活性和适应性，特别是在响应式设计和动态内容加载场景下。







##### 垂直对齐方式

属性名：vertical-align (va)

属性值：

| 属性值      | 适用场景                 | 效果描述                                                     |
| ----------- | ------------------------ | ------------------------------------------------------------ |
| baseline    | 默认值                   | 元素的基线与父元素的基线对齐                                 |
| top         | 行内/表格元素            | 元素顶部与行/单元格的最高元素顶部对齐                        |
| middle      | 行内/表格元素            | 元素中线与父元素的基线+0.5ex高度对齐（表格中表现为垂直居中） |
| bottom      | 行内/表格元素            | 元素底部与行/单元格的最低元素底部对齐                        |
| text-top    | 行内元素                 | 元素顶部与父元素字体的顶端对齐                               |
| text-bottom | 行内元素                 | 元素底部与父元素字体的底端对齐                               |
| sub         | 特殊文本                 | 模拟`<sub>`标签效果，将基线降低到合适位置                    |
| super       | 特殊文本                 | 模拟`<sup>`标签效果，将基线提升到合适位置                    |
| 长度值      | 精确调整（如2px, 0.5em） | 相对于基线向上（正值）或向下（负值）移动                     |
| 百分比值    | 相对行高调整             | 根据元素的line-height值计算移动距离（如50%）                 |

以下是对核心属性值的补充说明：

- **baseline**：文本类元素（如`<span>`）默认对齐方式，图片底部会与基线对齐
- **middle**：在表格单元格中可实现真正垂直居中，但在行内元素中可能受字体影响
- **top/bottom**：对齐依据是当前行框(line box)的最高/最低元素，而非容器边界
- **text-top/text-bottom**：对齐标准是父元素的字体尺寸，而非实际内容高度

###### 注意事项

1. 仅对以下元素有效：

   - 行内元素（`display: inline`）
   - 行内块元素（`display: inline-block`）
   - 表格单元格（`display: table-cell`）

2. 常见无效场景：

   - 块级元素（需改用flex/grid布局）
   - 绝对定位元素
   - 浮动元素

3. 图片对齐建议：

   ```css
   img {
     vertical-align: middle; /* 消除图片底部间隙 */
   }
   ```

4. 表格特殊行为：

   ```css
   td {
     vertical-align: middle; /* 单元格内容垂直居中 */
   }
   ```

###### 总结图示

```
[父元素]
│
├── text-top ──────┐
├── baseline ──────┤ ← 基线与父元素文字对齐
├── text-bottom ──┤
│                  ↓
│  [子元素]        → 可用长度/百分比值微调
└── line-height区域
```





#### 修饰属性



##### 过渡动画属性

属性名：transition (trs)

属性值（简写语法）：

```css
transition: <property> <duration> <timing-function> <delay>;
/*常用就是这样的*/
transition: all 1s;
```

> 本属性写于标签本身的css，不要写在类似于hover的css中

###### 详细属性分解表

| 子属性                     | 属性值示例                          | 默认值 | 作用描述                                           |
| -------------------------- | ----------------------------------- | ------ | -------------------------------------------------- |
| transition-property        | all, width, opacity                 | all    | 指定应用过渡的CSS属性（多个属性用逗号分隔）        |
| transition-duration        | 0.3s, 500ms                         | 0s     | 定义动画持续时间（必须指定至少该属性才会触发动画） |
| transition-timing-function | ease, cubic-bezier(.17,.67,.83,.67) | ease   | 控制动画速度曲线                                   |
| transition-delay           | 0.2s, 100ms                         | 0s     | 设置动画开始前的延迟时间                           |

###### 缓动函数详解表

| 函数值                | 运动曲线特征         | 典型应用场景         |
| --------------------- | -------------------- | -------------------- |
| ease                  | 先加速后减速（默认） | 通用动画效果         |
| linear                | 匀速运动             | 进度条、机械运动     |
| ease-in               | 逐渐加速             | 物体下落效果         |
| ease-out              | 逐渐减速             | 弹窗关闭效果         |
| ease-in-out           | 对称加减速           | 页面切换过渡         |
| cubic-bezier(n,n,n,n) | 自定义贝塞尔曲线     | 需要特殊节奏的动画   |
| steps(n)              | 分步跳跃变化         | 帧动画、数字切换效果 |

###### 注意事项

1. **生效前提**：

   - 元素必须具有有效可过渡属性（如尺寸/位置/颜色等）
   - 需要明确的属性值变化触发（如:hover状态切换）

2. **性能优化**：

   ```css
   /* 优先使用以下高性能属性 */
   transform: translate/scale/rotate;
   opacity: 0-1;
   filter: 简单效果;
   ```

3. **多属性控制**：

   ```css
   /* 同时控制多个属性的过渡 */
   .box {
     transition: 
       transform 0.3s ease-out,
       opacity 0.2s linear 50ms;
   }
   ```

4. **隐式动画关闭**：

   ```css
   /* 强制禁用所有过渡 */
   .no-transition {
     transition: none !important;
   }
   ```

###### 最佳实践示例

```css
/* 基础悬停效果 */
.button {
  transition: all 0.3s ease;
  background: #3498db;
}
.button:hover {
  background: #2980b9;
  transform: translateY(-2px);
}

/* 级联动画控制 */
.card {
  transition: 
    opacity 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94),
    transform 0.4s 0.1s ease-out;
}
.card.hidden {
  opacity: 0;
  transform: scale(0.9);
}
```

###### 总结图示

```
[动画时间轴]
│         ↗↘
│       ↗    ↘       ease-in-out曲线示例
│     ↗        ↘
│   ↗            ↘
├───┐              ┌───►
0  delay         duration
```



##### 透明度控制

属性名：opacity (opa)

属性值：

| 属性值      | 效果描述                     |
| ----------- | ---------------------------- |
| 0           | 完全透明（元素不可见）       |
| 0~1之间数值 | 半透明（如0.5表示50%透明度） |
| 1           | 完全不透明（默认值）         |

###### 核心特性说明

- **继承性**：不继承，但子元素会受父元素透明度影响（实际表现为叠加计算）
- **作用范围**：影响元素**及其所有子元素**的可见度
- **布局特性**：透明元素仍占据文档流空间（与`visibility: hidden`不同）
- **性能表现**：支持GPU加速，适合用于动画过渡

###### `opacity` 与 `rgba` 的区别？

- **`opacity`** 是一个属性，设置的是整个元素（包括元素里的内容）的不透明度。
- **`rgba`** 是颜色的设置方式，用于设置颜色，它的透明度，仅仅是调整颜色的透明度

###### 属性值详解

- **0**：

  - 元素完全透明，但依然可交互（可点击/聚焦）
  - 常用于实现淡出效果或无障碍隐藏

  ```css
  .hidden { opacity: 0; }
  ```

- **0~1之间数值**：

  - 实现元素半透明效果
  - 叠加计算公式：`最终透明度 = 父元素opacity * 当前元素opacity`

  ```css
  .translucent { opacity: 0.7; }
  ```

- **1**：

  - 默认状态，元素完全不透明
  - 常用于重置继承的透明状态

  ```css
  .reset-opacity { opacity: 1 !important; }
  ```

###### 注意事项

1. **交互保留**：

   ```css
   /* 透明元素仍可交互 */
   .ghost-button {
     opacity: 0.5;
     pointer-events: none; /* 需额外添加该属性禁用交互 */
   }
   ```

2. **叠加特性**：

   ```html
   <!-- 父元素opacity:0.5，子元素opacity:0.6 → 实际显示0.3 -->
   <div class="parent">
     <div class="child"></div>
   </div>
   ```

3. **与RGBA的区别**：

   ```css
   /* 仅影响背景透明度（不影响子元素） */
   .bg-transparent { background: rgba(0,0,0,0.5); }
   
   /* 影响整个元素及子元素 */
   .element-transparent { opacity: 0.5; }
   ```

4. **动画优化**：

   ```css
   /* 优先使用opacity实现淡入淡出 */
   .fade-in {
     transition: opacity 0.3s ease;
     opacity: 1;
   }
   ```

###### 应用场景示例

1. 基础淡入效果：

   ```css
   .fade {
     opacity: 0;
     transition: opacity 0.4s ease-in;
   }
   .fade.active {
     opacity: 1;
   }
   ```

2. 模态框遮罩层：

   ```css
   .overlay {
     position: fixed;
     top: 0;
     left: 0;
     width: 100%;
     height: 100%;
     background: black;
     opacity: 0.6;
   }
   ```

3. 加载状态提示：

   ```css
   .loading {
     opacity: 0.8;
     transition: opacity 0.2s;
   }
   .loading:hover {
     opacity: 1;
   }
   ```

###### 总结图示

```
透明度层级
┌───────────────┐
│  父元素opa:0.6│
│  ┌───────────┐│
│  │ 子元素opa:0.5 → 实际显示0.3 │
│  └───────────┘│
└───────────────┘
```





##### 滤镜修饰

属性名：filter

属性值：常用 filter 函数

| 滤镜函数          | 描述                                            | 示例                                                         |
| ----------------- | ----------------------------------------------- | ------------------------------------------------------------ |
| `blur(px)`        | 高斯模糊，值越大越模糊                          | `filter: blur(3px);`                                         |
| `brightness(%)`   | 调整亮度                                        | `filter: brightness(50%);`（变暗）<br>`filter: brightness(1.5);`（更亮） |
| `contrast(%)`     | 调整对比度                                      | `filter: contrast(200%);`（增强对比）                        |
| `grayscale(%)`    | 变成灰度图                                      | `filter: grayscale(100%);`（完全黑白）                       |
| `hue-rotate(deg)` | 色相旋转                                        | `filter: hue-rotate(90deg);`                                 |
| `invert(%)`       | 反转颜色                                        | `filter: invert(100%);`（负片效果）                          |
| `opacity(%)`      | 设置透明度（类似透明但不影响布局）              | `filter: opacity(50%);`                                      |
| `saturate(%)`     | 饱和度                                          | `filter: saturate(200%);`（更鲜艳）                          |
| `sepia(%)`        | 棕褐色调（老照片效果）                          | `filter: sepia(100%);`                                       |
| `drop-shadow()`   | 添加阴影（类似 box-shadow，但支持透明度和形状） | `filter: drop-shadow(2px 2px 4px rgba(0,0,0,0.5));`          |

------

💡 实际示例

1. 图片悬停模糊变清晰

```css
img {
  filter: blur(5px);
  transition: filter 0.3s ease;
}

img:hover {
  filter: blur(0);
}
```

2. 黑白图片 + 鼠标移上去恢复彩色

```css
img {
  filter: grayscale(100%);
  transition: filter 0.4s;
}

img:hover {
  filter: grayscale(0);
}
```

3. 创建“毛玻璃”（磨砂玻璃）效果

```css
.glass {
  background: url('bg.jpg');
  backdrop-filter: blur(10px); /* 注意：这是 backdrop-filter */
  filter: brightness(0.9) contrast(1.2);
}
```

> ⚠️ 注意：`backdrop-filter` 是另一个属性，作用于元素背后的区域（如半透明菜单），需要单独启用（部分浏览器需前缀）。

------

🌐 浏览器兼容性

- `filter` 属性在现代浏览器中支持良好（Chrome、Firefox、Safari、Edge）。

- 对于旧版 IE 不支持。

- Safari 需要

  ```
  -webkit-
  ```

  前缀（某些版本）：

  ```
  -webkit-filter: blur(2px);
          filter: blur(2px);
  ```

------

❗ 注意事项

1. **性能影响**：过度使用 `filter`（尤其是 `blur`）可能影响页面渲染性能，特别是在动画中。

2. 与 opacity 区别

   ：

   - `opacity: 0.5` 会让整个元素（包括子元素）变透明。
   - `filter: opacity(50%)` 只影响当前元素的绘制层，有时更适合做局部透明处理。

3. **硬件加速**：使用 `filter` 会触发 GPU 加速，有助于提升动画流畅度。

------

✅ 小技巧：结合 transform 使用，

```css
.card:hover {
  filter: brightness(1.1) saturate(120%);
  transform: scale(1.02);
  transition: all 0.3s ease;
}
```





##### 光标/鼠标样式控制

属性名：cursor  

属性值：  

| 属性值                  | 适用场景       | 效果描述                                  |
| ----------------------- | -------------- | ----------------------------------------- |
| default                 | 默认状态       | 浏览器默认光标（通常为箭头）              |
| pointer                 | 可点击元素     | 手形光标（常用于链接、按钮）              |
| text                    | 文本输入区域   | I形文本选择光标                           |
| move                    | 可拖拽元素     | 十字箭头（表示可移动）                    |
| wait                    | 加载等待状态   | 旋转圆圈/沙漏（表示系统繁忙）             |
| not-allowed             | 禁止操作       | 带斜杠的圆圈（表示当前操作不可用）        |
| crosshair               | 精准定位       | 十字线光标（用于绘图、测量工具）          |
| grab                    | 可抓取元素     | 手掌张开（表示可抓取，如拖拽视图）        |
| grabbing                | 抓取中状态     | 手掌闭合（表示正在抓取）                  |
| zoom-in / zoom-out      | 缩放操作       | 放大镜+“+”/“-”号（用于图片缩放控制）      |
| col-resize / row-resize | 调整列/行宽高  | 双向水平/垂直箭头（用于表格或分割线调整） |
| cell                    | 表格单元格选择 | 单元格选择框（类似Excel的光标）           |
| help                    | 帮助信息       | 箭头+问号（表示有额外说明）               |
| progress                | 后台处理中     | 箭头+旋转圆圈（表示进程运行但可交互）     |
| url()                   | 自定义光标     | 加载外部光标文件（需提供备用值）          |

---

 

- **pointer**：  
  浏览器中点击反馈的通用标识，建议与 `:hover` 状态配合使用：  

  ```css
  button:hover {
    cursor: pointer;
  }
  ```

- **grab系列**：  
  用于拖拽交互场景，需注意旧版浏览器可能显示为 `move`：  

  ```css
  .draggable {
    cursor: grab;
  }
  .draggable:active {
    cursor: grabbing;
  }
  ```

- **not-allowed**：  
  需同步禁用元素交互性以达到最佳效果：  

  ```css
  button:disabled {
    cursor: not-allowed;
    opacity: 0.6;
  }
  ```

- **自定义光标**：  
  支持 `.cur`、`.png` 等格式，需定义备用值：  

  ```css
  .magic-cursor {
    cursor: url('wand.cur'), url('wand.png'), auto;
  }
  ```

---

###### 注意事项  

1. **浏览器兼容性**：  

   - `grab`、`zoom-in` 等新特性需在CSS中提供备用值：  

     ```css
     .modern-cursor {
       cursor: grab;
       cursor: -webkit-grab; /* 旧版Webkit内核浏览器 */
     }
     ```

2. **无障碍设计**：  

   - 避免滥用特殊光标干扰用户认知  
   - 禁用状态需同时设置 `aria-disabled="true"`  

3. **性能优化**：  

   - 自定义光标文件建议小于32x32像素  
   - 避免对大面积元素使用复杂光标  

---

###### 应用场景示例  

1. 拖拽列表项：  

   ```css
   .list-item {
     cursor: move;
     transition: transform 0.2s;
   }
   .list-item:dragging {
     cursor: grabbing;
     opacity: 0.8;
   }
   ```

2. 图片缩放控制：  

   ```css
   .zoom-control {
     cursor: zoom-in;
   }
   .zoom-control.active {
     cursor: zoom-out;
   }
   ```

3. 自定义游戏光标：  

   ```css
   .game-canvas {
     cursor: url('sword.cur'), url('sword.png'), crosshair;
   }
   ```

---

###### 总结图示  

```
[光标类型映射]
┌───────────┬───────────────┐
│  default  │      →        │ 常规操作
│  pointer  │      →        │ 点击反馈
│  text     │      →        │ 文本输入
│  move     │      →        │ 拖拽移动
└───────────┴───────────────┘
```



###### **综合案例**

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



##### 删除项目符号

使用 `list-style:none` 删除项目符号

```html
<style></style>
.no-bullets {
    list-style: none; /* 移除所有列表项的项目符号 */
    padding-left: 0;  /* 可选：移除默认的内边距 */
}

/* 如果你需要对ol（有序列表）也进行相同的操作 */
.no-bullets ol {
    list-style: none;
}
</style>
<ul class="no-bullets">
    <li>项目 1</li>
    <li>项目 2</li>
    <li>项目 3</li>
</ul>
```





##### 线性渐变

- **基本语法**：

  ```css
  background: linear-gradient(direction, color-stop1, color-stop2, ...);
  ```

- **参数说明**：

  - **`direction`**：渐变的方向。可以是角度值（如 `45deg`）或关键字（如 `to top`, `to bottom`, `to left`, `to right`）。
  - **`color-stop`**：定义渐变中的颜色及其位置。格式为 `color position`，其中 `position` 是可选的，默认从 0% 开始。

- **常见用法**：

  - **从上到下**：

    ```css
    background: linear-gradient(to bottom, red, blue);
    ```

  - **从左到右**：

    ```css
    background: linear-gradient(to right, red, blue);
    ```

  - **带有颜色停止点**：

    ```css
    background: linear-gradient(to right, red 0%, yellow 50%, blue 100%);
    ```

  - **使用角度**：

    ```css
    background: linear-gradient(45deg, red, blue);
    ```



**repeating-linear-gradient() 函数用于重复线性渐变：**

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>重复渐变</title>
<style>
#grad1 {
  height: 200px;
  background-color: red; /* 浏览器不支持的时候显示 */
  background-image: repeating-linear-gradient(red, yellow 10%, green 20%);
    /* 这样在同一个大小的父元素重复的会更多 */
  background-image: repeating-linear-gradient(red, yellow 1%, green 5%);
}

#grad2 {
  height: 200px;
  background-color: red; /* 浏览器不支持的时候显示 */
  background-image: repeating-linear-gradient(45deg,red,yellow 7%,green 10%);
}

#grad3 {
  height: 200px;
  background-color: red; /* 浏览器不支持的时候显示 */
  background-image: repeating-linear-gradient(190deg,red,yellow 7%,green 10%);
}

#grad4 {
  height: 200px;
  background-color: red; /* 浏览器不支持的时候显示 */
  background-image: repeating-linear-gradient(90deg,red,yellow 7%,green 10%);
}
</style>
</head>
<body>

<h1>重复的线性渐变</h1>

<div id="grad1"></div>

<p>45deg:</p>
<div id="grad2"></div>

<p>190deg:</p>
<div id="grad3"></div>

<p>90deg:</p>
<div id="grad4"></div>

<p><strong>注意:</strong> Internet Explorer 9 及更早版本的 IE 浏览器不支持线性渐变。</p>

</body>
</html>
```

**通过修改每个首颜色和尾颜色的百分比而修改重复单位的基本大小**



##### 径向渐变

径向渐变由它的中心定义。

为了创建一个径向渐变，你也必须至少定义两种颜色结点。颜色结点即你想要呈现平稳过渡的颜色。同时，你也可以指定渐变的中心、形状（圆形或椭圆形）、大小。默认情况下，渐变的中心是 center（表示在中心点），渐变的形状是 ellipse（表示椭圆形），渐变的大小是 farthest-corner（表示到最远的角落）。

* 多个颜色之间的渐变，默认从圆心四散（不一定是正圆，要看容器本身宽高比）

```css
background-image: radial-gradient(red, yellow, green);
```

* 使用关键词调整渐变圆的圆心位置

```css
background-image: radial-gradient(at right top, red, yellow, green);
```

* 使用像素调整渐变圆的圆心位置

```css
background-image: radial-gradient(at 100px 50px, red, yellow, green);
```

* 调整渐变形状为正圆

```css
background-image: radial-gradient(circle, red, yellow, green);
```

* 调整形状的半径

```css
background-image: radial-gradient(100px, red, yellow, green);
background-image: radial-gradient(50px 100px, red, yellow, green);
```



**语法:**

background-image: radial-gradient(shape size at position, start-color, ..., last-color);

形状:ellipse（椭圆）/circle（圆形）

大小(半径)：属性值可用像素或关键字表示(圆形演示)

​        **closest-side**:圆心到距离最近的边

​        **farthest-side**:圆心到距离最远的边

​        **closest-corner**：圆心到距离最 近的角

​        **farthest-corner**：圆心到距离最远的角

发散方向：属性值可以为(at)left、right、top、bottom、center(可组合使用),像素百分比

起始颜色......

终止颜色......

**颜色结点均匀分布（默认情况下）**

颜色结点均匀分布的径向渐变：

```css
#grad { background-image: radial-gradient(red, yellow, green); }
```

**颜色结点不均匀分布**

颜色结点不均匀分布的径向渐变：

```css
#grad { background-image: radial-gradient(red 5%, yellow 15%, green 60%); }
```

**设置形状**

shape 参数定义了形状。它可以是值 circle 或 ellipse。其中，circle 表示圆形，ellipse 表示椭圆形。默认值是 ellipse。

形状为圆形的径向渐变：

```css
#grad { background-image: radial-gradient(circle at 100%, red, yellow, green); }
```



**不同尺寸大小关键字的使用**

size 参数定义了渐变的大小。它可以是以下四个值：

closest-side:圆心到距离最近的边

​    farthest-side:圆心到距离最远的边

​    closest-corner：圆心到距离最近的角

​    farthest-corner：圆心到距离最远的角

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>径向渐变尺寸</title>
<style>
#grad1 {
  height: 150px;
  width: 150px;
  background-color: red; /* 浏览器不支持的时候显示 */
  background-image: radial-gradient(closest-side at 60% 55%, red, yellow, black);
}

#grad2 {
  height: 150px;
  width: 150px;
  background-color: red; /* 浏览器不支持的时候显示 */
  background-image: radial-gradient(farthest-side at 60% 55%, red, yellow, black);
}

#grad3 {
  height: 150px;
  width: 150px;
  background-color: red; /* 浏览器不支持的时候显示 */
  background-image: radial-gradient(closest-corner at 60% 55%, red, yellow, black);
}

#grad4 {
  height: 150px;
  width: 150px;
  background-color: red; /* 浏览器不支持的时候显示 */
  background-image: radial-gradient(farthest-corner at 60% 55%, red, yellow, black);
}
</style>
</head>
<body>
<h3>径向渐变 - 不同尺寸大小关键字的使用</h3>
<p><strong>closest-side：</strong></p>
<div id="grad1"></div>
<p><strong>farthest-side：</strong></p>
<div id="grad2"></div>
<p><strong>closest-corner：</strong></p>
<div id="grad3"></div>

<p><strong>farthest-corner（默认）：</strong></p>
<div id="grad4"></div>

<p><strong>注意：</strong> Internet Explorer 9 及之前的版本不支持渐变。</p>

</body>
</html>
```



##### 重复径向渐变

**repeating-radial-gradient()** 函数用于重复径向渐变：

```css
#grad1 {height: 200px;background-image: repeating-radial-gradient(red, yellow 10%, green 15%);}
```



##### 字体霓虹灯

```html
<!DOCTYPE html>
<html lang="zh">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>霓虹灯文本效果</title>
    <style>
        body {
            background-color: #000; /* 背景颜色设置为黑色 */
            height: 100vh; /* 高度设置为视口高度的100% */
            margin: 0; /* 消除默认的外边距 */
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .neon-text {
            font-size: 72px; /* 字体大小设置为72像素 */
            background: linear-gradient(45deg, #ff00cc, #3333ff); /* 使用线性渐变背景 */
            background-clip: text; /* 将背景剪裁应用于文本 */
            color: transparent; /* 文本颜色设置为透明 */
            text-shadow: 0 0 10px rgba(255, 0, 204, 0.7), 0 0 20px rgba(255, 0, 204, 0.7), 0 0 30px rgba(255, 0, 204, 0.7); /* 添加多重阴影以模拟霓虹效果 */
        }
    </style>
</head>

<body>
    <!-- 应用霓虹灯文本效果 -->
    <span class="neon-text">你好，世界！</span>
</body>

</html>
```









### HTML 和 CSS之间的关系

父元素：**直接**包裹某个元素的元素，就是该元素的父元素

子元素：被父元素**直接**包含的元素

祖先元素：一直往上找，都是祖先，父元素也算祖先元素的一种，但一般都是父元素

后代元素：一直往下找，都是后代



#### 细说font-size

1. 由于字体设计原因，文字最终呈现的大小，并不一定与 `font-size` 的值一致，可能大，也可能小。例如：`font-size` 设为 `40px`，最终呈现的文字，可能比 `40px` 大，也可能比 `40px` 小。
2. 通常情况下，文字相对字体设计框，并不是垂直居中的，通常都靠下一些。





### 盒子模型

作用：布局网页，摆放盒子和内容，大概就是个容器

#### CSS中的常用的长度单位

1. `px`：像素。
2. `em`：相对元素 **`font-size`** 的倍数。
3. `rem`：相对**根字体**大小，html标签就是根。
4. `%`：相对父元素计算。
5. `vw`：**视口宽度**百分之多少  10vw就是视口宽度的10%     是可以随着视口大小的变化而变化的
6. `vh`：**视口高度**的百分之多少   10vh就是视口高度的10%    是可以随着视口大小的变化而变化的
7. `vmax`：视口宽高中大的那个百分之多少
8. `vmin`：视口宽高中小的那个百分之多少

**注意：**

CSS 中设置长度，必须加单位，否则样式无效！



#### 元素的显示模式

##### 块元素（block）

- **又称**：块级元素

- 特点

  1. 在页面中独占一行，不会与任何元素共用一行，是从上到下排列的。
  2. 默认宽度：撑满父元素。
  3. 默认高度：由内容撑开。
  4. 可以通过 CSS 设置宽高。

##### 行内元素（inline）

- **又称**：内联元素

- 特点

  1. 在页面中不独占一行，一行中不能容纳下的行内元素，会在下一行继续从左到右排列。
  2. 默认宽度：由内容撑开。
  3. 默认高度：由内容撑开。
  4. 无法通过 CSS 设置宽高。

##### 行内块元素（inline-block）

- **又称**：内联块元素

- 特点

  1. 在页面中不独占一行，一行中不能容纳下的行内元素，会在下一行继续从左到右排列。
  2. 默认宽度：由内容撑开。
  3. 默认高度：由内容撑开。
  4. 可以通过 CSS 设置宽高。

**注意：**

元素早期只分为：行内元素、块级元素，区分条件也只有一条：“是否独占一行”，如果按照这种分类方式，行内块元素应该算作行内元素。

**区分：**

**对比总结表**：

| 特性         | 块级元素         | 行内元素         | 行内块元素                                  |
| ------------ | ---------------- | ---------------- | ------------------------------------------- |
| 是否独占一行 | ✅ 是             | ❌ 否             | ❌ 否                                        |
| 排列方向     | 垂直（从上到下） | 水平（从左到右） | 水平（从左到右）                            |
| 可设置宽度   | ✅                | ❌                | ✅                                           |
| 可设置高度   | ✅                | ❌                | ✅                                           |
| 默认宽度     | 撑满父容器       | 由内容决定       | 由内容决定                                  |
| 默认高度     | 由内容决定       | 由内容决定       | 由内容决定                                  |
| 典型代表     | `<div>`, `<p>`   | `<span>`, `<a>`  | `<img>`, `<input>`, `display: inline-block` |

------

**实际应用建议**：

- 使用 **块级元素** 构建页面的主要结构（如布局容器、段落、标题等）。
- 使用 **行内元素** 包裹文本中的部分内容（如加粗、链接等）。
- 使用**行内块元素**实现水平排列的可控制尺寸的元素，比如：
  - 导航菜单项
  - 图标按钮
  - 图文混排布局

> 💡 提示：可以通过 `display` 属性在三种模式之间转换，例如：
>
> ```
> display: block;
> display: inline;
> display: inline-block;
> ```

掌握这三种显示模式的区别，是理解和实现CSS布局的基础。



#### 组成

盒子模型的重要组成部分：

- 内容区域 -content  width & height
- 内边距 - padding （出现在内容与盒子边缘之间）
- 边框线 - border（盒子的边框）
- 外边距 - margin (出现在盒子外面，盒子与外界的距离）

> 本质上这些都是属性，在对应选择器中书写即可
>
> 盒子的大小 = content + 左右 padding + 左右 border
>
> 外边距margin不会影响盒子的大小，但会影响盒子的位置



##### content内容区

**CSS 尺寸设置属性表**

| CSS属性名  | 功能                   | 属性值 |
| :--------- | :--------------------- | :----- |
| width      | 设置内容区域宽度       | 长度   |
| max-width  | 设置内容区域的最大宽度 | 长度   |
| min-width  | 设置内容区域的最小宽度 | 长度   |
| height     | 设置内容区域的高度     | 长度   |
| max-height | 设置内容区域的最大高度 | 长度   |
| min-height | 设置内容区域的最小高度 | 长度   |

**注意：**

- `max-width`、`min-width`一般不与 `width`一起使用。
- `max-height`、`min-height`一般不与 `height`一起使用。



###### 关于默认宽度

**所谓的默认宽度**，就是不设置width属性时，元素所呈现出来的宽度。

**总宽度** = 父的content - 自身的左右margin。

**内容区的宽度** = 父的content - 自身的左右margin - 自身的左右border - 自身的左右padding。



 

##### Padding内边距

作用：设置 内容 与 盒子边缘 之间的距离

设置的背景颜色会填充内边距 

属性名： padding / padding-方向名词

以下是代码示例：

```css
div{
    /*四个方向内边距相同*/
    padding: 30px;
    
    /*单独设置一个方向内边距*/
    padding-top: 10px;
    padding-bottom: 20px;
    padding-right: 30px;
    padding-left: 40px;
    
    width: 200px;
    height: 200px;
    background-color: pink;
    
}
```



> Padding内边距属性 会撑大盒子，比如设置 padding: 20px; 盒子会向外扩展20px出来

应用：在文本框中，可以用于文字与前边框的距离

![image-20250906175133715](./笔记/笔记/web-img/image-20250906175133715.png)

```css
    padding-left: 16px;
```



###### 多值写法

取值写法：

| 取值个数 | 示例                         | 含义                   |
| -------- | ---------------------------- | ---------------------- |
| 一个值   | padding: 10px                | 四个方向内边距均为10px |
| 四个值   | padding: 10px 20px 40px 80px | 上右下左               |
| 三个值   | padding: 10px 40px 80px      | 上 左右 下             |
| 两个值   | padding: 10px 80px           | 上下 左右              |





##### Border边框线

###### 全方向

作用：全方向添加一个边框线

设置的背景颜色会填充边框线

属性名：border（bd）

属性值：边框线粗细 线条样式 颜色（不区分顺序）

常用的线条样式

| 属性值 | 线条样式 |
| ------ | -------- |
| solid  | 实线     |
| dashed | 虚线     |
| dotted | 点线     |

> 此处只说明常用的三个属性值，并非只有这三个

 

```css
div{
    border: 1px solid black;
    /*三个参数分别为 边框线粗细 线条样式 颜色*/
}
```

 这段CSS代码将为盒子添加一个1px宽度 黑色 实线的盒子边框线

同时还可以单独设置单方向的边框线



去除选中边框可以使用 `outline:none;`



###### 单方向

属性名：border-方向名词（bd+方向名词首字母，例如，bdl）

属性值：边框线粗细 线条样式 颜色（不区分顺序）

方向名词表

| 属性名 | 方向 |
| ------ | ---- |
| top    | 顶部 |
| bottom | 底部 |
| right  | 右侧 |
| left   | 左侧 |



##### Margin外边距

作用：拉开两个盒子之间的距离

属性名：margin

提示：与 padding 属性值写法、含义相同

复合模式请参考padding

| CSS属性名     | 功能                                           | 属性值        |
| :------------ | :--------------------------------------------- | :------------ |
| margin-left   | 左外边距                                       | CSS中的长度值 |
| margin-right  | 右外边距                                       | CSS中的长度值 |
| margin-top    | 上外边距                                       | CSS中的长度值 |
| margin-bottom | 下外边距                                       | CSS中的长度值 |
| margin        | 复合属性，可以写1~4个值，规律同padding(顺时针) | CSS中的长度值 |



**注意：**

* 子元素的margin是参考父元素的content计算的
* 上margin、左margin会影响自身的位置，下margin、右margin会影响兄弟元素的位置
* 对于行内元素来说，左右的margin 是可以完美设置的，上下margin设置后是无效的
* 对于块级元素来说，margin的值也可以是auto，可以实现该元素在其父元素内水平居中
* margin的值可以是负值



> Margin外边距属性 会在盒子外面扩展一片空白，不会改变盒子的大小，但是位置变了
>
> PS：简单的来说，内边距相当于快递包裹里的填充物，外边距相当于箱子外面的快递包裹袋子



###### 版心居中(重要)

如果想要盒子页面居中，即使在不同尺寸与分辨率的页面也能居中，就添加 `Margin外边距属性` 并将值设置为 `auto`

```css
margin:0 auto
```





**注意！！注意！！**

**使用此方法需要盒子设置宽度，否则会跟随父级宽度，但是在某种意义上，也算是版心居中了**



###### margin的塌陷问题

**什么是 margin 塌陷？**

当两个垂直方向（上下）的盒子（比如兄弟元素或父子元素）的 margin 相遇时，它们不会叠加，而是会**“合并”成一个 margin**，取两者中较大的那个值。这种现象就叫 margin 塌陷。

###### **如何解决 margin 塌陷？**

1. **加隔离层**：比如给父元素加 `padding`或 `border`（例如 `border: 1px solid transparent`）。
2. **触发 BFC**：给父元素设置 `overflow: hidden`或 `display: flow-root`。
3. **用 Flex/Grid 布局**：这些布局方式不会塌陷。



###### margin合并问题

**什么是 margin 合并？**

上面兄弟元素的下外边距和下面兄弟元素的上外边距会合并，取一个最大的值，而不是相加。

**如何解决 margin 合并（塌陷）？**

无需解决，布局的时候上下的兄弟元素，只给一个设置上下外边距就可以了。



###### 区别

`margin` 的**塌陷问题**（Margin Collapse）和**合并问题**其实指的是同一个现象，即 **“外边距合并”**（Margin Collapse），中文里有时会因翻译或理解不同而出现“塌陷”或“合并”的说法。但在标准的 CSS 术语中，正确的说法是 **“外边距合并”**（Margin Collapse）。

不过，为了澄清你的疑问，我们可以从两个角度来理解这个现象的不同表现形式：

------

✅ 正确认知：**“塌陷”和“合并”是同一现象的不同描述**

- **“合并”**：强调两个 margin **叠加在一起**，但不是相加，而是取**最大值**。
- **“塌陷”**：多用于描述父子元素之间 margin 表现“塌陷”到父元素外部，给人一种“塌下去”的视觉错觉。

所以，**它们不是两种不同的问题，而是同一问题在不同场景下的表现**。

------

📌 外边距合并（Margin Collapse）发生的三种典型场景

1. **相邻兄弟元素之间的 margin 合并**

两个**垂直排列的兄弟元素**，上下 margin 会合并。

```css
<div class="box1">Box 1</div>
<div class="box2">Box 2</div>
```

```css
.box1 { margin-bottom: 20px; }
.box2 { margin-top: 30px; }
```

👉 实际间距不是 `20 + 30 = 50px`，而是取最大值：**30px**。

------

2. **父子元素之间的 margin 塌陷（常被称作“塌陷”）**

当**子元素的 margin-top** 与**父元素的内容区域**接触时，margin 会“向上溢出”，导致父元素整体向下移动，看起来像是父元素的 margin 塌陷了。

```css
<div class="parent">
  <div class="child">Child</div>
</div>
```

```css
.parent {
  width: 200px;
  height: 200px;
  background: lightblue;
  /* 没有 padding 或 border */
}
.child {
  margin-top: 30px;
  height: 50px;
  background: coral;
}
```

👉 你期望子元素距离父元素顶部 30px，但结果是**整个父元素被往下推了 30px**。这就是所谓的“margin 塌陷”。

✅ **解决方法**：

- 给父元素添加 `padding-top: 1px;`
- 给父元素添加 `border: 1px solid transparent;`
- 使用 `overflow: hidden;`（推荐）
- 使用 `display: flex;` 或 `display: grid;`（Flexbox/Grid 不会发生 margin collapse）

------

3. **空元素自身的上下 margin 合并**

一个没有内容、没有 padding、没有 border 的块级元素，其自身的 `margin-top` 和 `margin-bottom` 会合并成一个 margin。

```css
.empty {
  margin-top: 20px;
  margin-bottom: 30px;
  /* height: 0; 且无内容 */
}
```

👉 最终 margin 高度为 30px（取最大值）。

------

✅ **总结**：区别？其实没有本质区别！

| 说法            | 含义说明                                                 |
| --------------- | -------------------------------------------------------- |
| **margin 合并** | 标准术语，指垂直方向相邻 margin 合并为一个，取最大值     |
| **margin 塌陷** | 特指**父子元素间**的 margin 合并现象，视觉上像“塌下去”了 |

👉 所以：

- **“合并”是通用术语**（适用于兄弟、空元素、父子）
- **“塌陷”是特例描述**（多用于父子关系）

------

✅ 如何避免 margin 合并/塌陷？

1. 使用 `padding` 或 `border` 隔开父子元素
2. 父元素设置 `overflow: hidden`
3. 使用 Flexbox / Grid 布局（默认不合并）
4. 使用 `display: inline-block`
5. 使用 CSS 逻辑间距（如 `gap`）



#### 尺寸计算

相邻元素外边距相同时会碾压，不同时采用大值

- 默认情况

盒子尺寸 = 内容尺寸 + border尺寸 + 内边距尺寸

现在有一案例，要求设计的盒子是200*200，因为border和padding会撑大，目前解决方法有两种

解决方法

- 手动减法：减掉 border 与 padding 的尺寸，自己算
- 内减模式：box-sizing: border-box 直接卸载属性中，浏览器自己会减去

#### box-sizing

`box-sizing: border-box`； `width`和`height`包含`border`和`padding`的值，不会再额外增加

就是说，所写的`width`和`height`是盒子的总宽高

让你设定的 `width` 和 `height` 成为元素在页面上**实际占据的空间大小**，内边距和边框会“吃掉”内容区域的空间，而不是增加总尺寸。

使用 `box-sizing` 属性可以设置盒模型的两种类型。

| 可选值      | 含义                                                         |
| ----------- | ------------------------------------------------------------ |
| content-box | `width` 和 `height` 设置的是盒子内容区的大小。（默认值）     |
| border-box  | `width` 和 `height` 设置的是盒子总大小。（怪异盒模型） 内容区+padding+border |



#### resize（了解）

要和 overflow 配合使用

使用 `resize` 属性可以控制是否允许用户**调节元素尺寸**。

| 值         | 含义                               |
| ---------- | ---------------------------------- |
| none       | 不允许用户调整元素大小。（默认值） |
| both       | 用户可以调节元素的宽度和高度。     |
| horizontal | 用户可以调节元素的宽度。           |
| vertical   | 用户可以调节元素的高度。           |





#### 元素溢出

谁是容器，就在谁身上加属性

作用：控制溢出元素的内容的显示方式

属性名：overflow

属性值

| 属性值    | 说明                             |
| :-------- | :------------------------------- |
| `visible` | 显示，默认值                     |
| `hidden`  | 隐藏                             |
| `scroll`  | 显示滚动条，不论内容是否溢出     |
| `auto`    | 自动显示滚动条，内容不溢出不显示 |

**注意**：

1. `overflow-x`、`overflow-y`不能一个是 `hidden`，一个是 `visible`，是实验性属性，不建议使用。

​    2.`overflow`常用的值是 `hidden`和 `auto`，除了能处理溢出的显示方式，还可以解决很多疑难杂症。

tag: 超出 裁切 隐藏 溢出



#### 隐藏元素的两种方式

可以少写点代码

###### **方式一：visibility 属性**

`visibility`属性默认值是 `show`（应为 `visible`），如果设置为 `hidden`，元素会隐藏。

元素看不见了，还占有原来的位置（元素的大小依然保持）。

###### **方式二：display 属性**

设置 `display: none`，就可以让元素隐藏。

彻底地隐藏，不但看不见，也不占用任何位置，没有大小宽高。



#### 样式的继承

**核心概念：**

有些样式会继承。元素如果本身设置了某个样式，就使用本身设置的样式；但如果本身没有设置某个样式，会从父元素开始一级一级继承（优先继承离得近的祖先元素）。

**方式一：visibility 属性**

`visibility`属性默认值是 `show`（应为 `visible`），如果设置为 `hidden`，元素会隐藏。

元素看不见了，还占有原来的位置（元素的大小依然保持）。

**方式二：display 属性**

设置 `display: none`，就可以让元素隐藏。

彻底地隐藏，不但看不见，也不占用任何位置，没有大小宽高。

##### **会继承的 CSS 属性**

- 字体属性 (如 `font-family`, `font-size`)
- 文本属性 (除了 `vertical-align`)
- 文字颜色 (如 `color`)

------

##### **不会继承的 CSS 属性**

- 边框 (如 `border`)
- 背景 (如 `background`)
- 内边距 (如 `padding`)
- 外边距 (如 `margin`)
- 宽高 (如 `width`, `height`)
- 溢出方式 (如 `overflow`)

##### **核心规律**

一个规律：能继承的属性，都是不影响布局的，简单说：都是和盒子模型没关系的。



#### 元素的默认样式

**元素一般都有些默认的样式，例如：**

1. **`<a>`元素：**
   - 下划线
   - 字体颜色
   - 鼠标小手（光标样式）
2. **`<h1>`～ `<h6>`元素：**
   - 文字加粗
   - 文字大小
   - 上下外边距
3. **`<p>`元素：**
   - 上下外边距
4. **`<ul>`、`<ol>`元素：**
   - 左内边距
5. **`body`元素：**
   - 8px外边距（4个方向）

------

**优先级说明：**

**元素的默认样式 > 继承的样式**

因此，如果要重置元素的默认样式，选择器**一定要直接选择到该元素**。



#### 清除默认样式

作用：清楚标签默认的样式，比如：默认的内边距

常用的方法是 通配符选择器

```css
*{
    margin: 0;
    pading: 0;
    box-sizing: border-box;
}
```



#### 布局的小技巧

**1. 行内元素、行内块元素的对齐特性**

行内元素、行内块元素，可以被父元素当做文本处理。

即：可以像处理文本对齐一样，去处理行内、行内块元素在父元素中的对齐。

例如：使用 `text-align`、`line-height`、`text-indent`等属性。

------

**2. 如何让子元素在父元素中水平居中**

- **若子元素为块元素：** 给**子元素**加上 `margin: 0 auto;`。
- **若子元素为行内元素、行内块元素：** 给**父元素**加上 `text-align: center;`。

------

**3. 如何让子元素在父元素中垂直居中**

- **若子元素为块元素：** 给**子元素**加上 `margin-top`，其值为：`(父元素content高度 - 子元素盒子总高度) / 2`。
- **若子元素为行内元素、行内块元素：**
  1. 让**父元素**的 `height`值等于 `line-height`值。
  2. 给**每个子元素**都加上 `vertical-align: middle;`。
     - **补充：** 若想实现绝对垂直居中，可以将父元素的 `font-size`设置为 `0`。



#### 元素之间的空白问题

原因：行内元素、行内块元素，彼此之间的换行会被浏览器解析为一个空白字符

解决方法：

1. 别换行（不咋地）
2. 给父元素设置 font-size：0；，在给需要显示文字的元素，单独设置字体大小（推荐）



#### 行内块之间的幽灵空白问题

![image-20250905141743070](./笔记/笔记/web-img/image-20250905141743070.png)

**行内块元素与文本对齐问题**

**1. 产生原因**

行内块元素与文本的基线对齐，而文本的基线与文本最底端之间是有一定距离的。

**2. 解决方案**

- **方案一：** 给行内块元素设置 `vertical-align`属性，值不为 `baseline`即可（例如设置为 `middle`、`bottom`、`top`均可）。
- **方案二：** 若父元素中只有一张图片，设置图片为 `display: block`。
- **方案三：** 给父元素设置 `font-size: 0`。如果该行内块内部还有文本，则需单独为文本设置 `font-size`。



#### :heavy_exclamation_mark: 圆角与阴影

##### 圆角

###### 基础用法

作用：设置元素的外边框为圆角

属性名：border-radius

属性值：数字+px / 百分比

多值写法：左上角 右上角 右下角 左下角

提示：属性值是圆角半径，数字越大越圆，越小越尖

> 单独写是四个角相同的圆角大小，可以通过给属性添加多个值以达到控制每个角弧度的效果
>
> 关于记忆的顺序的方法：从左上角顺时针赋值，没有取值的角与对角取值相同

在 CSS3 中，使用 `border-radius` 属性可以将盒子变为圆角。

- **同时设置四个角的圆角：**

  ```css
  border-radius: 10px;
  ```

- **分开设置每个角的圆角（几乎不用）：**

| 属性名                       | 作用                                                         |
| ---------------------------- | ------------------------------------------------------------ |
| `border-top-left-radius`     | 设置左上角圆角半径：<br>1. 一个值是正圆半径。<br>2. 两个值分别是椭圆的 x 半径、y 半径。 |
| `border-top-right-radius`    | 设置右上角圆角半径：<br>1. 一个值是正圆半径。<br>2. 两个值分别是椭圆的 x 半径、y 半径。 |
| `border-bottom-right-radius` | 设置右下角圆角半径：<br>1. 一个值是正圆半径。<br>2. 两个值分别是椭圆的 x 半径、y 半径。 |
| `border-bottom-left-radius`  | 设置左下角圆角半径：<br>1. 一个值是正圆半径。<br>2. 两个值分别是椭圆的 x 半径、y 半径。 |

- 分开设置每个角的圆角，综合写法（几乎不用）：

  ```css
  border-radius: 左上角x 右上角x 右下角x 左下角x / 左上角y 右上角y 右下角y 左下角y
  ```

- **一个值**：所有四个角都应用相同的圆角半径。

- **两个值**：第一个值应用于左上角和右下角，第二个值应用于右上角和左下角。

- **三个值**：第一个值应用于左上角，第二个值应用于右上角和左下角，第三个值应用于右下角。

- **四个值**：顺时针方向从左上角开始，依次是左上、右上、右下、左下。

###### 常见应用

正圆形状

前提是盒子本身就是正方形的，给盒子设置圆角属性值为 宽高的一半 / 50%

写法：有两种，一种是算出来设置，一种是直接设置为50%

```css
img{
    width: 200px;
    height: 200px;
    
    /*在本案例中，他俩的最终效果是一样的，百分比比的是盒子宽高*/
    border-radius: 100px;
    border-radius: 50%;
}
```

> 效果大概就是圆形头像的样子，在一个盒子中，最大值为50%，再大就没效果了





胶囊形状

前提是盒子本身是长方形，给盒子设置圆角属性值为 盒子高度的一半

写法：`Talk is cheap Show me the code`

```css
div{
    width: 200px;
    height: 80px;
    background-color: orange;
    
    border-radius: 40px;
}
```





##### 阴影效果

在 CSS 中，主要有两种阴影：

1. **盒子阴影（box-shadow）** → 给盒子元素加阴影（最常用）
2. **文字阴影（text-shadow）** → 给文字加阴影

作用：给元素设置阴影效果

###### 盒子阴影效果

属性名：box-shadow

属性值： X轴偏移量 Y轴偏移量 模糊半径 扩散半径 颜色 内外阴影

```css
 box-shadow: 5px 5px 12px #ffffff ,
                -5px -5px 12px #c8d0e7;

```

使用 `box-shadow` 属性为盒子添加阴影。

**内阴影**（阴影在元素内部）

加 `inset` 关键字：

```css
input {
    box-shadow: inset 0 2px 5px rgba(0,0,0,0.2);
}
```

✅ 常用于输入框、凹陷按钮等。

**多重阴影**（叠加多个阴影）

用逗号分隔多个阴影：

```css
.button {
    box-shadow: 
        0 2px 5px rgba(0,0,0,0.2),
        0 4px 10px rgba(0,0,0,0.1);
}
```

👉 层层叠加，更真实立体。



各个值的含义：

| 值       | 含义                                 |
| -------- | ------------------------------------ |
| h-shadow | 水平阴影的位置，必须填写，可以为负值 |
| v-shadow | 垂直阴影的位置，必须填写，可以为负值 |
| blur     | 可选，模糊距离                       |
| spread   | 可选，阴影的外延值                   |
| color    | 可选，阴影的颜色                     |
| inset    | 可选，将外部阴影改为内部阴影         |

默认值：

- `box-shadow: none` 表示没有阴影



注意：

- X轴偏移量 和 Y轴偏移量 是必须指
- 默认是外阴影，内阴影需要添加 inset 属性 直接在后面加上就行了

> 其实吧，他是个复合属性，义眼顶针了，对吧。



###### 文字阴影效果

**基础文字阴影**

```css
h1 {
    text-shadow: 2px 2px 5px rgba(0,0,0,0.5);
}
```

👉 文字有立体感，适合深色背景上的标题。

**发光文字效果**

```css
.glow {
    text-shadow: 0 0 10px #fff, 0 0 20px #fff, 0 0 30px #00f;
}
```

✅ 常用于科技感、霓虹灯风格

文字阴影不支持内阴影



#### 边框外轮廓

outline

- `outline-width`：外轮廓的宽度。

- `outline-color`：外轮廓的颜色。

- `outline-style`：外轮廓的风格。

  - `none`：无轮廓
  - `dotted`：点状轮廓
  - `dashed`：虚线轮廓
  - `solid`：实线轮廓
  - `double`：双线轮廓

- `outline-offset` 设置**外轮廓与边框的距离**，正负值都可以设置。

   

  **注意**：`outline-offset` 不是 `outline` 的子属性，是一个独立的属性。

- `outline` 复合属性

  ```css
  outline: 50px solid blue;
  ```



#### 盒子模型问题合集



##### 外边距合并现象

场景：垂直排列的兄弟元素，上下 margin 会合并

现象：取两个 margin 中的 **较大值** 生效

> 大概就是大的margin覆盖了小的，看不到了而已



##### 外边距塌陷问题

场景：父子级的标签，当父级没有内容时，子级的添加 **上外边距** 会产生塌陷问题

现象：导致父级一起向下移动

> 大概就是父级没有内容，子级的内容继承上去了，两个盒子合成一个盒子，使用外边距会导致两个盒子一起移动，看起来就像是给大盒子设置了上外边距

解决方法：

- 取消子级margin，父级设置padding，同时设置box-sizing: border-box 就能保证整个父级标签大小不变
- 父级设置 overflow: hidden
- 父级设置 border-top
- 给父级随便写点内容



##### 内外边距问题

场景：行内元素添加 margin 和 padding，无法改变元素垂直位置

解决方法：给行内元素添加 line-height(行高) 可以改变垂直位置

> 

```css
span{
    /*无法改变垂直位置*/
    margin: 50px;
    padding: 20px;
    
    /*无法改变垂直位置*/
    line-height: 100px;
}
```



### 浮动  

在最初，浮动是用来实现文字环绕图片效果的，现在浮动是主流的页面布局方式之一

作用：让块元素水平排列

属性值：float

属性值：

- left：左对齐，将出现在父级的最左边
- right：右对齐，将出现在父级的最右边

特点：顶对齐，具备行内块显示模式的特点，浮动后脱离标准流的控制，有可能出现重合



#### 浮动的特点

1. **脱离标准文档流**。（不好）
2. 无论浮动前是什么元素，浮动后都具有以下特性：
   - 默认的宽度和高度均由内容撑开（尽可能小）。
   - 可以显式地设置宽度(`width`)和高度(`height`)。
3. **不会独占一行**，可以与其他元素共用一行。
4. **不会发生 margin 合并，也不会发生 margin 塌陷**，能够完美地设置四个方向的 `margin`和 `padding`。
5. **不会像行内块元素一样被当做文本处理**（因此没有行内块元素的空白间隙问题）。



#### 浮动后会有哪些影响

对兄弟元素的影响：对后面的兄弟元素，会占据浮动元素之前的位置，在浮动元素下面，对前面的兄弟无影响

对父元素的影响：不能撑起父元素的高度，导致父元素高度塌陷，但父元素的宽度依然束缚浮动的元素



#### 清除浮动

场景：浮动元素会脱标，如果父级没有高度，子级无法撑开父级高度（可能导致布局错乱）

结局方法：清除浮动（清除浮动带来的影响）

方法一：

- 在父级元素内容的最后添加一个块级元素，设置 CSS 属性  `clear:both`

> 通常都将清除浮动的 CSS 的类名设置为 `clearfix` 

方法二：单伪元素法

```css
.clearfix::after{
    content:"";
    display: block;
    clear: both;
}
```

| 属性  | 说明                                                         |
| ----- | ------------------------------------------------------------ |
| clear | 指定不允许元素周围有浮动元素。left：在左侧不允许浮动元素。right：在右侧不允许浮动元素。both： 在左右两侧均不允许浮动元素。None  默认值。允许浮动元素出现在两侧。 |

“float是魔鬼，会影响其他相邻元素；但是clear是小白，其只会影响自身，不会对其他相邻元素造成影响！”

元素盒子的边不能和前面的浮动元素相邻，那么就是自己下移。



浮动的本质作用还是实现图文混排的效果





### 定位



父相子绝



#### 定位属性

position 属性用于指定一个元素在文档中的定位方式。

position 属性的五个值：

|    值    |   效果   |
| :------: | :------: |
|  static  | 静态定位 |
| relative | 相对定位 |
|  fixed   | 固定定位 |
| absolute | 绝对定位 |
|  sticky  | 粘性定位 |



#### 相对定位

 **1.如何设置相对定位？**

- 给元素设置 `position: relative;`即可实现相对定位。
- 可以使用 `left`、`right`、`top`、`bottom`四个属性调整位置。

**2. 相对定位的参考点在哪里？**

- 相对自己原来的位置。

**3。 相对定位的特点：**

1. **不会脱离文档流**，元素位置的变化只是视觉效果上的变化，**不会对其他元素产生任何影响**。

2. 定位元素的显示层级比普通元素高，无论什么定位，显示层级都是一样的。

   **默认规则是：**

   - 定位的元素会盖在普通元素之上。
   - 都发生定位的两个元素，后写的元素会盖在先写的元素之上。

3. `left`和 `right`不能一起设置，`top`和 `bottom`不能一起设置。

4. 相对定位的元素也能继续浮动，但**不推荐**这样做。

5. 相对定位的元素也能通过 `margin`调整位置，但**不推荐**这样做。

**注意：**

绝大多数情况下，相对定位会与绝对定位配合使用。



- **保留文档流**：元素仍占据原始空间，周围元素布局不受影响。

- **定位基准**：相对于**自身原始位置**进行偏移。

- **定位方式**：通过 `top`, `right` 等属性微调位置（如 `left: 20px` 向右移动20像素）。

- **应用场景**：微调元素位置、作为绝对定位子元素的定位基准，子级绝对定位，父级相对定位（子绝对父相对）

- **示例**：

  ```css
  .box {
    position: relative;
    top: 10px; /* 从原位置向下移动10px */
    left: 20px; /* 从原位置向右移动20px */
  }
  ```







#### 绝对定位

**1 如何设置绝对定位？**

- 给元素设置 `position: absolute;`即可实现绝对定位。
- 可以使用 `left`、`right`、`top`、`bottom`四个属性调整位置。

------

**2 绝对定位的参考点在哪里？**

- 参考它的**包含块**。

**什么是包含块？**

1. 1.

   对于**没有脱离文档流**的元素：包含块就是父元素。

2. 2.

   对于**脱离文档流**的元素：包含块是第一个拥有**定位属性**（`position`值非 `static`）的祖先元素（如果所有祖先都没定位，那包含块就是整个页面）。

------

**3 绝对定位元素的特点**

1. 1.

   **脱离文档流**，会对后面的兄弟元素、父元素有影响。

2. 2.

   `left`和 `right`不能一起设置，`top`和 `bottom`不能一起设置。

3. 3.

   绝对定位、浮动不能同时设置，如果同时设置，**浮动失效**，以定位为主。

4. 4.

   绝对定位的元素，也能通过 `margin`调整位置，但**不推荐**这样做。

5. 5.

   无论是什么元素（行内、行内块、块级）设置为绝对定位之后，都变成了**定位元素**。

**何为定位元素？**

- 默认宽、高都被内容所撑开，且能自由设置宽高。

 



**元素可以使用的顶部，底部，左侧和右侧属性定位。**然而，这些属性无法工作，除非是先设定position属性(static除外)。他们也有不同的工作方式，这取决于定位方法。

| 属性     | 说明                                                         |
| -------- | ------------------------------------------------------------ |
| position | 指定元素的定位类型。<br><br/>static HTML 元素的默认值，即没有定位，遵循正常的文档流对象。静态定位的元素不会受到 top, bottom, left, right影响。<br><br/>absolute  绝对定位的元素的位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于```<html>```。absolute 定位使元素的位置与文档流无关，因此不占据空间。absolute 定位的元素和其他元素重叠。<br><br/>fixed  元素的位置相对于浏览器窗口是固定位置。即使窗口是滚动的它也不会移动：Fixed定位使元素的位置与文档流无关，因此不占据空间。Fixed定位的元素和其他元素重叠。     <br><br/>relative  相对定位元素的定位是相对其正常位置。移动相对定位元素，但它原本所占的空间不会改变。<br><br/>sticky  sticky 英文字面意思是粘，粘贴，所以可以把它称之为粘性定位。**position: sticky;** 基于用户的滚动位置来定位。粘性定位的元素是依赖于用户的滚动，在 position:relative 与 position:fixed 定位之间切换。它的行为就像 <br/><br/>position:relative; 而当页面滚动超出目标区域时，它的表现就像 position:fixed;，它会固定在目标位置。元素定位表现为在跨越特定阈值前为相对定位，之后为固定定位。这个特定阈值指的是 top, right, bottom 或 left 之一，换言之，指定 top, right, bottom 或 left 四个阈值其中之一，才可使粘性定位生效。否则其行为与相对定位相同。 |
| right    | 定义了定位元素右外边距边界与其包含块右边界之间的偏移。       |
| top      | 定义了一个定位元素的上外边距边界与其包含块上边界之间的偏移。 |
| bottom   | 定义了定位元素下外边距边界与其包含块下边界之间的偏移。       |
| left     | 定义了定位元素左外边距边界与其包含块左边界之间的偏移。       |





**案例：**

```html
    <style>
        /* 通用样式 */
        body {
            font-family: Arial, sans-serif;
            padding: 20px;
        }

        .box {
            width: 100px;
            height: 100px;
            margin: 10px;
            color: white;
        }

        /* static 定位 */
        .static {
            position: static;
            background-color: #3498db;
        }

        /* relative 定位 */
        .relative {
            position: relative;
            left: 50px;
            top: 20px;
            background-color: #2ecc71;
        }

        /* absolute 定位 */
        .parent {
            position: relative;
            width: 300px;
            height: 200px;
            border: 1px solid #ccc;
            margin: 20px;
        }

        .absolute {
            position: absolute;
            right: 20px;
            bottom: 20px;
            background-color: #e74c3c;
        }

        /* fixed 定位 */
        .fixed {
            position: fixed;
            top: 20px;
            right: 20px;
            background-color: #f39c12;
        }

    </style>
</head>

<body>
    <!-- static 定位示例 -->
    <h2>static 定位</h2>
    <p>元素默认的定位方式，按照正常的文档流进行布局。</p>
    <div class="box static">Static</div>

    <!-- relative 定位示例 -->
    <h2>relative 定位</h2>
    <p>元素相对于其正常位置进行偏移，仍占据原文档流中的空间。</p>
    <div class="box relative">Relative</div>

    <!-- absolute 定位示例 -->
    <h2>absolute 定位</h2>
    <p>元素相对于最近的已定位祖先元素进行定位，如果没有已定位的祖先元素，则相对于文档的初始包含块。</p>
    <div class="parent">
        <div class="box absolute">Absolute</div>
    </div>

    <!-- fixed 定位示例 -->
    <h2>fixed 定位</h2>
    <p>元素相对于浏览器窗口进行定位，滚动页面时元素位置不变。</p>
    <div class="box fixed">Fixed</div>


    <!-- 用于产生滚动效果 -->
    <div style="height: 1000px;"></div>
</body>
```

**粘性定位实例:**

```html
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
```



------





#### **固定定位**

**3.1 如何设置为固定定位？**

- 给元素设置 `position: fixed;`即可实现固定定位。
- 可以使用 `left`、`right`、`top`、`bottom`四个属性调整位置。

------

**3.2 固定定位的参考点在哪里？**

- 参考它的**视口**。

**什么是视口？**

- 对于PC浏览器来说，视口就是我们看网页的那扇“窗户”。

------

**3.3 固定定位元素的特点**

1. **脱离文档流**，会对后面的兄弟元素、父元素有影响。
2. `left`和 `right`不能一起设置，`top`和 `bottom`不能一起设置。
3. 固定定位和浮动不能同时设置，如果同时设置，**浮动失效**，以固定定位为主。
4. 固定定位的元素，也能通过 `margin`调整位置，但**不推荐**这样做。
5. 无论是什么元素（行内、行内块、块级）设置为固定定位之后，都变成了**定位元素**。

**何为定位元素？**

- 默认宽、高都被内容所撑开，且能自由设置宽高。



- **脱离文档流**：元素不再占据原始空间，后续元素会填补其位置。

- **定位基准**：相对于**浏览器窗口**，不随页面滚动而移动。

- **定位方式**：通过 `top`, `right`, `bottom`, `left` 指定偏移量来确定元素在视口中的具体位置。

- **应用场景**：创建固定的导航栏、返回顶部按钮、悬浮广告等需要在页面滚动时保持可见的界面元素。

- **示例**：

  ```css
  .fixed-element {
    position: fixed;
    bottom: 0; /* 固定在视窗底部 */
    right: 0; /* 固定在视窗右侧 */
    padding: 10px; /* 可选：为元素添加内边距 */
    background-color: white; /* 可选：设置背景颜色 */
    border: 1px solid #ccc; /* 可选：设置边框 */
  }
  ```

---

这种格式清晰地展示了固定定位的关键点和应用实例，有助于理解和记忆。固定定位是网页设计中非常实用的一种布局技术，特别适合用于实现那些需要持续对用户可见的UI组件。



```css
    position: fixed;
    top: 0px;
    z-index: 1000;    // 让固定定位的元素完全显示
```



---



**关键区别总结**

| 特性           | 绝对定位 (`absolute`)            | 相对定位 (`relative`)    |
| -------------- | -------------------------------- | ------------------------ |
| **文档流**     | 脱离文档流，不占空间             | 保留文档流，占据原空间   |
| **定位基准**   | 最近的已定位祖先元素或 `<body>`  | 自身原始位置             |
| **常见用途**   | 覆盖元素、模态框、精准定位       | 微调位置、创建定位上下文 |
| **父元素要求** | 需要父元素设置非 `static` 的定位 | 无特殊要求               |

---

**注意事项**

1. **层叠顺序**：定位元素可通过 `z-index` 控制堆叠层级，默认是0，其值越大越靠上。
2. **父容器限制**：绝对定位元素需父元素设置 `position: relative`（或其他非 `static` 值）以限制其定位范围。
3. **布局影响**：绝对定位可能导致内容重叠，需谨慎处理响应式布局中的尺寸问题。



#### 粘性定位

**4.1 如何设置为粘性定位？**

- 给元素设置 `position: sticky;`即可实现粘性定位。
- 可以使用 `left`、`right`、`top`、`bottom`四个属性调整位置，**不过最常用的是 `top`值**。

------

**4.2 粘性定位的参考点在哪里？**

- 离它最近的一个拥有 **“滚动机制”** 的祖先元素，即便这个祖先不是最近的真实可滚动祖先。

------

**4.3 粘性定位元素的特点**

1. 1.

   **不会脱离文档流**，它是一种专门用于窗口滚动时的新的定位方式。

2. 2.

   最常用的值是 `top`值。

3. 3.

   粘性定位和浮动可以同时设置，但**不推荐**这样做。

4. 4.

   粘性定位的元素，也能通过 `margin`调整位置，但**不推荐**这样做。

**核心特点总结：**

**粘性定位和相对定位的特点基本一致，不同的是：粘性定位可以在元素到达某个位置时将其固定。**



**定义**：

- **粘性定位** (`position: sticky;`) 是一种特殊的定位方式，它结合了相对定位和固定定位的优点。

**特性**：

- 元素默认按照文档流进行布局（相对定位）。
- 当页面滚动到某个预设的阈值时，元素会“固定”在指定位置（固定定位）。

**语法**：

```css
.sticky-element {
    position: sticky;
    top: 10px; /* 阈值，当元素距离视窗顶部10px时变为固定定位 */
}
```

**关键属性**：

- `position: sticky;`：声明元素使用粘性定位。
- `top`, `bottom`, `left`, `right`：定义元素变为固定定位的阈值。最常用的是`top`。

**示例**：

```html
<style>
    .sticky {
        position: sticky;
        top: 10px;
        background-color: #f1f1f1;
        padding: 10px;
        border: 2px solid #ddd;
    }
</style>

<div style="height: 1500px;">
    <div class="sticky">我是粘性定位的元素</div>
    <p>这里是一些页面内容。</p>
</div>
```

**应用场景**：

- **导航栏**：让导航栏在用户滚动页面时固定在屏幕顶部，方便用户操作。
- **侧边栏**：让侧边栏在用户滚动页面时固定在屏幕一侧，便于访问相关内容。
- **目录**：在长篇文章中，使目录部分固定在屏幕一侧，方便用户快速跳转。

**注意事项**：

- 粘性定位元素需要有一个具有滚动机制的父级容器，否则它的粘性效果不会生效。
- 在一些较老的浏览器版本中可能不支持`position: sticky;`，因此在实际项目中使用时需要注意兼容性问题。

---

通过合理利用粘性定位，你可以创建出既美观又实用的网页布局，提升用户的交互体验。希望这份笔记能帮助你更好地理解并应用粘性定位。



#### 定位的层级

1. 

   **定位元素的层级更高**：

   定位元素（无论何种定位）的显示层级比普通元素高，且所有定位类型的默认显示层级都一样。

2. 

   **默认的重叠规则**：

   如果发生位置重叠，默认后面的元素会显示在前面元素之上。

3. 

   **使用 `z-index`控制层级**：

   可以通过 CSS 属性 `z-index`来调整元素的显示层级。

4. 

   **`z-index`的属性值**：

   `z-index`的值是数字（没有单位），**数字越大，显示层级越高**。

5. 

   **`z-index`的生效条件**：

   **只有定位的元素**（即设置了 `position`且值非 `static`的元素）设置 `z-index`才会生效。

6. 

   **调试提示**：

   如果 `z-index`值大的元素没有覆盖值小的元素，请检查其**包含块**的层级。

##### **Z-index** 

是 CSS 中用于控制元素在堆叠上下文（stacking context）中的层级顺序的属性。它决定了当多个元素重叠时，哪个元素会显示在前面或后面。理解 `z-index` 的工作原理对于创建复杂的布局和确保界面元素按预期显示非常重要。

**基本概念**

- **堆叠顺序（Stacking Order）**：页面上的每个元素都有一个默认的堆叠顺序。默认情况下，后面的元素会在视觉上覆盖前面的元素。
- **Z-index 属性**：通过设置 `z-index` 属性，可以改变元素的堆叠顺序。值越大，元素越靠前；值越小，元素越靠后。默认值为 `auto`，即元素遵循其自然堆叠顺序。



```
.element {
    z-index: 1; /* 设置元素的堆叠层级 */
}
```



**使用方法**

- **数值范围**：`z-index` 可以接受正整数、负整数和 `auto`。较大的正值会使元素显示在前面，而较大的负值会使元素显示在后面。

  css

  深色版本

  

  ```
  .front {
      z-index: 10;
  }
  
  .back {
      z-index: -1;
  }
  ```

- **必须结合定位使用**：为了使 `z-index` 生效，元素必须具有以下任一定位属性：

  - `position: relative;`
  - `position: absolute;`
  - `position: fixed;`
  - `position: sticky;`

  css

  深色版本

  

  ```
  .element {
      position: relative;
      z-index: 1;
  }
  ```



**堆叠上下文（Stacking Context）**

- **堆叠上下文** 是指一组元素的堆叠顺序被独立管理的情况。一个新的堆叠上下文可以通过以下方式创建：
  - 根元素 (`<html>`)
  - `position` 值为 `absolute` 或 `relative` 且 `z-index` 不是 `auto`
  - `position` 值为 `fixed` 或 `sticky`
  - 元素具有 `opacity` 小于 1
  - 元素具有 `transform` 不是 `none`
  - 等等...
- 在同一个堆叠上下文中，`z-index` 的值决定元素的显示顺序。而在不同的堆叠上下文中，子元素的 `z-index` 只在其父级堆叠上下文中有效。



#### 定位的特殊应用

**注意：**

1. 1.

   发生**固定定位**、**绝对定位**后，元素都变成了**定位元素**，默认宽高被内容撑开，且依然可以设置宽高。

2. 2.

   发生**相对定位**后，元素依然是之前的显示模式。

3. 3.

   以下所说的特殊应用，只针对**绝对定位**和**固定定位**的元素，**不包括相对定位**的元素。

------

**让定位元素的宽/高充满包含块**

- **宽度与包含块一致**：给定位元素同时设置 `left: 0;`和 `right: 0;`。
- **高度与包含块一致**：给定位元素同时设置 `top: 0;`和 `bottom: 0;`。

------

**让定位元素在包含块中居中**

**方案一：**

```css
left: 0;
right: 0;
top: 0;
bottom: 0;
margin: auto;
```

**方案二：使用负外边距实现定位元素居中**

通过计算，先将元素左上角移动至包含块中心点，再通过负外边距将元素拉回，实现元素中心与包含块中心对齐。

**CSS代码方案：**

```css
left: 50%;
top: 50%;
margin-left: -宽度值的一半;
margin-top: -高度值的一半;
```

**重要注意事项：**

⚠️ **该定位的元素必须设置宽高！！！** ⚠️





### 布局

#### 版心

**1. 定义**

在PC端网页中，一般都会有一个**固定宽度**且**水平居中**的盒子，来显示网页的主要内容，这个盒子就是网页的**版心**。

**2. 版心宽度**

版心的宽度一般在 **960~1200像素** 之间（图中用红色圆圈特别强调了此范围，并单独标注了数字 **900** 作为示例）。

**3. 数量**

版心可以是一个，也可以是多个。



#### 常用类名

| 位置                   | 对应名词（CSS 类名常用）     |
| :--------------------- | :--------------------------- |
| **顶部导航条**         | `topbar`                     |
| **页头**               | `header`, `page-header`      |
| **导航**               | `nav`, `navigator`, `navbar` |
| **搜索框**             | `search`, `search-box`       |
| **横幅、广告、宣传图** | `banner`                     |
| **主要内容**           | `content`, `main`            |
| **侧边栏**             | `aside`, `sidebar`           |
| **页脚**               | `footer`, `page-footer`      |



### 重置默认样式

**HTML 元素的默认样式**

很多元素都有默认样式，例如：

1. **`<p>`元素**：有默认的上下 `margin`。
2. **`<h1>`~ `<h6>`元素**：有默认的上下 `margin`，并且字体加粗。
3. **`<body>`元素**：有默认的 `8px`外边距。
4. **超链接 (`<a>`)**：有默认的文字颜色和下划线。
5. **`<ul>`元素**：有默认的左 `padding`。
6. ……

------

**为何需要重置默认样式？**

在早期，这些默认样式为快速创建简单页面提供了便利。但在现代追求精细设计的复杂网页中，这些默认样式不仅会带来麻烦，而且在不同的浏览器中表现可能不一致。因此，我们需要将它们“重置”。

------

##### **方案一：使用全局选择器**

通过 CSS 全局选择器 (`*`) 来清除所有元素的默认外边距和内边距。

**CSS 代码：**

```css
* {
    margin: 0;
    padding: 0;
}
```

**评价：**

- 在简单案例中可以临时使用。
- **实际开发中不推荐使用**，原因：
  1. `*`会选择所有元素，但并非所有元素都有默认样式。
  2. 重置时通常需要做特定处理（例如：想让 `<a>`元素的文字是灰色，其他元素文字是蓝色）。

------

##### **方案二：reset.css**

**原理：**

选择具有默认样式的元素，清空其默认样式。

**效果：**

经过 reset 后的网页，好似“一张白纸”，开发人员可根据设计稿，精细地去添加具体的样式。

------

##### **方案三：Normalize.css**

**原理：**

一种最新方案，在清除默认样式的基础上，**保留了一些有价值的默认样式**。

**官方网站：**

http://necolas.github.io/normalize.css/

**相对于 reset.css 的优点：**

1. 保护了有价值的默认样式，而不是完全去掉它们。
2. 为大部分HTML元素提供一般化的样式
3. 新增对HTML5元素的设置
4. 对并集选择器的使用比较谨慎，有效避免调试工作杂乱

* 备注：

**Normalize.css 的重置，和 reset.css 相比，更加的温和，开发时可根据实际情况进行选择。**





### 字体图标

在网页设计中，字体图标是一种使用字体文件来显示图标的特殊技术。它们实际上是基于矢量的图形，可以无损地缩放到任意大小，并且可以通过CSS轻松调整其样式。以下是关于字体图标的一些关键点和应用示例。

---

#### **字体图标（Icon Fonts）**

- **矢量图形**：字体图标是基于矢量的，这意味着它们可以无损地缩放到任意大小，非常适合响应式设计。

- **易于修改**：由于字体图标本质上是文本字符，因此可以通过CSS轻松调整其颜色、大小、阴影等属性，就像操作普通文本一样简单。

- **轻量化**：相比图片图标，字体图标通常具有更小的文件大小，并且只需加载一次即可在整个网站中复用，有助于提高网页加载速度。

- **兼容性好**：字体图标支持所有现代浏览器，包括移动设备上的浏览器，同时在不同操作系统上也有一致的表现。

- **常见字体图标库**：
  - **Font Awesome**
  - **Material Icons**
  - **Ionicons**

---

#### **阿里巴巴 Iconfont 使用指南**

**注册并登录**

1. 访问 [Iconfont](https://www.iconfont.cn/) 并注册一个账号（如果还没有的话），然后登录。
2. 搜索和收藏图标，并将它们添加到您的项目中。

**创建项目并管理图标**

1. 在项目页面中，点击“下载至本地”，选择合适的格式（如 `Symbol` 或 `Font class`）进行下载。
2. 将下载的文件解压，并引入到您的项目中。

**下载为 Symbol（SVG Sprite）**

```html
<head>
  <script src="./path/to/iconfont.js"></script>
  <style>
    .icon {
      width: 1em;
      height: 1em;
      vertical-align: -0.15em;
      fill: currentColor;
      overflow: hidden;
    }

    .custom-icon {
      font-size: 200px;
      color: brown;
    }
  </style>
</head>
<body>
  <!-- 使用 Iconfont 图标 -->
  <svg class="icon custom-icon" aria-hidden="true">
    <use xlink:href="#icon-kuandai"></use>
  </svg>
</body>
```

**下载为 Font class**

```html
<head>
  <link rel="stylesheet" href="./path/to/iconfont.css">
  <style>
    .custom-icon {
      font-size: 200px;
      color: brown;
    }
  </style>
</head>
<body>
  <!-- 使用 Iconfont 图标 -->
  <i class="iconfont icon-kuandai custom-icon"></i>
</body>
```



##### 注意

建议根据随下载的指导文档或参考以下代码

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Icon Example</title>
    <style>
        @font-face {
            font-family: 'iconfont';
            src: url('./icon/iconfont.ttf'),
                url('./icon/iconfont.woff2'),
                url('./icon/iconfont.woff');
        }

        .iconfont {
            font-family: "iconfont" !important;
            font-size: 16px;
            font-style: normal;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        .webpaper {
            font-size: 200px;
            /* color:cyan; */
        }
    </style>
</head>

<body>
    <span class="iconfont webpaper">&#xe991;</span>
</body>

</html>
```



#### **总结**

字体图标极大地简化了网页设计中的图标管理，使得开发者能够更加高效地创建美观且功能强大的用户界面。无论是简单的导航栏图标还是复杂的交互元素，字体图标都是一个非常实用的选择。

- **Font Awesome** 提供了丰富的图标集和便捷的集成方式，适合快速开发和原型设计。
- **阿里巴巴 Iconfont** 提供了更多的自定义选项和灵活的集成方式，特别适合国内开发者使用。





### 动画属性

#### 2D变换

前提：二维坐标系如下图所示

------

##### 1. 2D位移

**traslate**

2D位移可以改变元素的位置，具体使用方式如下：

1. 先给元素添加转换属性 `transform`。
2. 编写 `transform` 的具体值，相关可选值如下：

| 值           | 含义                                                         |
| ------------ | ------------------------------------------------------------ |
| `translateX` | 设置水平方向位移，需指定长度值；若指定的是百分比，是参考自身宽度的百分比。 |
| `translateY` | 设置垂直方向位移，需指定长度值；若指定的是百分比，是参考自身高度的百分比。 |
| `translate`  | 一个值代表水平方向，两个值代表：水平和垂直方向。             |

1. 注意点：

   1. 位移与相对定位很相似，都不脱离文档流，不会影响到其它元素。

   2. 与相对定位的区别：相对定位的百分比值，参考的是其父元素；定位的百分比值，参考的是其自身。

   3. 浏览器针对位移有优化，与定位相比，浏览器处理位移的效率更高。

   4. `transform`可以链式编写，例如：

      ```css
      transform: translateX(30px) translateY(40px);
      ```

   5. 位移对行内元素无效。

   6. 位移配合定位，可实现元素水平垂直居中

      ```css
      .box {
          position: absolute;
          left: 50%;
          top: 50%;
          transform: translate(-50%, -50%);
      }
      ```

##### 2. 2D缩放

**scale**

缩放是指：让元素放大或缩小，具体使用方式如下：

1. 先给元素添加转换属性 `transform`。
2. 编写 `transform` 的具体值，相关可选值如下：

| 值       | 含义                                                         |
| -------- | ------------------------------------------------------------ |
| `scaleX` | 设置水平方向的缩放比例，值为一个数字，1 表示不缩放，大于 1 放大，小于 1 缩小。 |
| `scaleY` | 设置垂直方向的缩放比例，值为一个数字，1 表示不缩放，大于 1 放大，小于 1 缩小。 |
| `scale`  | 同时设置水平方向、垂直方向的缩放比例，一个值代表同时设置水平和垂直缩放；两个值分别代表：水平缩放、垂直缩放。 |

* 注意点：

1. `scale` 的值，是支持写负数的，但几乎不用，因为容易让人产生误解。
2. 借助缩放，可实现小于 12px 的文字。

##### 3. 2D旋转

**rotate**

旋转是指：让元素在二维平面内，顺时针旋转或逆时针旋转，具体使用方式如下：

1. 先给元素添加转换属性 `transform`。
2. 编写 `transform` 的具体值，相关可选值如下：

| 值       | 含义                                                         |
| -------- | ------------------------------------------------------------ |
| `rotate` | 设置旋转角度，需指定一个角度值 (deg)，正值顺时针，负值逆时针。 |

注意：`rotateZ(20deg)` 相当于 `rotate(20deg)`，当然到了 3D 变换的时候，还能写：`rotate(x, x, x)`

##### 4.  2D扭曲（了解）

**skew**

扭曲是指：让元素在二维平面内被“拉扯”，进而“走形”。实际开发几乎不用，了解即可，具体使用方式如下：

1. 先给元素添加转换属性 `transform`。
2. 编写 `transform` 的具体值，相关可选值如下：

| 值      | 含义                                                         |
| ------- | ------------------------------------------------------------ |
| `skewX` | 设置元素在水平方向扭曲，值为角度值，会将元素的左上角、右下角拉扯。 |
| `skewY` | 设置元素在垂直方向扭曲，值为角度值，会将元素的左上角、右下角拉扯。 |
| `skew`  | 一个值代表 `skewX`，两个值分别代表：`skewX`、`skewY`         |

##### 5.  2D多重变换

多个变换，可以同时使用一个 `transform` 来编写。

```css
transform: translate(-50%, -50%) rotate(45deg);
```

注意点：多重变换时，建议最后旋转。

##### 6.  变换原点

**transform-origin**

- 元素变换时，默认的原点是元素的中心，使用 `transform-origin` 可以设置变换的原点。
- 修改变换原点对位移没有影响，对旋转和缩放会产生影响。
- 如果提供两个值，第一个用于横坐标，第二个用于纵坐标。
- 如果只提供一个，若是像素值，表示横坐标，纵坐标取 50%；若是关键词，则另一个坐标取 50%。
  * `transform-origin: 50% 50%;` 变换原点在元素的中心位置，百分比是相对于自身。——默认值
  * `transform-origin: left top;` 变换原点在元素的左上角。
  * `transform-origin: 50px 50px;` 变换原点距离元素左上角 50px 50px 的位置。
  * `transform-origin: 0;` 只写一个值的时候，第二个值默认为 50%。



#### 3D变换

##### 1.   3D空间与景深

* 开启3D空间

  `transform-style` 

重要原则：元素进行 3D 变换的首要操作：**父元素**必须开启 3D 空间！

使用 `transform-style` 开启 3D 空间，可选值如下：

1. `flat`：让子元素位于此元素的二维平面内（2D 空间）——默认值
2. `preserve-3d`：让子元素位于此元素的三维空间内（3D 空间）

* 设置景深

  `perspective`

何为景深？——指定观察者与 z=0 平面的距离，能让发生 3D 变换的元素，产生透视效果，看来更加立体。

使用 `perspective` 设置景深，可选值如下：

1. `none`：不指定透视——（默认值）

2. 长度值：指定观察者距离 z=0 平面的距离，不允许负值。

注意：`perspective` 设置给发生 3D 变换元素的父元素！

##### 2.   透视点的位置

所谓透视点位置，就是观察者位置；默认的透视点在元素的中心。

使用 `perspective-origin` 设置观察者位置（透视点的位置），例如：

```css
/* 相对坐标轴向右偏移400px，往下偏移300px（相当于人蹲下300像素，然后向右移动400像素看元素）*/
perspective-origin: 400px 300px;
```

注意：通常情况下，我们不需要调整透视点位置。

##### 3.   3D位移

**translate**

3D 位移是在 2D 位移的基础上，可以让元素沿 z 轴位移，具体使用方式如下：

1. 先给元素添加转换属性 `transform`。
2. 编写 `transform` 的具体值，3D 相关可选值如下：

| 值            | 含义                                                         |
| ------------- | ------------------------------------------------------------ |
| `translateZ`  | 设置 z 轴位移，需指定长度值，正值向屏幕外，负值向屏幕里，且不能写百分比。 |
| `translate3d` | 第 1 个参数对应 x 轴，第 2 个参数对应 y 轴，第 3 个参数对应 z 轴，且均不能省略。 |

#####  4.   3D旋转

**rotate**

3D 旋转是在 2D 旋转的基础上，可以让元素沿 x 轴和 y 轴旋转，具体使用方式如下：

1. 先给元素添加转换属性 `transform`。
2. 编写 `transform` 的具体值，3D 相关可选值如下：

| 值         | 含义                                                         |
| ---------- | ------------------------------------------------------------ |
| `rotateX`  | 设置 x 轴旋转角度，需指定一个角度值 (deg)，面对 x 轴正方向：正值顺时针，负值逆时针。 |
| `rotateY`  | 设置 y 轴旋转角度，需指定一个角度值 (deg)，面对 y 轴正方向：正值顺时针，负值逆时针。 |
| `rotate3d` | 前 3 个参数分别表示坐标轴：x, y, z，第 4 个参数表示旋转的角度，参数不允许省略。<br>例如：`transform: rotate3d(1,1,1,30deg)`，意思是：x、y、z 分别旋转 30 度。 |

##### 5.  3D缩放

3D缩放是在2D缩放的基础上，可以让元素沿z轴缩放。

使用方式

1.先给元素添加转换属性`transform`。

2.编写`transform`的具体值，3D相关可选值如下：

* **`scaleZ`**：设置z轴方向的缩放比例，值为一个数字，1表示不缩放，大于1放大，小于1缩小。

- **`scale3d`**：第1个参数对应x轴，第2个参数对应y轴，第3个参数对应z轴，参数不允许省略。

##### 6.   3D的多重变换

多个变换,可以同时使用一个 transform 来编写。

```css
transform: translateZ(100px) scaleZ(3) rotateY(40deg);
```

> 注意点:多重变换时,建议最后旋转。

##### 7.  背部可见性

**backface-visibility**

在使用 CSS 3D 变换（比如 `transform: rotateY(180deg)`或 `rotateX()`等）时，一个元素实际上是有 **正面（front face）和背面（back face）** 的，就像一张卡片有正反两面。

默认情况下：

- **正面**：是你正常书写和看到的那一面（通常是元素初始状态）。
- **背面**：是当元素绕某个轴（如 Y 轴）翻转 180 度后你看到的那一面。

`backface-visibility`的作用

该属性决定了：**当元素的背面朝向用户时，是否显示这个背面。**

语法：

```css
backface-visibility: visible | hidden;
```

取值：

- **`visible`（默认值）**：即使元素的背面朝向用户，也依然可见。也就是说，你可以看到元素的“背面”。
- **`hidden`**：如果元素的背面朝向用户，则这个背面**不可见**（相当于隐藏了）。常用来实现“翻转卡片”只显示正面的效果。





#### 过渡

##### 使用

过渡可以在不使用 Flash 动画，不使用 JavaScript 的情况下，让元素从一种样式，平滑过渡为另一种样式。

1. **transition-property**

- **作用**：定义哪个属性需要过渡，只有在该属性中定义的属性（比如宽、高、颜色等）才会以有过渡效果。
- 常用值
  1. `none`：不过渡任何属性。
  2. `all`：过渡所有能过渡的属性。
  3. 具体某个属性名，例如：`width`、`height`，若有多个以逗号分隔。

不是所有的属性都能过渡，值为数字，或者值能转为数字的属性，都支持过渡，否则不支持过渡。常见的支持过渡的属性有：颜色、长度值、百分比、`z-index`、`opacity`、2D 变换属性、3D 变换属性、阴影。

2. **transition-duration**

- **作用**：设置过渡的持续时间，即：一个状态过渡到另外一个状态耗时多久。

- 常用值

  1. `0`：没有任何过渡时间——默认值。
  2. `s` 或 `ms`：秒或毫秒。
  3. 列表：
     - 如果想让所有属性都持续一个时间，那就写一个值。
     - 如果想让每个属性持续不同的时间那就写一个时间的列表。

  ```css
      <style>
  
          .box1 {
              width: 200px;
              height: 200px;
              background-color: #676767;
              /* 设置哪个属性需要过度 */
              /* transition-property: background-color, height, width; */
              /* 让能过渡的元素都过渡 */
              transition-property: all;
              /* 设置过渡时间 */
              transition-duration: 2s;
  
          }
  
          .box1:hover {
              background-color: aqua;
              height: 100px;
              width: 100px;
          }
      </style>
  </head>
  
  <body>
      <div class="box1"></div>
  </body>
  
  ```

  **淡入淡出效果（最常用）**
  
  ```css
  .hidden-content {
      opacity: 0;
      visibility: hidden;
      transition: opacity 0.3s ease, visibility 0.3s ease;
  }
  
  .parent:hover .hidden-content {
      opacity: 1;
      visibility: visible;
  }
  ```
  
  > ✅ 效果：内容平滑淡入淡出
  >  💡 `visibility` 确保元素完全隐藏时不占用布局空间

3.  **transition-delay**

- **作用**：指定开始过渡的延迟时间，单位：s 或 ms。

4.  **transition-timing-function**

- **作用**：设置过渡的类型。
- 常用值
  1. `ease`：平滑过渡——默认值。
  2. `linear`：线性过渡。
  3. `ease-in`：慢 → 快。
  4. `ease-out`：快 → 慢。
  5. `ease-in-out`：慢 → 快 → 慢。
  6. `step-start`：等同于 `steps(1, start)`。
  7. `step-end`：等同于 `steps(1, end)`。
  8. `steps(integer, ?)`：接受两个参数的步进函数。第一个参数必须为正整数，指定函数的步数。第二个参数取值可以是 `start` 或 `end`，指定每一步的值发生变化的时间点。第二个参数默认值为 `end`。
  9. `cubic-bezier(number, number, number, number)`：特定的贝塞尔曲线类型。

在线制作贝塞尔曲线：https://cubic-bezier.com/



##### 复合属性

如果设置了一个时间，表示 `duration`；如果设置了两个时间，第一个是 `duration`，第二个是 `delay`；其他值没有顺序要求。

```css
transition: 1s 1s linear all;
```

transition: 属性 时长 速度曲线 延迟;



#### 动画

##### 基本使用 

1. 什么是帧

- 一段动画，就是一段时间内连续播放 n 个画面。每一张画面，我们管它叫做“帧”。一定时间内连续快速播放若干个帧，就成了人眼中所看到的动画。同样时间内，播放的帧数越多，画面看起来越流畅。

2. 什么是关键帧

- 关键帧指的是，在构成一段动画的若干帧中，起到决定性作用的 2-3 帧。



**第一步：定义关键帧（定义动画）**

1. 简单方式定义：

```css
/*写法一*/
@keyframes 动画名 {
    from {
        /*property1:value1*/
        /*property2:value2*/
    }
    to {
        /*property1:value1*/
    }
}
```

2. 完整方式定义：

```css
@keyframes 动画名 {
    0% {
        /*property1:value1*/
    }
    20% {
        /*property1:value1*/
    }
    40% {
        /*property1:value1*/
    }
    60% {
        /*property1:value1*/
    }
    80% {
        /*property1:value1*/
    }
    100% {
        /*property1:value1*/
    }
}
```

第二步：给元素应用动画，用到的属性如下：

1. `animation-name`：给元素指定具体的动画（具体的关键帧）
2. `animation-duration`：设置动画所需时间
3. `animation-delay`：设置动画延迟

```css
.box {
    /* 指定动画 */
    animation-name: testKey;
    /* 设置动画所需时间 */
    animation-duration: 5s;
    /* 设置动画延迟 */
    animation-delay: 0.5s;
}
```



##### 其他属性

动画属性详解

* `animation-timing-function`，设置动画的类型，常用值如下：

1. `ease`：平滑动画 —— 默认值
2. `linear`：线性过渡
3. `ease-in`：慢 → 快
4. `ease-out`：快 → 慢
5. `ease-in-out`：慢 → 快 → 慢
6. `step-start`：等同于 `steps(1, start)`
7. `step-end`：等同于 `steps(1, end)`
8. `steps(integer, ?)`：接受两个参数的步进函数。第一个参数必须为正整数，指定函数的步数。第二个参数取值可以是 `start` 或 `end`，指定每一步的值发生变化的时间点。第二个参数默认值为 `end`。
9. `cubic-bezier(number, number, number, number)`：特定的贝塞尔曲线类型。

* `animation-iteration-count`，指定动画的播放次数，常用值如下：

1. `number`：动画循环次数
2. `infinite`：无限循环

*  `animation-direction`，指定动画方向，常用值如下：

1. `normal`：正常方向（默认）
2. `reverse`：反方向运行
3. `alternate`：动画先正常运行再反方向运行，并持续交替运行
4. `alternate-reverse`：动画先反运行再正方向运行，并持续交替运行

* `animation-fill-mode`，设置动画之外的状态

1. `forwards`：设置对象状态为动画结束时的状态
2. `backwards`：设置对象状态为动画开始时的状态

* `animation-play-state`，设置动画的播放状态，常用值如下：

1. `running`：运动（默认）
2. `paused`：暂停



##### 复合属性

```css
animation-name
animation-duration
animation-delay

animation-timing-function
animation-iteration-count
animation-direction
animation-fill-mode
animation-play-state
```

* `animation-name  `      

​	**动画名称**
​	 作用：指定你要使用的**关键帧动画的名字**。这个名字必须和 `@keyframes 动画名` 中定义的	名	字一致。

 	示例：`animation-name: slideIn;` 表示使用名为 `slideIn` 的关键帧动画。

* `animation-duration`

  动画持续时间

 作用：设置动画从开始到结束需要多长时间。

 单位：秒（`s`）或毫秒（`ms`）。

 示例：`animation-duration: 2s;` 表示动画持续 2 秒。

* `animation-timing-function`
  **动画时间函数 / 缓动效果**
  作用：控制动画在**时间上的播放节奏**，比如是匀速、先快后慢，还是分步跳转。
  常见值：
  1. `ease`：慢开始，快中间，慢结束（默认）
  2. `linear`：匀速播放
  3. `ease-in`：慢开始，快结束
  4. `ease-out`：快开始，慢结束
  5. `ease-in-out`：慢快慢
  6. `steps(3, end)`：分 3 步跳着播放（适合帧动画）`cubic-bezier()`：自定义贝塞尔曲线

* `animation-iteration-count`
  **动画播放次数**
  作用：设置动画播放多少次。
  常见值：
  1. `1`：播放 1 次（默认）
  2. `3`：播放 3 次
  3. `infinite`：无限循环播放

* **`animation-direction`**
  **动画播放方向**
  作用：控制动画是否反向播放或来回播放。
  常见值：
  1. `normal`：正常方向播放（默认）
  2. `reverse`：反方向播放
  3. `alternate`：奇数次正向，偶数次反向（来回播放）
  4. `alternate-reverse`：奇数次反向，偶数次正向

* **`a0nimation-fill-mode`**
  **动画填充模式**
  作用：定义动画**在开始前和结束后**，元素保持什么状态。
  常见值：
  1. `none`：动画外不应用任何样式（默认）
  2. `forwards`：动画结束后，保持最后一帧的样式
  3. `backwards`：动画开始前，使用第一帧的样式（通常不明显）
  4. `both`：结合 `forwards` 和 `backwards`

* **`animation-play-state`**
  **动画播放状态**
  作用：控制动画是**正在播放还是暂停**。
  常见值：
  1. `running`：播放（默认）
  2. `paused`：暂停
     示例：可用于鼠标悬停时暂停动画：

```css
.box:hover {
  animation-play-state: paused;
}
```

✅ 总结表格

| 属性名                      | 中文含义 | 常见用途           |
| --------------------------- | -------- | ------------------ |
| `animation-name`            | 动画名称 | 指定关键帧动画     |
| `animation-duration`        | 持续时间 | 控制动画长短       |
| `animation-delay`           | 延迟时间 | 设置开始前等待多久 |
| `animation-timing-function` | 缓动效果 | 控制动画节奏       |
| `animation-iteration-count` | 播放次数 | 设定循环次数       |
| `animation-direction`       | 播放方向 | 正放、反放、来回   |
| `animation-fill-mode`       | 填充模式 | 动画前后保持状态   |
| `animation-play-state`      | 播放状态 | 暂停或继续         |

------

这些属性可以单独使用，也可以用简写属性 `animation` 一起写：

```css
.box {
  animation: slideIn 2s 0.5s ease-in infinite alternate forwards;
}
```



##### 过渡与动画的区别

- **过渡（Transition）**：描述**两个状态之间**如何平滑地变化，需要**触发条件**（如鼠标悬停）。
- **动画（Animation）**：定义**一系列关键帧**，可以自动播放、循环、更复杂地控制整个动画过程。

------

✅ 二、详细对比

| 特性                   | **过渡（Transition）**                               | **动画（Animation）**                               |
| ---------------------- | ---------------------------------------------------- | --------------------------------------------------- |
| **是否需要触发**       | ✅ 必须由用户行为触发（如 `:hover`, `:focus`）        | ❌ 可以自动播放，无需用户交互                        |
| **是否自动播放**       | ❌ 不会自动播放                                       | ✅ 可以设置 `animation-play-state: running` 自动播放 |
| **是否支持循环**       | ❌ 只能来回切换状态，不支持真正循环                   | ✅ 支持无限循环 `infinite`                           |
| **是否支持多个关键帧** | ❌ 只能从 A 状态到 B 状态（`from` → `to`）            | ✅ 支持多个关键帧（`0%`, `25%`, `50%`, `100%`）      |
| **是否支持反向播放**   | ✅ 可以通过 `transition` 反向生效                     | ✅ 支持 `animation-direction: alternate` 来回播放    |
| **是否可暂停**         | ❌ 不易控制暂停                                       | ✅ 可通过 `animation-play-state: paused` 暂停        |
| **是否依赖状态变化**   | ✅ 必须有 CSS 属性变化（如 `width` 从 100px → 200px） | ❌ 不依赖，可独立运行                                |
| **是否支持填充模式**   | ❌ 不支持                                             | ✅ 支持 `animation-fill-mode: forwards` 保持最终状态 |
| **控制精细度**         | ⭐ 一般，适合简单变化                                 | ⭐⭐⭐ 高，适合复杂动画                                |



#### transfrom	transition	animation 的区别

| 属性         | 作用                             | 类比                       | 说明                                                         |
| ------------ | -------------------------------- | -------------------------- | ------------------------------------------------------------ |
| `transform`  | **让元素变形或移动**（静态）     | “动作本身”：比如伸展、旋转 | 单独用时，**是瞬间完成的**，没有动画效果                     |
| `transition` | **让变化“慢慢来”**（需要触发）   | “慢动作播放”：让变形变柔和 | 让某个属性的变化**有过渡效果**（比如从红变蓝，慢慢渐变）,需要**触发** |
| `animation`  | **自动播放的复杂动画**（可循环） | “自动播放的动画片”         | 不需要用户触发（可以自动播放），能做更复杂的动画序列         |

### 多列布局

一般做新闻可以这么做

常用属性如下：

- `column-count`：指定列数，值是数字。
- `column-width`：指定列宽，值是长度。
- `columns`：同时指定列宽和列数，复合属性；值没有数量和顺序要求。
- `column-gap`：设置列边距，值是长度。
- `column-rule-style`：设置列与列之间边框的风格，值与 `border-style` 一致。
- `column-rule-width`：设置列与列之间边框的宽度，值是长度。
- `column-rule-color`：设置列与列之间边框的颜色。
- `column-rule`：设置列边框，复合属性。
- `column-span`：指定是否跨列；值: `none`、`all`。





### 伸缩盒模型

#### 伸缩盒模型简介

- **2009 年，W3C 提出了一种新的盒子模型——Flexible Box（伸缩盒模型，又称：弹性盒子）。**
- 它可以轻松地控制：元素分布方式、元素对齐方式、元素视觉顺序……
- 截止目前，除了在部分 IE 浏览器不支持，其他浏览器均已全部支持。
- 伸缩盒模型的出现，逐渐演变出了一套新的布局方案——**flex 布局。**

>😀小贴士：
>
>1. 传统布局是指：基于传统盒状模型，主要靠：`display` 属性 + `position` 属性 + `float` 属性。
>2. flex 布局目前在移动端应用比较广泛，因为传统布局不能很好地呈现在移动设备上。



#### 伸缩容器、伸缩项目

伸缩容器：

- **定义**：开启了 `flex` 的元素，就是伸缩容器。

1. 给元素设置 `display: flex` 或 `display: inline-flex`，该元素就变为了伸缩容器。
2. `display: inline-flex` 很少使用，因为可以给多个伸缩容器的父容器，也设置为伸缩容器。
3. 一个元素可以同时是：伸缩容器、伸缩项目。

伸缩项目：

- **定义**：伸缩容器所有子元素自动成为了伸缩项目。

1. 仅伸缩容器的子元素成为了伸缩项目，孙子元素、重孙子元素等后代，不是伸缩项目。
2. 无论原来是哪种元素（块、行内块、行内），一旦成为了伸缩项目，全都会“块状化”。



#### 主轴方向

##### 主轴与侧轴

- **主轴**：伸缩项目沿着主轴排列，主轴默认是水平的，默认方向是从左到右（左边是起点，右边是终点）。
- **侧轴**：与主轴垂直的就是侧轴，侧轴默认是垂直的，默认方向是从上到下（上边是起点，下边是终点）。

------

##### 主轴方向

- **属性名**：`flex-direction`
- 常用值如下
  1. `row`：主轴方向水平从左到右 —— 默认值
  2. `row-reverse`：主轴方向水平从右到左
  3. `column`：主轴方向垂直从上到下
  4. `column-reverse`：主轴方向垂直从下到上

注意：

改变了主轴的方向，侧轴方向也随之改变。



#### 主轴换行

属性名：`flex-wrap`

`nowrap`：默认值，不换行。

![image-20250909150111172](./笔记/web-img/image-20250909150111172.png)

`wrap`：自动换行，伸缩容器不够时自动换行。

![image-20250909150130947](./笔记/web-img/image-20250909150130947.png)

`wrap-reverse`：反向换行。

![image-20250909150145448](./笔记/web-img/image-20250909150145448.png)



#### flex-flow

- `flex-flow` 是一个复合属性，复合了 `flex-direction` 和 `flex-wrap` 两个属性。值没有顺序要求。

```css
flex-flow: row wrap;
```





#### 主轴对齐方式

属性名：`justify-content`

- 常用值如下
  1. `flex-start`：主轴起点对齐。—— 默认值
  2. `flex-end`：主轴终点对齐。
  3. `center`：居中对齐。
  4. `space-between`：均匀分布，两端对齐（最常用）。
  5. `space-around`：均匀分布，两端距离是中间距离的一半。
  6. `space-evenly`：均匀分布，两端距离与中间距离一致。

![image-20250909151014062](./笔记/web-img/image-20250909151014062.png)

#### 侧轴对齐

 1.只有一行的情况

- **所需属性**：`align-items`
- 常用值如下
  1. `flex-start`：侧轴的起点对齐。
  2. `flex-end`：侧轴的终点对齐。
  3. `center`：侧轴的中点对齐。
  4. `baseline`：伸缩项目的第一行文字的基线对齐。
  5. `stretch`：如果伸缩项目未设置高度，将占满整个容器的高度。——（默认值）

<img src="./笔记/web-img/image-20250909151835146.png" alt="image-20250909151835146" style="zoom: 67%;" />

<img src="./笔记/web-img/image-20250909151856490.png" alt="image-20250909151856490" style="zoom:67%;" />







2.多行的情况

所需属性：`align-content`

- 常用值如下
  1. `flex-start`：与侧轴的起点对齐。
  2. `flex-end`：与侧轴的终点对齐。
  3. `center`：与侧轴的中点对齐。
  4. `space-between`：与侧轴两端对齐，中间平均分布。
  5. `space-around`：伸缩项目间的距离相等，比距边缘大一倍。
  6. `space-evenly`：在侧轴上完全平分。
  7. `stretch`：占满整个侧轴。——默认值

![image-20250909152633503](./笔记/web-img/image-20250909152633503.png)

<img src="./笔记/web-img/image-20250909152701051.png" alt="image-20250909152701051" style="zoom: 67%;" />

<img src="./笔记/web-img/image-20250909152724476.png" alt="image-20250909152724476" style="zoom:67%;" />



#### 元素的水平垂直居中

方案一：

给父容器

```css
display:flex;
justify-content:center;
align-items:center;
```

方案二：

给父元素

```css
display:flex;
```

给子元素

```css
margin:auto;
```





#### 基准长度

flex-basis

- **概念**：`flex-basis` 设置的是主轴方向的基准长度，会让宽度或高度失效。
  - **备注**：主轴横向：宽度失效；主轴纵向：高度失效
- **作用**：浏览器根据这个属性设置的值，计算主轴上是否有多余空间，默认值 `auto`，即：伸缩项目的宽或高。





#### 拉伸

 **flex-grow（伸）**

- **概念**：`flex-grow` 定义伸缩项目的放大比例，默认为 `0`，即：纵使主轴存在剩余空间，也不拉伸（放大）。
- **规则**：
  1. 若所有伸缩项目的 `flex-grow` 值都为 `1`，则：它们将等分剩余空间（如果有空间的话）。
  2. 若三个伸缩项目的 `flex-grow` 值分别为 `1`、`2`、`3`，则：分别瓜分到 `1/6`、`2/6`、`3/6` 的空间



#### 压缩

**flex-shrink（缩）**

- **概念**：`flex-shrink` 定义了项目的压缩比例，默认为 `1`，即：如果空间不足，该项目将会缩小。
- **收缩项目的计算**，略微复杂一点，我们拿一个场景举例：

例如：

三个收缩项目，宽度分别为：200px、300px、200px，它们的 `flex-shrink` 值分别为：1、2、3。 若想刚好容纳下三个项目，需要总宽度为 700px，但目前容器只有 400px，还差 300px。 所以每个人都要收缩一下才可以放下，具体收缩的值，这样计算：

1. 计算分母：(200×1) + (300×2) + (200×3) = 1400
2. 计算比例：
   - 项目一：(200×1) / 1400 = 比例值1
   - 项目二：(300×2) / 1400 = 比例值2
   - 项目三：(200×3) / 1400 = 比例值3
3. 计算最终收缩大小：
   - 项目一需要收缩：比例值1 × 300
   - 项目二需要收缩：比例值2 × 300
   - 项目三需要收缩：比例值3 × 300



#### flex复合属性

复合了 flex-grow	flex-shrink	flex-basis 三个属性，默认值为 0	1 	auto

```css
/* 可以拉伸 可以压缩 不设置基准长度，可简写为: flex:auto */
/* flex:1 1 auto; */

/* 可以拉伸 可以压缩 设置基准长度为0，可简写为: flex:1 */
/* flex: 1 1 0; */

/* 不可以拉伸 不可以压缩 不设置基准长度，可简写为: flex:none */
/* flex: 0 0 auto; */

/* 不可以拉伸 可以压缩 不设置基准长度，可简写为: flex:0 auto */
/* flex: 0 1 auto; */
```



#### 排序和单独对齐

项目排序

- **order 属性** 定义项目的排列顺序。数值越小，排列越靠前，默认为 `0`。

单独对齐

- 通过 `align-self` 属性，可以单独调整某个伸缩项目的对齐方式。
- 默认值为 `auto`，表示继承父元素的 `align-items` 属性。





### 响应式布局

#### 媒体查询

**@media**

##### 媒体类型

* 只有在打印机或打印预览才应用的样式

```css
@media print {
    h1 {
        background: transparent;
    }
}
```

* 只有在屏幕上才应用的样式

```css
@media screen {
    h1 {
        font-family: "翩翩体-简";
    }
}
```

* 一直都应用的样式

```css
@media all {
    h1 {
        color: red;
    }
}
```

##### 媒体特性

| 值                 | 含义                               |
| ------------------ | ---------------------------------- |
| `width`            | 检测视口宽度。                     |
| `max-width`        | 检测视口最大宽度。                 |
| `min-width`        | 检测视口最小宽度。                 |
| `height`           | 检测视口高度。                     |
| `max-height`       | 检测视口最大高度。                 |
| `min-height`       | 检测视口最小高度。                 |
| `device-width`     | 检测设备屏幕的宽度。               |
| `max-device-width` | 检测设备屏幕的最大宽度。           |
| `min-device-width` | 检测设备屏幕的最小宽度。           |
| `orientation`      | 检测视口的旋转方向（是否横屏）。   |
| portrait           | 视口处于纵向，即高度大于等于宽度。 |
| landscape          | 视口处于横向，即宽度大于高度。     |

- **portrait**：视口处于纵向，即高度大于等于宽度。
- **landscape**：视口处于横向，即宽度大于高度。

------

完整列表请参考：

https://developer.mozilla.org/zh-CN/docs/Web/CSS/@media



##### 运算符

| 值        | 含义                                                         |
| --------- | ------------------------------------------------------------ |
| `and`     | 并且（用于组合多个媒体特性）                                 |
| `, 或 or` | 或（用逗号分隔不同的媒体查询，满足任一条件即应用样式）       |
| `not`     | 否定（取反整个媒体查询的结果）                               |
| `only`    | 肯定（限定仅当条件完全匹配时应用样式，主要用于防止旧版浏览器错误应用样式） |

```css
/* @media (min-width:700px) and (max-width:800px) { ... */

@media screen and (min-width: 700px) and (max-width: 800px) {
    h1 {
        background-color: orange;
    }
}
```



#### 常用阈值

在实际开发中，会将屏幕划分成几个区间，例如：

- **超小屏幕**：宽度小于 768px
- **中等屏幕**：宽度在 768px 到 992px 之间
- **大屏幕**：宽度在 992px 到 1200px 之间
- **超大屏幕**：宽度大于 1200px

------

结合外部样式的用法

用法一：

```html
<link rel="stylesheet" media="具体的媒体查询" href="mystylesheet.css">
```

用法二：

```css
@media screen and (max-width: 768px) {
    /* CSS-Code */
}

@media screen and (min-width: 768px) and (max-width: 1200px) {
    /* CSS-Code */
}
```







### BFC

* 什么是BFC？

1. BFC 是 Block Formatting Context（块级格式化上下文），可以理解成元素的一个“特异功能”。
2. 该“特异功能”，在默认的情况下处于关闭状态；当元素满足了某些条件后，该“特异功能”被激活。
3. 所谓激活“特异功能”，专业点说就是：该元素创建了 BFC（又称：开启了 BFC）。



* BFC有什么用？

1. 元素开启 BFC 后，其**子元素**不会再产生 margin 塌陷问题。
2. 元素开启 BFC 后，自己不会被其他浮动元素所覆盖。
3. 元素开启 BFC 后，就算其子元素浮动，元素自身高度也不会塌陷。



* 如何开启BFC？
  1. 根元素
  2. 浮动元素
  3. 绝对定位、固定定位的元素行内块元素
  4. 表格单元格：`table`、`thead`、`tbody`、`tfoot`、`th`、`td`、`tr`、`caption``
  5. ``overflow` 的值不为 `visible` 的块元素
  6. 伸缩项目
  7. 多列容器
  8. `column-span` 为 `all` 的元素（即使该元素没有包裹在多列容器中）
  9. `display` 的值，设置为 `flow-root`







## JavaScript

1. JavaScript（是什么？）
   - 是一种运行在客户端（浏览器）的编程语言，实现人机交互效果。
2. 作用（做什么？）
   - 网页特效（监听用户的一些行为让网页作出对应的反馈）
   - 表单验证（针对表单数据的合法性进行判断）
   - 数据交互（获取后台的数据，渲染到前端）
   - 服务端编程（node.js）
3. JavaScript的组成（有什么？）

-  ECMAScript:
   - 规定了js基础语法核心知识。
     - 比如：变量、分支语句、循环语句、对象等等
-  Web APIs：
   - DOM 操作文档，比如对页面元素进行移动、大小、添加删除等操作
   - BOM 操作浏览器，比如页面弹窗，检测窗口宽度、存储数据到浏览器等等



### JS的引入方式

##### **内部 JavaScript**

- 直接写在html文件里，用script标签包住
- 规范：script标签写在</body>上面
- 拓展：alert('你好，js') 页面弹出警告对话框

```js
<script>
    alert('嗨，欢迎来传智播学习前端技术！')
</script>
</body>
```

> 注意事项

我们将 <script> 放在HTML文件的底部附近的原因是浏览器会按照代码在文件中的顺序加载 HTML。

如果先加载的 JavaScript 期望修改其下方的 HTML，那么它可能由于 HTML 尚未被加载而失效。

因此，将 JavaScript 代码放在 HTML页面的底部附近通常是最好的策略。



##### **外部 JavaScript**

代码写在以 `.js`结尾的文件里

语法：通过 script 标签，引入到 html 页面中。

```js
<body>
    <!-- 通过src引入外部js文件 -->
    <script src="my.js"></script>
</body>
```

>注意事项

1. script标签中间无需写代码，否则会被忽略！
2. 外部JavaScript会使代码更加有序，更易于复用，且没有了脚本的混合，HTML也会更加易读，因此这是个好的习惯。



##### **内联 JavaScript**

- **代码位置**：代码写在标签内部，用 onclick
- **语法**：无具体语法展示，仅作概念说明
- **注意事项**：此处作为了解即可，但是后面 vue 框架会用这种模式

示例代码

```js
<body>
  <button onclick="alert('逗你玩~~~')">点击我月薪过万</button>
</body>
```



###  注释和结束符

通过注释可以屏蔽代码被执行或者添加备注信息，JavaScript 支持两种形式注释语法：

##### 单行注释

使用 `// ` 注释单行代码

##### 多行注释

使用 `/* */` 注释多行代码

> 编辑器中单行注释的快捷键为 `ctrl + /`

##### 结束符

在 JavaScript 中 `;` 代表一段代码的结束，多数情况下可以省略 `;` 使用回车（enter）替代。

> 实际开发中有许多人主张书写 JavaScript 代码时省略结束符 `;`



### 输入和输出

##### 输出语法:

语法 1:（一般不用了）

```js
document.write('要出的内容')
```

作用: 向 body 内输出内容

注意: 如果输出的内容写的是标签, 也会被解析成网页元素

语法 2:

```js
alert('要出的内容')
```

作用: 页面弹出警告对话框

语法 3:

```js
console.log('控制台打印')
```

作用: 控制台输出语法, 程序员调试使用

##### 输入语法：

语法：`prompt('请输入您的姓名:')`

作用：显示一个对话框，对话框中包含一条文字信息，用来提示用户输入文字



### 字面量

##### 定义：

源代码中，直接写出的，不需要计算的、能够被编译器直接理解，并转化成对应数据类型的值

##### 示例：

- 我们工资是：1000，此时1000就是数字字面量。

- '黑马程序员'是字符串字面量。

  

### 变量

定义：计算机中用来存储数据的“容器”，简单理解是一个个的盒子。用来存储数据的

##### 声明变量

语法：`let 变量名`

- 声明变量有两部分构成：声明关键字、变量名（标识）。

举例：`let age`

- 我们声明了一个`age`变量。
- `age`即变量的名称，也叫标识符。



##### 变量赋值

定义：定义了一个变量后，你就能够初始化它（赋值 。在变量名之后跟上一个 “=”，然后是数值。）

```js
// 1. 声明一个 age 变量
let age
// 2. age 变量赋值为 18
age = 18
// 3. 输出age变量
alert(age)
```

> 是通过变量名来获得变量里面的数据



##### 更新变量

变量赋值后，还可以通过简单地给它一个不同的值来更新它。

```js
// 声明了一个age变量，同时里面存放了18这个数据
let age = 18
// 变量里面的数据发生变化更改为19
age = 19
// 页面输出的结果为19
document.write(age)
```

> let 不允许多次声明一个变量。



##### 声明多个变量

定义：变量赋值后，还可以通过简单地给它一个不同的值来更新它。

语法：多个变量中间用逗号隔开。

```js
let age = 18, uname = 'pink'
```

> 看上去代码长度更短，但并不推荐这样。为了更好的可读性，请一行只声明一个变量。



##### 交换变量的值

**步骤**：

1. 声明一个临时变量 temp
2. 把 num1 的值赋值给 temp
3. 把 num2 的值赋值给 num1
4. 把 temp 的值给 num2

> 没了~~~临时变量不用自动销毁



##### 变量的命名规则和规范

**规则**

- 不能用关键字

  > 关键字：有特殊含义的字符，JavaScript 内置的一些英语词汇。例如：let、var、if、for等

- 只能用下划线、字母、数字、$组成，且数字不能开头

- 字母严格区分大小写，如 Age 和 age 是不同的变量

**规范**

- 起名要有意义

- 遵守小驼峰命名法

  > 第一个单词首字母小写，后面每个单词首字母大写。例：userName



##### ‼️ let 和 var 区别

let声明局部变量，不可重复声明，先使用后声明会报错

var声明全局变量，可重复声明，二次声明会覆盖其前一次的声明；如果在编译阶段会将全局变量在不同的作用域中提升至全局位置，所以可以先使用后声明，但是赋值得先赋值



### 常量

**定义**：使用 const 声明的变量称为“常量”

**使用场景**: 当某个变量**永远不会改变**的时候, 就可以使用 const 来声明, 而不是let。

**命名规范**: 和变量一致

**常量使用:**

```js
// 声明一个常量
const G = 9.8
//输出这个常量
console.log(G)
```

> 常量不允许重新赋值, 声明的时候必须赋值(初始化)；并且不能二次赋值



### 数据类型

##### **基本数据类型**

基本数据类型是按值访问的，存储在栈内存中，共有 6 种：

| 类型        | 说明                     | 示例                       |
| ----------- | ------------------------ | -------------------------- |
| `number`    | 数字类型，包括整数和小数 | `10`, `3.14`, `-100`       |
| `string`    | 字符串类型，文本数据     | `'hello'`, `"JavaScript"`  |
| `boolean`   | 布尔类型，表示逻辑值     | `true`, `false`            |
| `undefined` | 未定义类型               | 变量声明但未赋值时的默认值 |
| `null`      | 空值类型                 | 表示“无”或“空对象指针”     |
| `symbol`    | 符号类型（ES6 新增）     | 用于创建唯一标识符         |

> 💡 注意：虽然 `null` 被认为是对象类型（`typeof null` 返回 `"object"`），但它属于基本数据类型。

##### **引用数据类型**

引用类型的数据存储在堆内存中，通过引用地址访问，主要包括：

| 类型       | 说明                                           |
| ---------- | ---------------------------------------------- |
| `object`   | 对象类型，用于存储键值对                       |
| `array`    | 数组类型，一种特殊的对象，用于存储有序数据集合 |
| `function` | 函数类型，也可看作可调用的对象                 |

> 🔍 扩展说明：
>
> - 在 JavaScript 中，**数组和函数本质上都是对象**，因此引用类型统称为 `object`。
> - 使用 `typeof` 检测引用类型时，对象、数组返回 `"object"`，函数返回 `"function"`。



##### 数值类型

定义：在 JavaScript 中，**所有数字**（无论是整数还是小数）都属于 `number` 类型。

```js
let age = 25;        // 整数
let price = 9.99;    // 小数
let temp = -10;      // 负数
```

🔍 `typeof` 检测结果均为 `"number"`：

```js
console.log(typeof 100);     // "number"
console.log(typeof 3.14);    // "number"
```

> JS 是弱数据类型,变量到底属于那种类型,只有赋值之后,我们才能确认
>
> Java 是强数据类型 例如 int a = 3 必须是整数



###### NaN

NaN 不等于任何人，包括他自己

NaN 代表一个计算错误。它是一个不正确的或者一个未定义的数学操作所得到的结果

```js
console.log('老师' - 2) // NaN
```

NaN 是粘性的。任何对 NaN 的操作都会返回 NaN

```js
console.log(NaN + 2) // NaN
```



##### 字符串类型

定义：通过单引号、双引号或反引号包裹的数据都叫字符串，单引号和双引号没有本质上的区别，推荐使用单引号

```js
let uname = '小明' // 使用单引号
let gender = "男" // 使用双引号
let goods = `小米` // 使用反引号
let tel = '13681113456' // 看上去是数字，但是引号包裹了就是字符串
let str = '' // 这种情况叫空字符串
```

> 1. 无论单引号或是双引号必须成对使用
> 2. 单引号/双引号可以互相嵌套, 但是不以自己嵌套自己 (口诀: 外双内单, 或者外单内双)
> 3. 必要时可以使用转义符 ,输出单引号或双引号



###### 字符串拼接

**场景**：

+运算符 可以实现字符串的拼接。

**口诀**：数字相加，字符相连



##### 布尔类型

`true` —— 真（表示“是”或“开启”）

`false` —— 假（表示“否”或“关闭”）

```js
let isLogin = true;
let isLoading = false;

console.log(typeof true);   // "boolean"
console.log(typeof isLogin); // "boolean"
```

> 布尔值常用于条件判断、循环控制和逻辑运算。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JavaScript 基础 - 数据类型</title>
</head>
<body>
  
  <script> 
    //  pink老师帅不帅？回答 是 或 否
    let isCool = true // 是的，摔死了！
    isCool = false // 不，套马杆的汉子！

    document.write(typeof isCool) // 结果为 boolean
  </script>
</body>
</html>
```



##### undefined

定义：`undefined` 是 JavaScript 中的一种**基本数据类型**（也是其唯一的值），表示**“未定义”或“没有值”**。

######  什么时候会出现 `undefined`？

1. **变量声明但未赋值**

```js
let age;
console.log(age); // undefined
```

2. **对象中不存在的属性**

```js
let user = { name: "小明" };
console.log(user.age); // undefined
```

3. **函数没有返回值**

```js
function sayHello() {
  console.log("Hello");
}
let result = sayHello(); // 函数没有 return
console.log(result);     // undefined
```

4. **函数参数未传值**

```js
function greet(name) {
  console.log("你好，" + name);
}
greet(); // 没传参数
// 输出：你好，undefined
```



##### null

###### 什么是 `null`？

`null` 是 JavaScript 中的一个**基本数据类型**，表示 **“空值”或“无对象”** —— 即**有意地表示“这里什么都没有”**。

```js
let selectedUser = null;
console.log(selectedUser); // null
```

> 📌 关键点：`null` 是**开发者主动赋值**的，表示“我明确知道这个变量现在没有值，但以后可能会有”。



###### `null` 的特点

| 特性     | 说明                                                         |
| -------- | ------------------------------------------------------------ |
| 类型     | 基本数据类型（但 `typeof null` 返回 `"object"` —— 这是 JS 的历史 bug ❗） |
| 值       | 只有一个值：`null`                                           |
| 含义     | “空值”、“无”、“未指向任何对象”                               |
| 谁设置的 | 通常由**开发者手动赋值**                                     |

```js
console.log(null);           // null
console.log(typeof null);    // "object" （错误！应为 "null"）
```

> ⚠️ `typeof null === "object"` 是一个著名的 JavaScript 设计错误，需注意。



######  `null` 的常见用途

1. **初始化变量，表示“暂无值”**

```js
let currentUser = null; // 先设为空，登录后再赋值
```

2. **清空对象引用**

```js
let data = { name: "张三", age: 25 };
data = null; // 主动释放引用，便于垃圾回收
```

3. **表示函数返回“无结果”**

```js
function findUser(id) {
  // 如果没找到用户，返回 null
  return null;
}
```

4. **DOM 操作中表示“元素不存在”**

```js
let element = document.getElementById("notExist");
console.log(element); // null （注意：不是 undefined）
```



###### 如何正确检测 `null`？

由于 `typeof null` 返回 `"object"`，不能直接用 `typeof` 判断。

✅ 正确方法：使用严格相等 `===`

```js
let value = null;

if (value === null) {
  console.log("value 是 null");
}
```

❌ 错误方式：

```js
if (typeof value === "null") { ... } // 永远不会成立！
```



##### `null` vs `undefined` 对比

| 对比项        | `null`                     | `undefined`                  |
| ------------- | -------------------------- | ---------------------------- |
| 含义          | “**人为设为空**”           | “**自动未定义**”             |
| 设置者        | 开发者主动赋值             | JavaScript 自动设置          |
| 使用场景      | 初始化、清空、表示“无结果” | 变量声明未赋值、属性不存在等 |
| `typeof` 结果 | `"object"`（历史 bug）     | `"undefined"`                |
| 推荐做法      | ✅ 手动赋值                 | ❌ 避免手动赋 `undefined`     |



### 检测数据类型

##### 通过typeof关键字检测数据类型

typeof运算符可以返回被检测的数据类型。它支持两种语法形式：

1. **作为运算符**：typeof x （常用的写法）
2. **函数形式**：typeof(x)

换言之，有括号和没有括号，得到的结果是一样的，所以我们直接使用运算符的写法。

```js
<script>
let num = 10;
console.log(typeof num);

let str = 'pink';
console.log(typeof str);

let str1 = '10';
console.log(typeof str1);

let flag = false;
console.log(typeof flag);

let un;
console.log(typeof un);

let obj = null;
console.log(typeof obj);
</script>
```



### 模板字符串

##### 什么是模板字符串？

**定义**：**模板字符串**（Template Strings / Template Literals）是 ES6（ES2015）引入的一种新语法，用于更方便地创建和拼接字符串。

它使用**反引号（```）**包裹字符串，支持：

- 多行文本
- 嵌入变量和表达式（插值）
- 函数调用、运算等

| 特性           | 描述                                                         | 示例                                                         |
| -------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **基本语法**   | 使用反引号（`` ` ``）定义模板字符串。                        | `` `这是一个模板字符串` ``                                   |
| **变量插值**   | 使用 `${}` 语法在字符串中嵌入变量或表达式。                  | `` `姓名: ${name}, 年龄: ${age}` ``                          |
| **多行支持**   | 自然支持多行文本，不需要额外的换行符或转义字符。             | `` `这是第一行<br>这是第二行` ``                             |
| **表达式嵌入** | 可以在 `${}` 中嵌入任意有效的JavaScript表达式，包括函数调用和运算符。 | `` `结果: ${2 + 3}, 函数结果: ${myFunction()}` ``            |
| **嵌套模板**   | 可以在一个模板字符串中嵌套另一个模板字符串。                 | `` `外部模板: ${`内部模板: ${value}`} ` ``                   |
| **标签模板**   | 可以为模板字符串添加标签，以便对生成的字符串进行进一步处理。 | `` taggedTemplate`Hello ${name}!` ``                         |
| **HTML转义**   | 不自动转义HTML内容，因此需要手动处理以防止XSS攻击。          | `` `<div>${userInput}</div>` `` （注意：需确保 `userInput` 安全） |



##### 基本语法

```javascript
let message = `这是一个模板字符串`;
console.log(message); // 输出: 这是一个模板字符串
```

##### 变量插值

```javascript
let name = "Alice";
let age = 30;
let message = `姓名: ${name}, 年龄: ${age}`;
console.log(message); // 输出: 姓名: Alice, 年龄: 30
```

##### 多行支持

```javascript
let multiLine = `这是第一行
这是第二行`;
console.log(multiLine);
// 输出:
// 这是第一行
// 这是第二行
```

##### 表达式嵌入

```javascript
let a = 5;
let b = 10;
let result = `两数之和: ${a + b}`;
console.log(result); // 输出: 两数之和: 15

function add(x, y) {
    return x + y;
}

let expressionResult = `函数结果: ${add(3, 4)}`;
console.log(expressionResult); // 输出: 函数结果: 7
```

##### 嵌套模板

```javascript
let value = "嵌套内容";
let nestedTemplate = `外部模板: ${`内部模板: ${value}`} `;
console.log(nestedTemplate); // 输出: 外部模板: 内部模板: 嵌套内容
```

##### 标签模板

```javascript
function taggedTemplate(strings, ...values) {
    return strings.map((str, i) => `${str}${values[i] || ''}`).join('');
}

let name = "Alice";
let greeting = taggedTemplate`Hello ${name}!`;
console.log(greeting); // 输出: Hello Alice!
```

#### 

### 类型转换

定义：把一种数据类型的变量转换成我们需要的数据类型

##### 隐式转换

1. **+号**可以将其他类型转换为数值类型，有字符串的加法 `"" + 1`，结果是 `"1"`
2. **减法 -**（像大多数数学运算一样）只能用于数字，它会使空字符串 `""` 转换为 `0`
3. `null` 经过数字转换之后会变为 `0`
4. `undefined` 经过数字转换之后会变为 `NaN`
5. 任何数据和字符串相加都是拼接状态



##### 显式转换

定义：开发者**主动控制**类型转换过程，确保程序行为的准确性和可读性。

###### 1. **转换为字符串（String）**

- 使用 `String()` 函数：

  ```js
  let num = 123;
  let str = String(num);        // "123"
  let bool = String(true);      // "true"
  ```

- 使用 `.toString()` 方法：

  ```js
  let num = 456;
  let str = num.toString();     // "456"
  ```

------

###### 2. **转换为数字（Number）**

**Number（数据）**

> 转成数字类型
>
> 如果字符串里有非数字，转换失败结果为 NaN，不是一个数字
>
> NaN 也是number 类型的数据，代表非数字

**parselnt（数据）（整数）**

> 只保留整数

**parseFloat（数据）（小数）**

> 可以保留小数

- 使用 `Number()` 函数：

  ```js
  let str = "123";
  let num = Number(str);        // 123
  
  Number("12.3");   // 12.3
  Number("abc");    // NaN
  Number(true);     // 1
  Number(false);    // 0
  ```

- 使用 `parseInt()` 和 `parseFloat()`（常用于字符串转数字，可自动忽略非数字字符）：

  ```js
  parseInt("123px");   // 123
  parseFloat("3.14abc"); // 3.14
  ```

- 使用一元加号 `+`（简写方式）：

  ```js
  let num = +"123";   // 123
  let x = +"3.14";    // 3.14
  ```

------

###### 3. **转换为布尔值（Boolean）**

- 使用

  ```
  Boolean()
  ```

  函数：

  ```js
  Boolean(1);        // true
  Boolean(0);        // false
  Boolean("hello");  // true
  Boolean("");       // false
  Boolean(null);     // false
  ```

> 注意：只有 `0`、`""`、`null`、`undefined`、`NaN`、`false` 转为 `false`，其余都为 `true`。



##### 区别

| 对比项       | **显式转换（Explicit Coercion）**                            | **隐式转换（Implicit Coercion）**       |
| ------------ | ------------------------------------------------------------ | --------------------------------------- |
| **定义**     | 开发者**主动、明确地**将一种类型转换为另一种类型             | JavaScript **自动、悄悄地**进行类型转换 |
| **谁触发**   | 你写的代码（调用函数）                                       | JS 引擎根据运算符或上下文自动触发       |
| **是否可见** | 代码中明显能看到转换函数                                     | 看不到转换过程，容易被忽略              |
| **常见方法** | `Number()`, `String()`, `Boolean()` `parseInt()`, `toString()` 等 | `+`, `-`, `!`, `if`, `                  |
| **可控性**   | ✅ 高：你知道它会发生                                         | ⚠️ 低：容易产生意外结果                  |
| **可读性**   | 更清晰，意图明确                                             | 可能让代码变得“神奇”或难懂              |



### 运算符

#### 算术运算符

数字是用来计算的，比如：乘法 * 、除法 / 、加法 + 、减法 - 等等，所以经常和算术运算符一起。

算术运算符：也叫数学运算符，主要包括加、减、乘、除、取余（求模）等

| 运算符 | 作用                                                 |
| ------ | ---------------------------------------------------- |
| +      | 求和                                                 |
| -      | 求差                                                 |
| *      | 求积                                                 |
| /      | 求商                                                 |
| **%**  | 取模（取余数），开发中经常用于作为某个数字是否被整除 |

> 注意：在计算失败时(undefined加任何值 除了字符串)，显示的结果是 NaN （not a number）

```javascript
// 算术运算符
console.log(1 + 2 * 3 / 2) //  4 
let num = 10
console.log(num + 10)  // 20
console.log(num + num)  // 20

// 1. 取模(取余数)  使用场景：  用来判断某个数是否能够被整除
console.log(4 % 2) //  0  
console.log(6 % 3) //  0
console.log(5 % 3) //  2
console.log(3 % 5) //  3

// 2. 注意事项 : 如果我们计算失败，则返回的结果是 NaN (not a number)
console.log('pink老师' - 2)
console.log('pink老师' * 2)
console.log('pink老师' + 2)   // pink老师2
```

#### 赋值运算符

赋值运算符：对变量进行赋值的运算符

 =     将等号右边的值赋予给左边, 要求左边必须是一个容器

| 运算符 | 作用     |
| ------ | -------- |
| +=     | 加法赋值 |
| -+     | 减法赋值 |
| *=     | 乘法赋值 |
| /=     | 除法赋值 |
| %=     | 取余赋值 |

```javascript
<script>
let num = 1
// num = num + 1
// 采取赋值运算符
// num += 1
num += 3
console.log(num)
</script>
```

#### 自增/自减运算符

| 符号 | 作用 | 说明                       |
| ---- | ---- | -------------------------- |
| ++   | 自增 | 变量自身的值加1，例如: x++ |
| --   | 自减 | 变量自身的值减1，例如: x-- |

1. ++在前和++在后在单独使用时二者并没有差别，而且一般开发中我们都是独立使用
2. ++在后（后缀式）我们会使用更多

> 注意：
>
> 1. 只有变量能够使用自增和自减运算符
> 2. ++、-- 可以在变量前面也可以在变量后面，比如: x++  或者  ++x 

```javascript
<script>
    // let num = 10
    // num = num + 1
    // num += 1
    // // 1. 前置自增
    // let i = 1
    // ++i
    // console.log(i)

    // let i = 1
    // console.log(++i + 1)
    // 2. 后置自增
    // let i = 1
    // i++
    // console.log(i)
    // let i = 1
    // console.log(i++ + 1)

    // 了解 
    let i = 1
    console.log(i++ + ++i + i)
  </script>
```

前置自增和后置自增有什么区别

>单独使用时，没有区别
>
>前置自增：
>
>​		++在前，先加
>
>后置自增：
>
>​		++在后，先使用再加

#### 比较运算符

使用场景：比较两个数据大小、是否相等，根据比较结果返回一个布尔值（true / false）

| 运算符 | 作用                                                         |
| ------ | ------------------------------------------------------------ |
| >      | 左边是否大于右边                                             |
| <      | 左边是否小于右边                                             |
| >=     | 左边是否大于或等于右边                                       |
| <=     | 左边是否小于或等于右边                                       |
| ===    | 左右两边是否`类型`和`值`都相等（重点）全等（以后判断是否相等） |
| ==     | 左右两边`值`是否相等 只判断                                  |
| !=     | 左右值不相等                                                 |
| !==    | 左右两边是否不全等                                           |

```javascript
<script>
  console.log(3 > 5)
  console.log(3 >= 3)
  console.log(2 == 2)
  // 比较运算符有隐式转换 把'2' 转换为 2  双等号 只判断值
  console.log(2 == '2')  // true
  // console.log(undefined === null)
  // === 全等 判断 值 和 数据类型都一样才行
  // 以后判断是否相等 请用 ===  
  console.log(2 === '2')
  console.log(NaN === NaN) // NaN 不等于任何人，包括他自己
  console.log(2 !== '2')  // true  
  console.log(2 != '2') // false 
  console.log('-------------------------')
  console.log('a' < 'b') // true
  console.log('aa' < 'ab') // true
  console.log('aa' < 'aac') // true
  console.log('-------------------------')
</script>
```

不同类型之间比较会发生隐式转换：

* 最终把数据隐式转换成number类型再比较
* 开发中，如果进行准确的比较更喜欢 === 或者 ！==

#### 逻辑运算符

使用场景：可以把多个布尔值放到一起运算，最终返回一个布尔值

| 符号 | 名称   | 日常读法 | 特点                       | 口诀                 |
| ---- | ------ | -------- | -------------------------- | -------------------- |
| &&   | 逻辑与 | 并且     | 符号两边有一个假的结果为假 | 一假则假，两个都得真 |
| \|\| | 逻辑或 | 或者     | 符号两边有一个真的结果为真 | 一真则真             |
| !    | 逻辑非 | 取反     | true变false  false变true   | 真变假，假变真，取反 |

| A     | B     | A && B | A \|\| B | !A    |
| ----- | ----- | ------ | -------- | ----- |
| false | false | false  | false    | true  |
| false | true  | false  | true     | true  |
| true  | false | false  | true     | false |
| true  | true  | true   | true     | false |

```javascript
<script>
    // 逻辑与 一假则假
    console.log(true && true)
    console.log(false && true)
    console.log(3 < 5 && 3 > 2)
    console.log(3 < 5 && 3 < 2)
    console.log('-----------------')
    // 逻辑或 一真则真
    console.log(true || true)
    console.log(false || true)
    console.log(false || false)
    console.log('-----------------')
    // 逻辑非  取反
    console.log(!true)
    console.log(!false)

    console.log('-----------------')

    let num = 6
    console.log(num > 5 && num < 10)
    console.log('-----------------')
  </script>
```





#### 运算符优先级

从上到下，优先级越低

| 优先级 | 运算符     | 顺序            |
| ------ | ---------- | --------------- |
| 1      | 小括号     | ()              |
| 2      | 一元运算符 | ++ -- !         |
| 3      | 算数运算符 | 先 * / % 后 + - |
| 4      | 关系运算符 | > >= < <=       |
| 5      | 相等运算符 | == != === !==   |
| 6      | 逻辑运算符 | 先 && 后        |
| 7      | 赋值运算符 | =               |
| 8      | 逗号运算符 | ,               |



### 表达式和语句

**定义：**表达式是生成值的代码片段，语句是执行操作的完整指令

表达式：表达式是可以被求值的代码，JS引擎会将其计算出一个结果

​				表达式可以被求值，所以他可以写在赋值语句的右侧

语句：语句是一段可以执行的代码	eg.prompt（）可以弹出一个输入框，if 语句，for 循环语句

​			而语句不一定有值，所以 alert() for 和break 等语句就不能被用于赋值

某些情况下，也可以把表达式理解为表达式语句，因为它是在计算结果，但不是必需的成分



#### 分支语句

分支语句可以让我们**有选择性**的执行想要的代码

##### if分支语句

- if语句有三种使用：单分支、双分支、多分支
- 单分支使用语法：

```
if (条件) {
    满足条件要执行的代码
}
```

- 括号内的条件为true时，进入大括号里执行代码
- 小括号内的结果若不是布尔类型时，会发生隐式转换转为布尔类型
- 如果大括号只有一个语句，大括号可以省略，但是，俺们不提倡这么做~

###### 单分支

```js
 // if单分支
        if(false){
            console.log('执行语句')
        }
        if(true){
            console.log('执行语句')
        }
        if(3>1){
            console.log("真假")
        }  
        // 除了0,所有数字都为正
        if(3){
            console.log("真")
        }
        if(0){
            console.log("jia")
        }
        // 除了""空字符串，所有数字都为真
        if(""){
            console.log("加")
        }
```

###### 双分支

双分支两条代码，只有一条被执行

```js
if (条件) {
    满足条件要执行的代码 1
} else {
    不满足条件执行的代码 2
}
```

```js
// 双分支
        let name = prompt("请输入姓名")
        let password = prompt("请输入密码")
        if(name === "wjm" && password ==="123"){
            alert('成功')
        }else{
            alert('不成功')
        }
```

```js
// 判断闰年
        let year = +prompt("请输入年份")
        if(year % 4 === 0 && year % 100 !== 0 || year % 400 === 0){
            alert('是闰年')
        }else{
            alert('不是闰年')
        }
```

###### 多分支 

选择性的满足其中的一条

- 按顺序检查每个条件。
- 执行第一个满足条件的代码块，并跳过后续条件。
- 如果没有条件满足，则执行 `else` 中的代码。

```js
if (条件1) {
    代码1 // 若条件1为真，执行代码1并跳过后续条件
} else if (条件2) {
    代码2 // 若条件1为假且条件2为真，执行代码2并跳过后续条件
} else if (条件3) {
    代码3 // 若前两个条件都为假且条件3为真，执行代码3
} else {
    代码n // 若所有条件都为假，执行代码n
}
```



##### 三元运算符

- **使用场景**：比 `if` 双分支更简洁，适用于简单的条件判断。

- **符号**：`?` 和 `:` 配合使用。

- 语法

  ```
  条件 ? 满足条件执行的代码 : 不满足条件执行的代码
  ```

- **用途**：常用于取值。

```js
        console.log(3 > 5 ? 3 : 5)
```

```js
        let num1 = +prompt('请你输入第一个数')
        let num2 = +prompt('请你输入第二个数')
        num1 > num2 ?alert(`最大值是${num1}`) : alert(`最大值是${num2}`)
```



##### switch分支语句

- **匹配全等**：执行与 `switch` 中数据全等的 `case` 对应的代码。
- **无匹配**：执行 `default` 中的代码。
- **示例**：若数据等于值2，则执行代码2。

**注意事项：**

1. **用于等值判断**，不适合区间判断。
2. **需配合 `break` 使用**，否则会发生 `case` 穿透。

```js
// switch分支语句
        switch (5) {
            case 1:
                console.log("选择1")
                break
            case 2:
                console.log("选择2")
                break
            case 3:
                console.log("选择3")
                break
            default:
                console.log('没有符合条件的')

        }
```



#### 循环语句

**while循环和for循环的区别：**

for循环是确定了循环的次数，while循环是不确定执行的次数

##### while循环

**死循环**

```js
while(true){
    
}
```

在某个期间，while循环就是在满足条件期间，重复执行某些代码

```js
while (循环条件) {
    要重复执行的代码(循环体)
}
```

- **条件判断**：与 `if` 类似，小括号内条件为 `true` 时执行循环体。
- **循环机制**：执行完大括号内的代码后，返回检查条件是否仍为 `true`。若满足则继续执行，直到条件不满足才跳出循环。



##### do-while循环

```js
do {
    // 循环体（要执行的代码）
} while (条件);
```

- **先执行一次循环体**，然后再判断条件。
- 如果条件为 `true`，就继续循环；否则结束。
- **无论条件如何，循环体至少执行一次**。



##### for循环

**死循环**

```js
for( ; ; ){
    
}
```

- **作用**：重复执行代码。
- **好处**：将变量起始值、终止条件和变化量集中声明，清晰易读。

**语法：**

```js
for (变量起始值; 终止条件; 变量变化量) {
    // 循环体
}
```

**示例：**

```js
        // for循环
        for(let i = 1 ; i <= 3 ; i++){
            console.log('月薪过万')
        }
```



###### for-in 和 for-of的区别

> - `for...in`：遍历**索引（键）**，不推荐用于数组。
> - `for...of`：遍历**元素值**，推荐用于数组。



**总结**

- 想遍历对象的**属性名**？ → 用 `for...in`
- 想遍历数组/字符串的**元素值**？ → 用 `for...of`
- **不要用 `for...in` 遍历数组的值**，容易出错！

✅ 正确姿势：

```
for (let key in obj)      // 遍历对象的键
for (let value of arr)    // 遍历数组的值
```



###### for循环嵌套

> 外层循环打印行数
>
> 内层循环打印列数

```js
for（外部声明记录循环次数的变量；循环条件；变化值）{
    for（内部声明记录循环次数的变量；循环条件；变化值）{
        循环体
    }
}
```

说明：

> **一个循环里再套一个循环，一般用在for循环里**

```js
        // 循环嵌套
        for(let i = 1 ; i <= 3 ; i++){
            console.log(`记录了第${i}天`)
            for(let a = 1 ; a <= 5 ; a++){
                console.log(`记录了第${a}个单词`)
            }
        }
```

例子：

* 5行5列星星

```js
        // 5行5列星星
        let row = +prompt('请输入行数：')
        let col = +prompt('请输入列数：')
        // 外层循环打印行数
        for(let i = 1 ; i <= row ; i++){
            // 内层循环打印列数
            for(let a = 1 ; a <= col ; a++){
                document.write('⭐')
            }
            document.write('<br>')
        }
```

* 三角星星

```js
        // 三角星星
        let row = +prompt("请输入行数：")
        let col = +prompt("请输入列数：")

        for(let i = 1 ; i <= row ; i++){
            for(let a = 1 ; a <= i ; a++){
                document.write("⭐")
            }
            document.write('<br>')
        }

```

* 99乘法表

```js
        // 99乘法表
        for(let i = 1 ; i <= 9 ; i++){
            for(let a = 1 ; a <= i ; a++){
                document.write(`<span>${a} x ${i} = ${i * a}</span>`)
            }
            document.write('<br>')
        }
```





##### 循环三要素

1. **变量起始值**：设定初始值。
2. **终止条件**：避免死循环，必须有明确的结束条件。
3. **变量变化量**：通过自增或自减逐步接近终止条件。



> 案例：

循环的例子：

1.  输入 1 - 100 

```js
        // 输入 1 - 100 
        let i = 1
        while(i <= 100){
            console.log(`这是第${i}个数`)
            i++
        }

        console.log("----")

```

2. 计算从1+ 到100总和

```js
        // 计算从1+ 到100总和
        let a = 1
        let sum = 0
        while(a <= 100){
            sum = sum +a
            a++
        }
        console.log(sum)

```

3. 1-100的偶数和

```js
        // 1-100的偶数和
        let num = 1
        let sum2 = 0
        while (num <= 100) {
            if (num % 2 == 0) {
                sum2 = sum2 + num
            }
            num++
        }
        console.log(sum2)

```



##### 循环退出

**break**: 退出整个循环。

```js
        let a = 1
        while (a <= 5) {
            if (a === 3){
                  break
            }

            console.log(`我要吃${a}个包子`)
            a++

        }
```

```js
 while(true){
            let love = prompt("你爱我吗")
            if(love === "我爱你"){
                break
            }
        }
```

注意：			

> break 是终止整个循环



**continue**: 结束本次循环，结束后继续执行

```js
        let i = 1
        while (i <= 5) {
            if (i === 3) {
                i++
                continue
            }
            console.log(`我吃了${i}个包子`)
            i++
        }
```

> continue 是结束本次循环，结束后继续执行
>
> **`continue` 会跳过它后面的代码**。
> 如果 `i++` 写在 `continue` 后面，就不会执行，导致 `i` 不更新 → 死循环！



> 案例：存钱取钱

```js
let mon = 100
while(true){
    let re = +prompt(
        `
        请选择你所需要的操作：
        1.存钱
        2.取钱
        3.查看余额
        4.退出
        `
    )
    if(re === 4){
        break
    }
    switch(re){
        case 1 : 
            let cun = +prompt('请输入您要存的金额数')
            mon = mon + cun 
            break
        case 2: 
            let qu = +prompt('请输入您要取走的金额')
            mon = mon -qu
            break
        case 3: 
            alert(`您的存款是${mon}`)
            break
    }
}
```



##### 无限循环

while（true）/while（1）可以进行死循环，需要用 break 退出循环

for( ， ，) 也会死循环，同样需要用break退出死循环



### 数组

定义：一种按顺序保存数据的数据类型

作用：多个数据用数组保存，放到一个变量中，管理方便

#### 声明数组

1. 字面量声明数组

```js
        let arr = [1,2, 'wjm', 'true']
```

2. 使用new Array构造函数声明

```js
        let arr1 = new Array(1,2,'wzx')
```

> - 数组按顺序保存数据，每个数据有自己的编号（索引或下标）。
> - 计算机中编号从0开始，如小明为0，小刚为1。
> - 数组可存储任意类型的数据。

#### 遍历数组

定义：遍历数组就是从头到尾，一个一个查看或处理数组里的每个数据

语法：用`for`循环遍历数组里的每个数组

```js
for (let i = 0; i < 数组名.length; i++) {
    数组名[i]
}
```

```js
let nums = [10, 20, 30, 40, 50];
for (let i = 0; i < nums.length; i++) {
    document.write(nums[i]);
}
```

> 说明
>
> - 初始化 `i` 为 0。
> - 每次循环检查 `i` 是否小于数组长度。
> - 访问并处理 `nums[i]`，然后 `i` 自增。



#### 数组的增、删、查、改

- **查（查询数据）**：

  - `数组[下标]`：访问数组元素。

- **改（重新赋值）**：

  - `数组[下标] = 新值`：修改指定位置的元素。

  ```js
          let arr = []
          console.log(arr[0])        // undefined
          arr[1] = 2
          arr[2] = 3
          console.log(arr)
  ```

  ```js
          // 修改
          let arr = ['red','pink','blue']
          console.log(arr)      //['red', 'pink', 'blue']
          arr[0] = 'orange'
          console.log(arr)      //['orange', 'pink', 'blue']
  ```

  ```js
          let arr = ['pink','orange','blue']
          console.log(arr)          //['pink', 'orange', 'blue']
          
          for(let i = 0 ; i <= arr.length-1 ; i++){
              arr[i] = arr[i]+'老师'
          }
          console.log(arr)          //['pink老师', 'orange老师', 'blue老师']
  ```

- **增（添加数据）**：

  - `arr.push(新增内容)`：在末尾添加。

  ```js
          // 新增
          let arr = [2,8899,9034]
          console.log(arr)        //[2, 8899, 9034]
          arr.push(78787878,9876,'blackpink')
          console.log(arr)           //[2, 8899, 9034, 78787878, 9876, 'blackpink']
  ```

  - `arr.unshift(新增内容)`：在开头添加。

  ```js
          let arr = [23,982,35,6,435]
          console.log(arr)      //23, 982, 35, 6, 435]
          arr.unshift(45345,45235,234234)
          console.log(arr)      //[45345, 45235, 234234, 23, 982, 35, 6, 435]
  ```

  例子：数组筛选

  ```js
          let arr = [87,91,90,59,81,79,94,80]
          let newArr = []
          for(let i = 0 ; i <= arr.length-1 ; i++){
              if(arr[i]>=90){
                  newArr.push(arr[i])
              }
          }
          console.log(newArr)
  ```

- **删（删除数据）**：

  - `arr.pop()`：删除末尾元素。

  ```js
          let arr = [2,45,67,29]
          arr.pop()
          console.log(arr)
  ```

  - `arr.shift()`：删除开头元素。

  - `arr.splice(下标, 删除个数)`：从指定位置删除指定数量的元素。

    **`splice()` 方法：删除指定元素**

    - **语法**：

      ```js
      arr.splice(start, deleteCount)
      ```

      - `start`：起始位置（从0开始计数）
      - `deleteCount`：删除的元素个数（可选，默认删除到数组末尾）

    - **示例**：

      ```js
              let arr = [234,66,23,78,1,0,4]
              arr.splice(1,2)
              console.log(arr)        //[234, 78, 1, 0, 4]
      ```

> 案例：**数组求和/平均值**

```js
// 数组求和
let arr = [2,8,4,2,9]
let sum = 0

for(let i = 0 ; i <= arr.length-1 ; i++){
    sum += arr[i]
}

// //数组求和
console.log(sum)
// //数组平均值
console.log(sum / arr.length )

```

> 案例：**求数组最大值/最小值**

```js
let arr = [2,738,45,66,21,50]
let max = 0
let min = 0
for(let i = 1 ; i <= arr.length-1 ; i++){
    //最大值
    if(max < arr[i]){
        max = arr[i]
    }
    //最小值
    if(min > arr[i]){
        min = arr[i]
    }
}
console.log(max)
console.log(min)

```



#### 数组中的map方法

定义：用于对数组中的每个元素进行**转换操作**，并返回一个**新数组**，其长度与原数组相同。

##### ✅ 基本语法

```js
const newArray = array.map(function(element, index, array) {
  return element+'颜色';
});
console.log(newArray)
```

- **`element`**：当前遍历的元素
- **`index`**（可选）：当前元素的索引
- **`array`**（可选）：原数组
- **返回值**：一个由回调函数返回值组成的新数组

> 🚫 `map()` **不会修改原数组**，而是返回一个全新的数组。

##### 🔍 核心特点

| 特性             | 说明                                       |
| ---------------- | ------------------------------------------ |
| **纯函数式转换** | 每个元素一对一映射到新值                   |
| **不改变原数组** | 原数组保持不变（不可变性）                 |
| **返回新数组**   | 长度与原数组一致                           |
| **必须有返回值** | 回调函数中 `return` 的值将构成新数组的元素 |

> 案例：将字符串数组转为大写

```js
const fruits = ['apple', 'banana', 'orange'];

const upperFruits = fruits.map(fruit => fruit.toUpperCase());

console.log(upperFruits); // ['APPLE', 'BANANA', 'ORANGE']
console.log(fruits);      // ['apple', 'banana', 'orange']（原数组不变）
```



#### 数组的join方法

定义：`join()` 是 JavaScript 数组的一个内置方法，用于将数组中的所有元素**连接成一个字符串**。

数组-->字符串

##### ✅ 基本语法

```js
const str = array.join([separator]);
```

- **`separator`**（可选）：指定连接每个元素的分隔符。

  - 如果省略，默认使用英文逗号 `,`。
  - 可以是任意字符串（如 `'-'`、`' '`、`''` 等）。
  - 如果传入 `undefined` 或 `null`，也会被当作字符串处理（`"undefined"` 或 `"null"`）。

- **返回值**：一个由数组元素拼接而成的字符串。

  > 🚫 `join()` **不会修改原数组**，而是返回新字符串。

##### 🔍 核心特点

| 特性                                     | 说明                           |
| ---------------------------------------- | ------------------------------ |
| **返回字符串**                           | 所有元素被转换为字符串后拼接   |
| **可指定分隔符**                         | 自定义元素之间的连接符号       |
| **空数组返回空字符串**                   | `[]`.join() → `""`             |
| **`undefined` 和 `null` 被转为空字符串** | 但作为分隔符时会作为字符串处理 |

##### 🧪 基本示例

###### 1. 默认分隔符（逗号）

```js
const fruits = ['apple', 'banana', 'orange'];
const result = fruits.join();
console.log(result); // "apple,banana,orange"
```

###### 2. 自定义分隔符

```js
console.log(fruits.join('-'));   // "apple-banana-orange"
console.log(fruits.join(' '));   // "apple banana orange"
console.log(fruits.join(' | ')); // "apple | banana | orange"
console.log(fruits.join(''));    // "applebananaorange"（无分隔）
```

###### 3. 数字数组

```js
const numbers = [1, 2, 3, 4];
console.log(numbers.join(''));     // "1234"
console.log(numbers.join(' + '));  // "1 + 2 + 3 + 4"
console.log(numbers.join('0'));    // "1020304"
```

###### 4. 包含 `undefined` 或 `null` 的数组

```
const arr = ['a', undefined, 'c', null];
console.log(arr.join('-')); // "a--c-"（undefined 和 null 转为空字符串）
```

> ⚠️ 注意：`undefined` 和 `null` 作为**元素**时，会被转为空字符串；但作为**分隔符**时，会变成字符串 `"undefined"` 或 `"null"`。

```js
['a', 'b'].join(undefined); // "aundefinedb"
['a', 'b'].join(null);      // "anullb"
```

###### 5. 空数组

```js
console.log([].join('-')); // ""（空字符串）
```



##### 💡 实际应用场景

###### 1. 构造 URL 查询参数

```js
const params = ['name=Alice', 'age=25', 'city=Beijing'];
const queryString = params.join('&');
console.log(queryString); // "name=Alice&age=25&city=Beijing"
```

###### 2. 生成文件路径（跨平台注意）

```jsp
const pathParts = ['home', 'user', 'docs'];
const path = pathParts.join('/'); // Unix: "home/user/docs"
// 或 Windows: pathParts.join('\\') → "home\user\docs"
```

###### 3. 拼接 HTML 片段（简单场景）

```js
const items = ['Apple', 'Banana', 'Orange'];
const html = `<ul><li>${items.join('</li><li>')}</li></ul>`;
console.log(html);
// "<ul><li>Apple</li><li>Banana</li><li>Orange</li></ul>"
```

> ⚠️ 复杂 HTML 拼接建议使用模板引擎或 DOM 操作。

###### 4. 将数字数组转为连续字符串（如验证码）

```js
const code = [1, 2, 3, 4, 5, 6];
const pin = code.join(''); // "123456"
```

------

##### ✅ 与 `toString()` 的区别

| 方法             | 行为                                            |
| ---------------- | ----------------------------------------------- |
| `arr.join()`     | 可自定义分隔符                                  |
| `arr.toString()` | 固定使用逗号 `,` 分隔，等价于 `join()` 不传参数 |

```
[1, 2, 3].toString();     // "1,2,3"
[1, 2, 3].join();         // "1,2,3"
[1, 2, 3].join('-');      // "1-2-3" —— 只有 join 支持
```



##### ✅ 总结

> `join()` 的本质是：**“把数组变成字符串”**

- ✅ 用于将数组元素拼接为字符串
- ✅ 可自定义分隔符
- ✅ 不修改原数组
- ✅ 所有元素自动转为字符串
- ✅ `undefined` 和 `null` 元素转为空字符串



#### 数组总结

| 操作     | 推荐方法                                                     |
| -------- | ------------------------------------------------------------ |
| 添加元素 | `push()`（末尾）、`unshift()`（开头）                        |
| 删除元素 | `pop()`（末尾）、`shift()`（开头）、`splice(起始位置，删除个数)` |
| 查找元素 | `find() `（找**元素的索引**（位置），返回数字）、`indexOf()`、`includes()` |
| 遍历     | `for...of`、`map()`、`forEach()`                             |
| 转换     | `map()`、`filter()`、`reduce()`                              |
| 合并     | `concat()`、`[...arr1, ...arr2]`                             |
| 拷贝     | `[...arr]`、`slice()`、`structuredClone()`                   |



### 冒泡排序

定义：冒泡排序是一种通过重复比较相邻元素并交换位置，使较大元素像“冒泡”一样逐渐移到数组末尾的排序算法。

相邻两数比较，大的往后“冒”，每轮把最大数放到末尾。

> 外循环控制**轮数**（每轮冒出一个最大值），内循环负责**比较和交换**相邻元素。

```js
        let arr = [4,5,9,0,1]
        for(let i = 0 ; i <= arr.length-1 ; i++){
            for(let j = 0 ; j <= arr.length-i -1 ; j++){
                if(arr[j]>arr[j+1]){
                    let temp = arr[j]
                    arr[j] = arr[j+1]
                    arr[j+1] = temp
                }
            }
        }
        console.log(arr)           //[0, 1, 4, 5, 9]
```

**数组的 `sort()` 方法可以排序**

语法：

```js
let arr = [4, 2, 5, 1, 3];

// 1. 升序排列写法
arr.sort(function (a, b) {
    return a - b;
});
console.log(arr); // [1, 2, 3, 4, 5]

// 降序排列写法
arr.sort(function (a, b) {
    return b - a;
});
console.log(arr); // [5, 4, 3, 2, 1]
```

总结：

- `sort()` 方法用于对数组元素进行排序。
- 默认按字符串顺序排序，需自定义比较函数实现数字排序。
- **升序**：`return a - b`
- **降序**：`return b - a`



### 函数

**定义**：执行特定任务的代码块。

**作用**：封装相同或相似逻辑，便于复用和精简代码。

**示例**：`alert()`, `prompt()`, `console.log()` 是预封装的 JS 函数，直接调用即可。

**总结：**函数将代码“打包”，通过调用实现功能，如 `alert()` 显示提示框。



#### 函数的使用

##### **函数的声明语法：**

```js
function 函数名() {
    函数体
}
```

- **`function`**：关键字，用于定义函数。
- **`函数名`**：自定义的函数名称。
- **`()`**：参数列表（可为空）。
- **`{}`**：包含函数体，即执行的具体代码。



##### 函数有哪些声明方式？

1. 用function关键字定义一个带参数的函数
2. 将一个匿名函数赋值给变量的函数
3. 用箭头定义的函数
4. 构造函数的方式



##### 函数名命名规范：

- 和变量命名基本一致。
- 尽量使用小驼峰式命名法。
- 前缀应为动词。
- 命名建议：常用动词约定。



##### **函数的调用语法：**

```js
// 函数调用，这些函数体内的代码逻辑会被执行
函数名()
```

**注意：**

- 声明（定义）的函数必须调用才会真正被执行。
- 使用 `()` 调用函数。

**示例：**

```js
// 函数一次声明可以多次调用，每一次函数调用函数体里面的代码会重新执行一次
sayHi()
sayHi()
```

我们曾经使用的 `alert()`, `parseInt()` 这种名字后面跟小括号的本质都是函数的调用。



**函数体：**

**函数体是存放具体功能代码的地方，只有调用函数时这些代码才会运行**

- **定义**：函数的组成部分，用于“包裹”相同或相似的代码。
- **执行时机**：只有在调用函数时，函数体内的代码才会被执行。
- **位置**：所有实现函数功能的代码都写在函数体内。

**示例：**

```js
function sayHi() { // 函数体开始
    console.log('嗨~'); // 函数体内容
} // 函数体结束

sayHi(); // 调用函数，执行函数体内的代码
```

 求两个数的和

```js
        function sum (){
            let num1 = +prompt("请输入第一个数：")
            let num2 = +prompt("请输入第二个数：")
            console.log(num1 + num2)
        }
        sum()
```

1-100的累加和

```js
        function sum(){
            let getsum = 0
            for(let i = 1 ; i <= 100 ; i++){
                getsum = getsum +i
            }
            console.log(getsum)
        }
        sum()
```



#### 函数的参数

##### 动态参数`arguments`

定义：`arguments`是函数内部内置的**伪数组**变量

```js
function getSum() {
    let sum = 0;
    for (let i = 0; i < arguments.length; i++) {
        sum += arguments[i];
    }
    console.log(sum);
}

getSum(2, 3, 4);
getSum(1, 2, 3, 4, 2, 2, 3, 4);
```

特点：

1. `arguments`是一个伪数组，**只存在于函数中**
2. `arguments`的作用是动态互殴去函数的实参
3. 可以通过for循环依次得到传递过来的实参



##### 剩余参数 （. . .）

使用场景：用于获取多余的实参

特点：

1. `...`是语法符号，置于最末函数形参之前，用于获取多余的实参，**只存在于函数中**
2. 借助`...`获取的剩余实参，是个真数组
3. 开发中，提倡多使用**剩余参数**

基本语法：

```html
    <script>
        function arrA(...arr){
            console.log(arr)
        }
        arrA(1,12,4)
        arrA(1,12,4,456)
    </script>
```



##### `arguments`和 剩余函数 的区别

`arguments`是伪数组

剩余参数是真数组





#### 展开运算符

**定义**：**展开运算符（Spread Operator）** 也是用三个点 `...` 表示，但它与剩余参数的用法相反——用于“展开”数组或对象。

**作用**：展开数组或对象

**运用场景**：求数组最大值，合并数组

```js
// 求数组最大值/最小值
const arr = [1,23,4,66,80]
console.log(Math.max(...arr))   // 80
console.log(Math.min(...arr))   // 1

// 合并数组
const arr1 = [2,7,2]
const arr2 = [...arr1,...arr]
console.log(arr2)     // [2, 7, 2, 1, 23, 4, 66, 80]
```



##### 展开运算符 or 剩余参数

剩余参数：函数参数中使用，得到真数组

展开运算符：数组中使用，数组展开





#### 函数的传参

极大的提高了函数的灵活性

若函数完成功能需要调用者传入数据，那么就需要用有参数的函数。

##### **声明语法：**

```js
function 函数名(参数列表) {
    函数体
}
```

- **函数名**：自定义的函数名称。
- **参数列表**：用于接收外部传入的数据，多个参数用逗号隔开。
- **函数体**：包含具体执行的代码逻辑。



##### **参数列表：**

- 用于指定函数需要接收的数据。
- 多个数据用逗号分隔。

**示例：**

1. 计算平方：

   ```js
   function getSquare(num1) {
       document.write(num1 * num1);
   }
   ```

2. 计算和：

   ```js
   function getSum(num1, num2) {
       document.write(num1 + num2);
   }
   ```

**总结：**

- 参数列表允许函数接收外部数据。
- 函数体中使用这些参数进行计算或操作。

例子： x-x的累加和

```js
function num (start,end){
    let sum = 0
    for(let i = 1 ; i <= end ; i++){
        sum = sum + i
    }
    console.log(sum)
}
num(1,88)   //实参--调用的小括号里面
num(1,100)   //实参
```



##### 函数传参

> 函数可以分为形参和实参。
>
> 函数声明时，小括号里面的是形参，形式上的参数。
>
> 函数调用时，小括号里面的是实参，实际的参数。
>
> 尽量保持形参和实参的个数一致。

- **形参**：声明函数时，写在函数名右边小括号里的参数，相当于函数内部的变量。

  > 函数声明时小括号内的参数，相当于变量，用于**接收实参**。
  >
  > 如果没有传递实参，默认值为 `undefined`。

  - 示例：`function getSum(num1, num2)` 中的 `num1` 和 `num2`。

- **实参**：调用函数时，传入的具体值，给形参赋值。

  > 函数调用时小括号内的参数，可以是变量、常量或表达式，**实际传给形参的值**。

  - 示例：`getSum(10, 20)` 中的 `10` 和 `20` 分别赋值给 `num1` 和 `num2`。

- **形参和实参的关系**：

  - 形参是函数内的变量（如 `num1`）。
  - 实参是给这些变量赋的具体值（如 `10` 赋给 `num1`）。

- **开发建议**：尽量保持形参和实参个数一致，避免错误。

- **常见示例**：

  - `alert('打印')`、`parseInt('11')`、`Number('11')` 都是函数调用并传递实参的例子。



##### 参数默认值

这个默认值只会在缺少实参参数传递时才会被执行，所以有参数会优先执行传递过来的实参，否则默认为 `undefined`。

- **形参可以看作变量**，如果未传入实参，默认值为 `undefined`。

  - 示例：`getSum()` 调用时，`x` 和 `y` 都是 `undefined`，计算结果为 `NaN`。

- **改进方法**：给形参设置默认值（如 `0`），避免 `undefined` 导致的错误。

  - 示例代码：

    ```
    function getSum(x = 0, y = 0) {
        document.write(x + y);
    }
    ```

- **效果**：

  - `getSum()` 结果为 `0`（默认值相加）。
  - `getSum(1, 2)` 结果为 `3`（传入值相加）。



##### 函数返回值

函数内部不需要输入结果，而是**返回结果**

> - 当调用某个函数，这个函数会返回一个结果出来。
> - 这就是有返回值的函数。

- **内置函数有返回值**：
  - 如 `prompt('请输入你的年龄?')` 返回用户输入的字符串。
  - `parseInt('111')` 返回转换后的整数。
- **内置函数无返回值**：
  - 如 `alert('我是弹框，不需要返回值')` 只显示信息，不返回任何值。
- **根据需求设定**：
  - 自定义函数时，根据实际需要决定是否设置返回值。

```js
        // 函数的返回值
        function fn(){
            return 20
        }
        let re = fn()
        console.log(re)
```

> **return 作用**：将函数内部的执行结果传递给外部使用。
>
> **return 后代码不执行**：遇到 return 后，函数立即结束，后面的代码不会运行。因此，**return 后的数据不要换行写。**
>
> **无 return 的情况**：如果函数没有 return 语句，默认返回 `undefined`。

例子：

```js
        function getMax(x,y){
            return x > y ? x : y
        }
        let max = getMax(11,234)
        console.log(max)
```

* 求任意数组的最大值/最小值，并且返回

```js
        // 求任意数组的最大值/最小值，并且返回
        function getArr(arr = []) {
            let max = arr[0]
            let min = arr[0]

            for (let i = 1; i <= arr.length - 1; i++) {
                if (max < arr[i]) {
                    max = arr[i]
                }
                if (min > arr[i]) {
                    min = arr[i]
                }
            }
            return [max,min]
        }

        let max = getArr([1, 10, 5, 2, 9])
        console.log(max)

```



#### 函数的补充

两个相同的函数后面的会覆盖前面的函数。

```js
        // 函数的覆盖
        function fn(){
            console.log(1)
        }
        function fn(){
            console.log(2)
        }
        fn()    //2
```



在JavaScript中，实参的个数和形参的个数可以不一致：

- 如果形参过多，会自动填上 `undefined`（了解即可）。
- 如果实参过多，多余的实参会忽略（函数内部有一个 `arguments`，里面装着所有的实参）。

```js
        function fn (a,b){
            console.log(a+b)
        }
        // 实参多于形参    剩下的实参不参与计算
        fn(1,2,3)         //3
        // 实参少于形参     
        fn(1)             //1 + undefined = NaN
```



函数一旦碰到 `return` 就不会再往下执行了，**函数的结束用 `return`**。

> break 的结束和 return 的结束有什么区别？

break 的结束是结束循环，return 的结束是结束函数



#### 函数提升

定义：会把所有函数声明提升至当前作用域的最前面；只提升函数声明，不提升函数调用，不提升赋值。

![image-20251010090132418](./web-img/image-20251010090132418.png)

特点：

1. 函数提升能够使函数的声明调用更灵活
2. 函数表达式不存在提升的现象
3. 函数提升出现在相同作用域当中



### 箭头函数

**定义**：箭头函数简化了我们之前写的函数书写方式，他和之前函数表达式的创建函数行为是相同的。在任何使用函数表达式的地方，都可以使用箭头函数

```js
     //Es5
    let sum = function(a,b){
        return a + b;
    }
    // Es6
    let sum1 = (a,b) =>{
        return a + b;
    }
    console.log(sum(1,2));//3
    console.log(sum1(1,2));//3

```

#### 基本语法

```js
const fn = (x) => {
    console.log(x)
}
fn(1)
```

**单个参数可省略小括号**

```js
const fn = x => {
    console.log(x)
}
fn(1)
```

**单行代码可省略大括号**

```js
const fn = x => console.log(x)
fn(1)
```

**只有一行代码的时候，我们可以省略大括号**

```js
const fn = x => x + x
console.log(fn(1))
```

**单行返回对象要用括号包裹**

```js
// 错误：大括号被解释为代码块
const fn = x => { name: x, age: 20 } // 返回 undefined

// 正确：用括号包裹对象
const fn = x => ({ name: x, age: 20 })
console.log(fn('张三')) // {name: '张三', age: 20}
```



#### 箭头函数参数

**箭头函数没有`arguments`**

箭头函数也没有 `arguments` 变量。

当我们需要使用当前的 `this` 和 `arguments` 转发一个调用时，这对装饰器（decorators）来说非常有用。

例如，`defer(f, ms)` 获得了一个函数，并返回一个包装器，该包装器将调用延迟 `ms` 毫秒：

```js
js 体验AI代码助手 代码解读复制代码function defer(f, ms) {
  return function() {
    setTimeout(() => f.apply(this, arguments), ms)
  };
}

function sayHi(who) {
  alert('Hello, ' + who);
}

let sayHiDeferred = defer(sayHi, 2000);
sayHiDeferred("John"); // 2 秒后显示：Hello, John
```

不用箭头函数的话，可以用剩余函数去写：

```js
js 体验AI代码助手 代码解读复制代码function defer(f, ms) {
  return function(...args) {
    let ctx = this;
    setTimeout(function() {
      return f.apply(ctx, args);
    }, ms);
  };
}
```

在这里，我们必须创建额外的变量 `args` 和 `ctx`，以便 `setTimeout` 内部的函数可以获取它们。



#### 箭头函数没有 ' this ' 

定义：箭头函数没有`this`，如果访问`this`，则会从外部获取

使用它在对象内部进行迭代

```js
let group = {
  title: "Our Group",
  students: ["John", "Pete", "Alice"],

  showList() {
    this.students.forEach(
      student => alert(this.title + ': ' + student)
    );
  }
};

group.showList();

```

这里 `forEach` 中使用了箭头函数，所以其中的 `this.title` 其实和外部方法 `showList` 的完全一样。那就是：`group.title`。

如果我们使用正常的函数，则会出现错误：

```js
js 体验AI代码助手 代码解读复制代码let group = {
  title: "Our Group",
  students: ["John", "Pete", "Alice"],

  showList() {
    this.students.forEach(function(student) {
      // Error: Cannot read property 'title' of undefined
      alert(this.title + ': ' + student)
    });
  }
};

group.showList();
```

报错是因为 `forEach` 运行它里面的这个函数，但是这个函数的 `this` 为默认值 `this=undefined`，因此就出现了尝试访问 `undefined.title` 的情况。

但箭头函数就没事，因为它们没有 `this`。

> **不能对箭头函数进行 `new` 操作**
>
> 不具有 `this` 自然也就意味着另一个限制：箭头函数不能用作构造器（constructor）。不能用 `new` 调用它们。

> **箭头函数 VS bind**
>
> 箭头函数 `=>` 和使用 `.bind(this)` 调用的常规函数之间有细微的差别：
>
> - `.bind(this)` 创建了一个该函数的“绑定版本”。
> - 箭头函数 `=>` 没有创建任何绑定。箭头函数只是没有 `this`。`this` 的查找与常规变量的搜索方式完全相同：在外部词法环境中查找。





### 解构赋值

定义：可以将数组中的值或对象的属性取出，赋值给其他变量

#### 数组解构

定义： 数组解构是将**数组的单元值**快速批量**赋值**给**一系列变量**的简洁语法。

基本语法：

1. 赋值运算符 `=` 左侧的 `[]` 用于批量声明变量
2. **右侧数组的单元值**将被赋值给**左侧的变量**
3. 变量的顺序对应数组单元值的位置依次进行赋值操作

```html
<script>
    const arr = [100,60,80]
    const [max , min , arg] = arr
    console.log(max)
</script>
```



```js
// 交换两个变量
let a = 1;
let b = 2;   // 必须加分号
[b,a] = [a,b]
console.log(a,b)
```



变量多，单元值少，undefined

```js
const [a,b,c,d] = [1,2,3]
console.log(a)  // a
console.log(b)  // b
console.log(c)  // c
console.log(d)  // undefined
```



变量少，单元值多

```js
const [a,b] = [1,2,3]
console.log(a)  //1
console.log(b)  //2
```



剩余参数，变量少，单元值多

```js
const [a,b,...c] = [1,2,3]
console.log(a)  //1
console.log(b)  //2
console.log(c)  // [3,4]
```



防止undefined传递单元值的情况，可以设置默认值

```js
const [a = '手机', b = '华为'] = ['小米']
console.log(a) // 小米
console.log(b) // 华为
```



按需导入，忽略某些返回值

```js
const [a,b, ,d] = [1,2,3,4]
console.log(a)  // 1
console.log(b)  // 2
console.log(d)  // 4
```



二维数组

```js
// 二维数组
const arr = [1,2,[3,4]]
console.log(arr[0])   // 1
console.log(arr[1])   // 2
console.log(arr[2])   // [3,4]
console.log(arr[2][1])  //4
```



多维数组解构

```js
const [a,b,c] = [1,2,[3,4]]
console.log(a)  // 1
console.log(b)  // 2
console.log(c)  // [3,4]
```

```js
const [a,b,[c,d]] = [1,2,[3,4]]
console.log(a)  // 1
console.log(b)  // 2
console.log(c)  // 3
console.log(d)  // 4
```



补充：JavaScript 必须加分号的情况

1. 立即执行函数

```js
(function t() { })();
// 或者
;(function t() { })()
```

2. 数组解构

当数组开头，特别是前面有语句时，必须注意加分号：

```js
;[b, a] = [a, b]
```



#### 对象解构

定义：对象解构是将对象属性和方法快速批量赋值给一系列变量的简洁语法

基本语法：

1. 赋值运算符 `=` 左侧的 `{}` 用于批量声明变量，**右侧对象的属性值**将被赋值给**左侧的变量**
2. **对象属性的值**将被赋值给与**属性名相同的变量**
3. 注意解构的变量名不要和外面的变量名冲突，否则报错
4. 对象中找不到与变量名一致的属性时，变量值为 `undefined`

**对象解构的变量名 可以重新改名**

方法： 旧变量名：新变量名

```js
const{uname:username,age} = {uname:'pink老师',age:18}
```

**多级对象解构**

```js
const pig = {
    name:'佩奇',
    family:{
        mother:'猪妈妈',
        father:'猪爸爸',
        sister:'乔治'
    },
    age:6
}
// 多级对象解构
const {name,family:{mother,father,sister}} = pig
console.log(name)
console.log(mother)
console.log(father)
console.log(sister)
```



### forEach

定义：forEach () 方法用于调用数组的每个元素，并将元素传递给回调函数

使用场景： 遍历数组的每个元素；适合遍历数组对象

语法：

```js
被遍历的数组.forEach(function(当前数组元素，当前元素索引号){
    
})
```

```js
const arr = ['red','green','pink']
arr.forEach(function(item,index){
    console.log(item)
    console.log(index)
})
```

注意：forEach主要是遍历数组；参数当前数组元素必须要写的，索引号可选

 



### 作用域

**定义**：**限定名字**在程序中**有效和可用**的**代码范围**。

**作用**：提高程序逻辑的局部性，增强可靠性，减少名字冲突。

#### **全局作用域**：

定义：全局作用域中声明的变量，任何其他作用域都可以访问。

弊端：

> 1. 为 `window` 对象动态添加的属性默认也是全局的，**不推荐！**
> 2. 函数中未使用任何关键字（如 `let`、`const`、`var`）声明的变量会自动成为全局变量，**不推荐！！！**
> 3. 尽可能少地声明全局变量，防止全局变量被污染，影响程序稳定性与可维护性。

```js
<script>
  // 全局作用域
  // 全局作用域下声明了 num 变量
  const num = 10;

  function fn() {
    // 函数内部可以使用全局作用域的变量
    console.log(num); // 输出：10
  }

  // 此处仍是全局作用域
</script>
```

#### **局部作用域**：

###### 函数作用域

**定义**：在函数内部声明的变量只能在函数内部被访问，外部无法直接访问。且函数执行结束后局部变量会被销毁。

```js
<script>
function getSum() {
  // 函数内部是函数作用域，属于局部变量
  const num = 10
}
console.log(num) // 此处报错：函数外部不能使用局部作用域变量
</script>
```

**特点**：

> 1. 函数内部声明的变量，在函数外部无法被访问
> 2. 函数的参数也是函数内部的局部变量
> 3. 不同函数内部声明的变量无法互相访问
> 4. 函数执行完毕后，函数内部的变量实际被清空了



###### 块作用域

**定义**：块作用域（Block Scope）是指在**一对大括号** `{}` 所创建的**代码块**中**形成的作用域**。在块作用域中声明的变量或常量，只能在该**代码块**内部被访问，外部无法访问。

```js
for (let t = 1; t <= 6; t++) {
  // t 只能在该代码块中被访问
  console.log(t) // 正常
}
// 超出了 t 的作用域
console.log(t) // 报错
```

**特点**：

> 1. `let` 声明的变量会产生**块作用域**，`var` 不会产生块作用域
> 2. `const` 声明的常量也会产生块作用域
> 3. 不同代码块之间的变量无法互相访问
> 4. 推荐使用 `let` 或 `const` 声明变量



**变量的访问原则**

- 只要是代码，就至少有一个作用域。
- 写在函数内部的是局部作用域。
- 如果函数中还有函数，在这个作用域中又可以诞生一个作用域。
- 访问原则：在能够访问到的情况下先局部，局部没有再找全局。

> **特殊情况**：在函数内部，如果变量未声明直接赋值，会被视为全局变量（不推荐）。
>
> **例外情况**：函数内部的形参被视为局部变量

**作用域链**：采取就近原则的方式来查找变量最终的值





### 作用域链

**定义**：作用域链是由**当前执行环境**与**上层环境**（逐级向上）构成的层级结构，用于变量查找。作用域链本质是底层的变量查找机制

**规则**：（就近原则）

> 在函数被执行时，会优先查找当前函数作用域中查找变量
>
> 如果当前作用域查找不到则会依次逐级查找父级作用域指代全局作用域

**核心要点：**

- 作用域链是 JavaScript 实现变量查找的基础机制。
- 支持闭包、函数嵌套等高级特性。
- 遵循“由内向外”、“先近后远”的查找原则。



### 垃圾回收机制（GC）

**定义**：（不用的内存直接回收）js中内存的分配和回收都是自动完成的，内存在不适用的时候会被垃圾回收器自动回收

**内存的生命周期：**

1. **内存分配**：声明变量、函数、对象时，系统自动分配内存。
2. **内存使用**：读写变量、调用函数等操作。
3. **内存回收**：使用完毕后，由垃圾回收器自动释放不再使用的内存。

**说明**：

- 全局变量通常不会被回收（页面关闭才释放）。
- 局部变量不用了，一般会被自动回收。

⚠️ **内存泄漏**：程序分配的内存未释放或无法释放，导致内存占用持续增长。



#### 垃圾回收机制-算法说明

**堆栈空间分配区别：**

一般复杂数据类型由垃圾回收机制回收

1. **栈（操作系统）**
   - 由操作系统自动分配和释放。
   - 存放函数的参数值、局部变量等。
   - 基本数据类型（如 number、string、boolean）存储在栈中。
2. **堆（操作系统）**
   - 一般由程序员手动分配，若未释放，则由**垃圾回收机制回收。**
   - **复杂数据类型**（如对象、数组）存储在堆中。

**常见浏览器垃圾回收算法：**

引用计数法

标记清除法



##### **引用计数：**

定义：IE 使用的算法，判断对象是否“不再使用”：看是否有引用指向它。

规则如下：

1. 记录对象被引用的次数。
2. 每次被引用，计数 +1。
3. 引用减少，计数 -1。
4. 当引用次数为 0，释放内存。

✅ 简单说：**没被引用的对象 → 自动回收**。

**引用计数—弊端**

引用计数的致命问题：嵌套引用（循环引用）

```js
function fn() {
  let o1 = {};
  let o2 = {};
  o1.a = o2;      // o1 指向 o2
  o2.a = o1;      // o2 指向 o1
  return '引用计数无法回收';
}
fn();
```

原因：

1. 两个对象互相引用，彼此的引用次数永远不会为 0。

2. 引用计数算法无法判断它们是否“无用”，因此不会释放内存。

后果：引用计数法虽简单，但无法处理循环引用，是其主要缺陷。



##### 标记清除法

从根部扫描对象，能查找到的就是使用的，查找不到的就要回收

**定义**：将“不再使用的对象”定义为“**无法达到的对象**”。从根部（在 JS 中就是全局对象）出发，扫描内存中的对象。凡是能从根部到达的对象，都是**仍需使用**的。那些**无法从根部触及**的对象，被标记为不再使用，稍后进行回收。

![image-20251009151141979](./web-img/image-20251009151141979.png)

### 闭包

**定义**：**内层函数**和**外层函数的变量**一起构成了闭包

**基本格式**：

```js
// 里层函数 用到了 外层函数的变量才是闭包
function outer() {
  const a = 1;
  function f() {
    console.log(a);
  }
  f();
}
outer();

// 这个就没有闭包
function outer() {
  const a = 1;
  function f() {
    console.log(11);
  }
  f();
}
outer();
```

**作用**：封闭数据，提供操作，外部也可以访问函数内部的变量 

**闭包的作用**：

**实现共有变量**：在模块化开发中，闭包可以用来创建私有变量并暴露有限的公共接口，实现数据的封装和隔离。

**做缓存**：利用闭包可以存储计算结果，避免重复计算，提高程序效率。

**封装模块，防止全局变量污染**：通过闭包封装变量和函数，可以有效减少全局作用域的污染，保持代码的整洁和可维护性。

**弊端**：内存泄露

常见的闭包写法：外部可以访问使用函数内部的变量



**闭包应用：实现数据的私有化**

🎯 需求：

统计函数调用次数，每次调用 `count++`。

------

❌ 问题代码（不推荐）：（内存泄露）

```js
let count = 1; // 全局变量

function fn() {
  count++;
  console.log(`函数被调用${count}次`);
}

fn(); // 输出：函数被调用2次
fn(); // 输出：函数被调用3次
```

> ⚠️ 问题：`count` 是全局变量，容易被其他代码意外修改，导致数据不安全。（内存泄漏）

**什么是内存泄漏**？

**程序在运行过程中分配了内存，但未能正确释放，导致内存占用持续增加，最终影响性能甚至造成崩溃。**

------

✅ 改进方案（使用闭包实现私有数据）

```js
function fn() {
  let count = 1; // 局部变量，外部无法直接访问

  function fun() {
    count++;
    console.log(`函数被调用${count}次`);
  }

  return fun; // 返回内部函数
}

const result = fn(); // 获取返回的函数
result(); // 输出：函数被调用2次
result(); // 输出：函数被调用3次
```

------

✅ 优势：

- `count` 被封装在内部，**外部无法直接修改**。
- 实现了**数据私有化**，防止污染和误操作。
- 利用闭包特性，内部函数保留对外部变量的引用。



#### 变量提升

关键字：var

定义：把所有var声明的变量提升至**当前作用域**的最前面，**只提升声明，不提升赋值**

```js
var num;
console.log(num + '件');
num = 10;
console.log(num);
```

特点：

1. 变量在未声明即被访问时会报语法错误。
2. 变量在 `var` 声明之前被访问，其值为 `undefined`（变量提升）。
3. `let` / `const` 声明的变量不存在变量提升。
4. 变量提升只出现在相同作用域中。
5. 实际开发中推荐先声明再访问变量。



#### 匿名函数

##### **具名函数**：

- 声明时有名称（如 `function fn() {}`）。
- 可通过名称调用（如 `fn()`）。
- 具有**函数提升**（可在声明前调用）。

##### **匿名函数**：

- 声明时没有名称（如 `function() {}`）。
- 无法直接调用，必须**赋值给变量**或**作为参数传递**，或**立即执行**。

> ✅ **定义**：没有函数名的函数，也称为“无名函数”。

> ✅ **使用方式**：
>
> 1. **函数表达式**：赋值给变量使用。
> 2. **回调函数**：作为参数传递给其他函数（如 `setTimeout(fn, 1000)`）。
> 3. **立即执行函数（IIFE）**：定义后立即运行。

------

##### 写法

###### 函数表达式的写法

**函数表达式**：将匿名函数赋值给一个变量。调用时使用**变量名**。

```
let fn = function(a, b) {
    console.log('求和：', a + b);
};
```

**调用**：

```
fn(2, 3);  // 输出：求和：5
```

> ⚠️ **重要特点**：
>
> - **不会函数提升**：必须先声明，后调用。
>
> - 错误示例：
>
>   ```
>   fn();  // 报错：Cannot access 'fn' before initialization
>   let fn = function() { console.log('hello'); };
>   ```

> ✅ **参数使用**：支持形参、实参、默认值、剩余参数等，与具名函数完全相同。

------

✅ **补充说明（可选扩展）**

你还可以加一句：

> 💡 **小知识**：ES6 引入了**箭头函数** `() => {}`，它本质上也是一种匿名函数：
>
> ```
> let greet = () => console.log('Hello');
> greet();
> ```

------

✅ **总结**

你的原始笔记**完全正确**，只是可以稍作润色，使其更严谨、更完整。特别是强调：

- 匿名函数**不能提升**（与具名函数的重要区别）
- 函数表达式必须**先声明后使用**
- 匿名函数的三大用途：**赋值、传参、立即执行**



#### 立即执行函数

##### ✅ 定义

一个函数在**定义完成后立即执行**，不需要手动调用。

```js
(function() {
    console.log('我一出生就运行了！');
})();
```

------

##### ✅ 作用 / 优点

**用来创建私有作用域，防止变量污染全局**

1. **创建独立作用域**，避免变量泄露到全局，防止命名冲突。
2. **封装私有变量**，外部无法访问内部变量。
3. **避免污染全局命名空间**，尤其在早期 JS 模块化不成熟时非常重要。

```js
(function() {
    let secret = "这是私有的";
    // 外部无法访问 secret
})();
// console.log(secret); // 报错：secret is not defined
```

----

##### ✅注意事项

- **必须用分号 `;` 结尾**，否则多个 IIFE 连写可能出错：

  ```js
  (function(){})()
  (function(){})() // ❌ 报错：尝试把第二个函数当参数传给第一个
  ```

  ✅ 正确写法：

  ```js
  (function(){})();
  (function(){})();
  ```

- **不要再次调用**，因为它已经执行过了。

-------

##### ✅两种标准写法

###### 写法一：`(function(){})()` —— 更常见

```js
(function(x, y) {
    console.log(x + y);
})(1, 2); // 输出：3
```

###### 写法二：`(function(){}())` —— 也可用

```js
(function(x, y) {
    console.log(x + y);
}(1, 4)); // 输出：5
```

> 💡 两种写法功能完全相同，**第一种更推荐**，因为更清晰地表明“先定义，后调用”。

----

##### ✅补充：箭头函数也可以立即执行（ES6+）

```js
(() => {
    console.log('箭头函数版 IIFE');
})();

((name) => {
    console.log(`Hello, ${name}`);
})("小明");
```



> 案例：计算时分秒

- **小时**：`h = parseInt(总秒数 / 60 / 60 % 24)`
- **分钟**：`m = parseInt(总秒数 / 60 % 60)`
- **秒数**：`s = parseInt(总秒数 % 60)`

```js
    //计时器
    // 用户输入
    let second = +prompt('请输入秒数：')
    function getTime(t) {
        // - ** 小时 **：`h = parseInt(总秒数 / 60 / 60 % 24)`
        // - ** 分钟 **：`m = parseInt(总秒数 / 60 % 60)`
        // - ** 秒数 **：`s = parseInt(总秒数 % 60)`
        h = parseInt(t / 60 / 60 % 24)
        m = parseInt(t / 60 % 60)
        s = parseInt(t % 60)
        h = h< 10 ? '0'+h : h
        m = m < 10 ? '0' + m : m
        s = s < 10 ? '0' + s :s 
        return `转换完毕之后是${h}小时${m}分${s}秒`
    }
    let str = getTime(second)
    document.write(str)
```



#### 逻辑中断（**逻辑运算中的短路**）

- **短路**：只存在于 `&&` 和 `||` 中，当满足一定条件会让右边代码不执行。

| 符号 | 中断条件                            |
| ---- | ----------------------------------- |
| `&&` | 左边为 `false` 就中断，后面不再执行 |
| `||` | 左边为true就中断，后面不再执行      |

- **原因**：通过左边能得到整个式子的结果，因此没必要再判断右边。
- **运算结果**：无论 `&&` 还是 `||`，运算结果都是最后被执行的表达式值，一般用在变量赋值。

```js
        function fn(x,y){
            x = x || 0
            y = y || 0
            console.log(x+y)
        }
        fn(1,3)
        fn()
```

```js
        let age1 = 19
        console.log(true || age++)
        console.log(age1)
```

```js
        let age2 = 18
        console.log(11 && 22)     //都是真，这返回最后一个真值
        console.log(11 || 22)     //输出第一个真值 
```



### 构造函数

**定义**：把对象中公共的属性抽取出来，封装起来放到一个函数里，这个就是构造函数。一种特殊的函数，用来初始化对象。可以快速创建多个类似的对象

**作用**：可以快速创建多个类似的对象

**规定**：函数命名以大写字母开头；他们**只能**由 "**new**" 操作符来执行

**创建构造函数**：需要使用new关键字来调用构造函数，并将其赋值给一个变量即可

```js
function Pig(uname,age){
    this.uname = uname
    this.age = age
}
// console.log(new Pig('nihao',18))
const obj = new Pig('nihao',18)
console.log(obj)   // {uname: 'nihao', age: 18}
```

注意：

> 1. 使用**new关键字**调用函数的行为被称为**实例化**（变成了一个实际的对象）
>
> 2. 实例化构造函数时没有参数时可以省略（）
> 3. 构造函数内部无需写return，返回值即是新创造的对象
> 4. 构造函数内部的return返回的值无效，所以不要写return
> 5. new Object()  new Date() 也是实例化构造函数



#### 实例化执行过程

1. 创建新的空对象
2. 构造函数`this`指向新对象
3. 执行构造函数代码，修改`this`，添加新的属性
4. 返回新对象



#### 实例对象

定义：通过构造函数创建的对象称为实例对象

##### 实例成员

定义：**实例对象**中的**属性和方法**称为实例成员（实例属性和实例方法）

特点：

1. 为构造函数传入参数，创建结构相同但值不同的对象
2. 构造函数创建的实例对象彼此独立**互不影响**

```js
function Pig(name) {
    this.name = name
}

const peiqi = new Pig('佩奇')
const qiaozhi = new Pig('乔治')
peiqi.name = '小猪佩奇' // 实例属性
peiqi.sayHi = () => { // 实例方法
    console.log('nihao ')
}

console.log(peiqi)
console.log(qiaozhi)
console.log(peiqi === qiaozhi)
```



##### 静态成员

定义：**构造函数**的**属性和方法**被称为静态成员（静态属性和静态方法）

特点：

1. 静态成员只能构造函数来访问
2. 静态方法中的`this`指向构造函数。比如：`Date.now()`,`Math.PI`,`Math.random()`

```js
// 构造函数
function Person(name, age) {
    // 省略实例成员
}

// 静态属性
Person.eyes = 2
Person.arms = 2

// 静态方法
Person.walk = function () {
    console.log('^_^人都会走路...')
    // this 指向 Person
    console.log(this.eyes)
}
```



### 内置构造函数

**定义**：内置构造函数是编程语言在内部定义的特殊函数，它可以创建和初始化对象

**引用类型**：Object , Array , RegExp , Date等

**包装类型**：String , Number , Boolean等

**在 JavaScript 中最主要的数据类型有 6 种：**

基本数据类型：字符串、数值、布尔、undefined、null

引用类型：对象

**但是，我们会发现有些特殊情况：**

```js
// 普通字符串
const str = 'andy'
console.log(str.length) // 4
```

其实字符串、数值、布尔等基本类型也都有专门的构造函数，这些我们称为**包装类型**。
 JS 中几乎所有的数据都可以基于构造函数创建。



#### Object 

定义：`Object` 是 JavaScript 中的一个内置构造函数，用于创建**普通对象**。可以通过 `new Object()` 的方式来实例化一个对象。

```js
// 通过构造函数创建普通对象
const user = new Object({name:'小明',age:15})
```

######  静态方法

###### **`Object.keys(obj)`**

**作用**：获取对象中所有**可枚举属性的键名（key）**，返回一个字符串数组。

📌 语法：

```
Object.keys(obj)
```

📌 示例：

```js
const user = { name: '小明', age: 18, city: '北京' };
console.log(Object.keys(user)); 
// 输出: ['name', 'age', 'city']
```

- 只返回对象**自身的**、**可枚举**的属性。
- 不包括原型链上的属性。
- 返回的是一个**数组**，便于遍历或处理。

> ⚠️ 注意：`Symbol` 类型的键不会被包含。



###### **`Object.values(obj)`**

**作用**：获取对象中所有**可枚举属性的值（value）**，返回一个数组。

📌 语法：

```
Object.values(obj)
```

📌 示例：

```js
const user = { name: '小明', age: 18, city: '北京' };
console.log(Object.values(user)); 
// 输出: ['小明', 18, '北京']
```

- 与 `Object.keys()` 对应，返回的是值而不是键。
- 顺序与 `Object.keys()` 一致（按属性插入顺序）。

> ✅ 常用于快速提取所有字段值进行处理。



###### **`Object.assign() `**

**作用：** `Object.assign` 是一个静态方法，常用于**对象之间的拷贝**操作，可以将源对象的所有可枚举属性复制到目标对象上。

**示例：**

```js
const o = { name: 'wjm', age: 18 };

// 创建一个空对象，然后使用 Object.assign 进行拷贝
const oo = {};
Object.assign(oo, o);
console.log(oo); // { name: 'wjm', age: 18 }

// 向对象 o 添加新属性 gender
Object.assign(o, { gender: 'male' });
console.log(o); // { name: 'wjm', age: 18, gender: 'male' }
```



#### Arrey

**定义**：`Array` 是 JavaScript 内置的构造函数，用于**创建数组**。

```js
const arr = new Array(3, 5)
console.log(arr) // [3, 5]
```

> 创建数组建议使用**字面量语法**（如 `[3, 5]`），**不要使用 `Array` 构造函数**创建。

###### 数组常用方法对比表

| 方法      | 作用     | 说明                                                         |
| --------- | -------- | ------------------------------------------------------------ |
| `forEach` | 遍历数组 | 不返回新数组，经常用于查找或遍历数组元素                     |
| `filter`  | 过滤数组 | **返回新数组**，返回的是筛选满足条件的数组元素               |
| `map`     | 迭代数组 | **返回新数组**，返回的是处理之后的数组元素；想要使用返回的新数组 |
| `reduce`  | 累计器   | 返回累计处理的结果，经常用于求和等                           |

**数组常见方法**

| 序号 | 方法名      | 说明                                                         |
| ---- | ----------- | ------------------------------------------------------------ |
| 5.   | `join`      | 实例方法：将数组元素拼接为字符串，返回字符串（重点）         |
| 6.   | `find`      | 实例方法：查找元素，返回符合测试条件的第一个数组元素值；如果没有符合条件的则返回 `undefined`（重点） |
| 7.   | `every`     | 实例方法：检测数组所有元素是否都符合指定条件；如果**所有元素**都通过检测则返回 `true`，否则返回 `false`（重点） |
| 8.   | `some`      | 实例方法：检测数组中是否有元素满足指定条件；**如果数组中有元素满足条件**则返回 `true`，否则返回 `false` |
| 9.   | `concat`    | 实例方法：合并两个数组，返回生成的新数组                     |
| 10.  | `sort`      | 实例方法：对原数组单元值进行排序（会修改原数组）             |
| 11.  | `splice`    | 实例方法：删除或替换原数组中的元素（会修改原数组）           |
| 12.  | `reverse`   | 实例方法：反转数组（会修改原数组）                           |
| 13.  | `findIndex` | 实例方法：查找元素的索引值，返回第一个匹配元素的索引；如果没有匹配则返回 `-1` |

![image-20251011095814048](./web-img/image-20251011095814048.png)



```js
const numbers = [1, 2, 3, 4, 5];

// forEach：遍历，无返回值
numbers.forEach(num => console.log(num)); // 输出每个数字

// filter：过滤出偶数
const evens = numbers.filter(num => num % 2 === 0); // [2, 4]

// map：将每个数乘以 2
const doubled = numbers.map(num => num * 2); // [2, 4, 6, 8, 10]

// reduce：求和
const sum = numbers.reduce((acc, num) => acc + num, 0); // 15
```

###### Arrey.reduce()

**作用**：`reduce` 返回累计处理的结果，经常用于求和、累积计算等场景。

**reduce执行过程**

1. **如果没有起始值**，则“上一次值”以数组的第一个元素的值作为初始值。
2. **每一次循环**，把**返回值**作为下一次循环的“上一次值”。
3. **如果有起始值**，则该起始值作为第一次循环的“上一次值”。

```js
        // 数组reduce方法
        // arr.reduce(function(上一个值，当前值){}，初始值)
        const arr = [1,2,3]
        // 没有初始值
        const title = arr.reduce(function(prev,current){
            return prev+current
        })
        console.log(title)    // 6

        // 有初始值
        const total = arr.reduce(function(prev,current){
            return prev+current
        },10)
        console.log(total)   //16

        // 箭头函数
        const tatal = arr.reduce((prev,current) => prev+current,10)
        console.log(tatal)  // 16

```

###### Arrey.from()

伪数组转换为真数组

```html
<body>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>

    <script>
        const lis = document.querySelector('li')
        const liss = Array.from('li')
        console.log(liss)
    </script>
</body>
```



#### string

| 序号 | 方法/属性                                | 说明                                                         |
| ---- | ---------------------------------------- | ------------------------------------------------------------ |
| 1.   | `length`                                 | 实例属性：用于获取字符串的长度（重点）                       |
| 2.   | `split('分隔符')`                        | 实例方法：将字符串按指定分隔符拆分为数组（重点）             |
| 3.   | `substring(开始索引[, 结束索引])`        | 实例方法：用于截取字符串（不包含结束索引），从指定位置开始到结束位置前一个字符（重点） |
| 4.   | `startsWith(检测字符串[, 检测位置索引])` | 实例方法：检测字符串是否以某字符开头，返回 `true` 或 `false`（重点） |
| 5.   | `includes(搜索字符串[, 检测位置索引])`   | 实例方法：判断一个字符串是否包含在另一个字符串中，返回 `true` 或 `false`（重点） |
| 6.   | `toUpperCase()`                          | 实例方法：将字符串中的字母转换为大写                         |
| 7.   | `toLowerCase()`                          | 实例方法：将字符串中的字母转换为小写                         |
| 8.   | `indexOf()`                              | 实例方法：检测字符串是否包含某字符，返回首次出现的位置索引；未找到返回 `-1` |
| 9.   | `endsWith()`                             | 实例方法：检测字符串是否以某字符结尾，返回 `true` 或 `false` |
| 10.  | `replace()`                              | 实例方法：用于替换字符串中的内容，支持正则表达式匹配         |
| 11.  | `match()`                                | 实例方法：用于查找字符串，支持正则表达式匹配                 |

```js
const str = "Hello World";

// 1. length
console.log(str.length); // 11

// 2. split
// split 把字符串转换为数组，和 join 相反
console.log(str.split(" ")); // ['Hello', 'World']
console.log(str.split(""));  // ['H','e','l','l','o',' ','W','o','r','l','d']

// 3. substring
console.log(str.substring(0, 5)); // 'Hello'（从索引0到4）
console.log(str.substring(6));    // 'World'（从索引6到最后）

// 4. startsWith
console.log(str.startsWith("He")); // true
console.log(str.startsWith("Hi")); // false

// 5. includes
console.log(str.includes("ll"));   // true
console.log(str.includes("xyz"));  // false

// 6. toUpperCase / toLowerCase
console.log(str.toUpperCase()); // 'HELLO WORLD'
console.log(str.toLowerCase()); // 'hello world'

// 7. indexOf
console.log(str.indexOf("l"));    // 2（第一个'l'的位置）
console.log(str.indexOf("xyz"));  // -1（未找到）

// 8. endsWith
console.log(str.endsWith("ld"));  // true
console.log(str.endsWith("abc")); // false

// 9. replace
console.log(str.replace("World", "JavaScript")); // 'Hello JavaScript'
console.log(str.replace(/l/g, "X"));             // 'HeXXo WorXd'（使用正则替换所有'l'）

// 10. match
console.log(str.match(/l/g)); // ['l', 'l', 'l']（匹配所有'l'）
```

##### toString

**定义**：`toString` 是 JavaScript 中几乎所有对象都继承的一个方法，它用于将**一个值**转换为**字符串**表示

###### `Object.prototype.toString`

作用：返回一个表示该对象的字符串，格式为 `[object Type]`。

```js
Object.prototype.toString.call({})        // "[object Object]"
Object.prototype.toString.call([])        // "[object Array]"
Object.prototype.toString.call(new Date)  // "[object Date]"
Object.prototype.toString.call(/abc/)     // "[object RegExp]"
Object.prototype.toString.call(null)      // "[object Null]"
Object.prototype.toString.call(undefined) // "[object Undefined]"
```

说明：这个方法非常有用，常被用来**精确判断数据类型**，因为它不会被对象自身的 `toString` 方法覆盖（除非特意重写）。

**对象的`toString()`**

1. 如果`toString`接收的值是`undefined`，则返回“[object Undefined]"
2. 如果`toString`接收的值是`null`，则返回“[object Null]"

```js
let a={}
let b=[]
let c='hello'

console.log(Object.prototype.toString(a));//[object Object]
console.log(Object.prototype.toString.call(b)); //[object Array]
console.log(Object.prototype.toString.call(c));//[object String]

```

**为何`b`和`c`使用`Object.prototype.toString()`时为何同时使用了`call()`？**

直接调用数组和字符串实例的`toString`方法可能会受到对象原型上`toString`方法被覆盖的影响。而使用`Object.prototype.toString.call()`确保了调用的是最原始、未被修改的`toString`方法，提高了代码的稳定性和可靠性。

**数组的`toString()`**

```js
let arr=[1,2,3];
console.log(arr.toString());//"1,2,3"
```

数组的`toString()`方法是一个非常实用且内置的功能，它能够将数组中的所有元素转换成字符串形式，并用逗号`,`连接这些字符串，最后返回一个由这些字符串组成的单个字符串。这个过程简单直观，非常适合于需要将数组内容以易于阅读的文本格式展示的场景。

**其它的`toString()`**

```js
js 体验AI代码助手 代码解读复制代码//Number
let num = 123;
console.log(num.toString()); // 输出 "123"

//String
let str = "Hello";
console.log(str.toString()); // 输出 "Hello"

//Boolean
console.log(true.toString()); // 输出 "true"
console.log(false.toString()); // 输出 "false"

//函数function
let func = function() { return "Hello"; };
console.log(func.toString()); // 输出 "function (){ return "Hello"; }"
```

直接将值修改成字符串字面量





###### `Function.prototype.toString`

作用：这是**函数对象**特有的toString方法，返回一个表示该函数源代码的字符串

```js
function hello() {
  console.log("Hello");
}

hello.toString();
// 输出：
// "function hello() {
//   console.log("Hello");
// }"
```

说明：对于**内置构造函数**，这个方法会返回一个标准的、代表该函数的字符串，通常是 `[native code]`，表示它是用底层语言（如 C++）实现的，而不是 JavaScript 源码。

```js
Array.toString();
// 输出： "function Array() { [native code] }"

Number.toString();
// 输出： "function Number() { [native code] }"

Object.toString();
// 输出： "function Object() { [native code] }"
```



#### Number

定义：Number 是内置的构造函数，用于**创建数值** 常用方法

常用方法：

`toFixed() `设置保留小数位的长度

```js
// 数值类型
const price = 12.345
// 保留两位小数 四舍五入
console.log(price.toFixed(2)) // 12.35
```

 



### 处理`this`

没有明确指示指向`window`，严格模式下指向`undefined`

#### `this`指向

##### 普通函数

```js
// 普通函数
function sayHi() {
    console.log(this)
}

// 函数表达式
const sayHello = function () {
    console.log(this)
}
```

**调用方式与 this 值：**

- `sayHi()` → `this` 指向 `window`（非严格模式）
- `window.sayHi()` → `this` 指向 `window`

> **说明：** 当没有明确调用者时，普通函数在非严格模式下 `this` 指向全局对象（浏览器中为 `window`）。



###### 对象方法中的this

```js
// 普通对象
const user = {
    name: '小明',
    walk: function () {
        console.log(this)
    }
}

// 动态为 user 添加方法
user.sayHi = sayHi
user.sayHello = sayHello

// 调用方法
user.sayHi()
user.sayHello()
```

**结果：**

- `user.sayHi()` → `this` 指向 `user` 对象
- `user.sayHello()` → `this` 指向 `user` 对象

> **说明：** 当函数作为对象的方法被调用时，`this` 指向该对象。



###### 严格模式下的this

```js
<script>
'use strict'
function fn() {
    console.log(this) // undefined
}
fn()
</script>
```

**结果：**

- `fn()` → `this` 为 `undefined`

> **说明：** 在严格模式下，如果函数没有明确的调用者，`this` 不再指向 `window`，而是为 `undefined`。



1. **箭头函数会默认帮我们绑定外层 `this` 的值**
    → 所以在箭头函数中，`this` 的值和外层的 `this` 是一样的。
2. **箭头函数中的 `this` 引用的是最近作用域中的 `this`**
    → 它不会创建自己的 `this`，而是继承外部上下文的 `this`。
3. **向外层作用域中，一层一层查找 `this`，直到有 `this` 的定义**
    → 沿着作用域链向上查找，找到最近的 `this` 绑定。



##### 箭头函数

✅ **1. 箭头函数没有自己的 `this`**

- 它**不会创建独立的执行上下文**。
- 因此，**`this` 不由调用方式决定**（不像普通函数）。

------

✅ **2. `this` 继承自外层作用域（词法作用域）**

- 箭头函数中的 `this` 是**定义时所在作用域的 `this`**，而不是调用时的。
- 会**沿作用域链向上查找**，直到找到最近一个有 `this` 绑定的上下文。

------

✅ **3. 不受以下操作影响**

- 无法通过 `call()`、`apply()`、`bind()` 改变箭头函数的 `this`。
- 即使作为对象方法、事件回调或构造函数使用，`this` 依然保持定义时的值。

------

⚠️ **常见陷阱（不推荐使用箭头函数的场景）**

| 场景                        | 问题                                                 |
| --------------------------- | ---------------------------------------------------- |
| **对象方法**                | `this` 不指向对象本身，而是外层作用域（如 `window`） |
| **DOM 事件回调**            | `this` 指向 `window`，而非触发事件的元素             |
| **原型方法（`prototype`）** | `this` 无法绑定到实例，导致逻辑错误                  |
| **构造函数**                | 箭头函数不能作为构造函数（会报错）                   |

------

 **推荐使用场景**

- 数组方法中的回调（如 `map`、`filter`、`forEach`），需保留外层 `this`
- 定时器、Promise 回调等需要稳定 `this` 上下文的场合

```js
// DOM 节点
const btn = document.querySelector('.btn')

// 箭头函数：此时 this 指向 window
btn.addEventListener('click', () => {
    console.log(this) // 输出: window
})

// 普通函数：此时 this 指向 DOM 对象（即 btn）
btn.addEventListener('click', function () {
    console.log(this) // 输出: <button class="btn">...</button>
})
```





#### 改变this

##### `call()`了解

使用call方法调用函数，同时指定调用函数中this的值

`fun.call(thisArg,arg1,arg2,...)`

> thisAry：在fun函数运行时指定的this值
>
> arg1 , arg2 : 传递的其他参数
>
> 返回值就是函数的返回值，因为他就是调用函数

```js
<script>
const obj = {
    uname: 'pink'
}

function fn(x, y) {
    console.log(this) // window
    console.log(x + y)
}

// 1. 调用函数
// 2. 改变 this 指向
fn.call(obj, 1, 2)
</script>
```



##### `apply()`

使用apply方法调用函数，并指定`this`和参数（以数组形式），特别适用于处理数组参数的场景

`fun.apply(thisArg, [argsArray])`

1. **`thisArg`**
   - 在 `fun` 函数运行时指定的 `this` 值。
   - 即：调用函数时，`this` 指向的对象。
2. **`argsArray`**
   - 传递给函数的参数，**必须是一个数组**（或类数组）。
   - 如果没有参数，可以传 `null` 或省略。
3. **返回值**
   - 返回的是被调用函数的返回值。
   - 因为 `apply` 本质是调用函数，所以返回结果与直接调用函数一致。

```js
    <script>
        const obj = {
            name:'nihao'
        }
        function fn(x,y){
            console.log(this)
            console.log(x+y)
        }
        fn.apply(obj,[1,2])
        // 返回值 本身就是再调用函数，多以返回值就是函数的返回值

        
        // 求数组最大值
        const arr = [100,22,85]
        const max = Math.max.apply(Math,arr)   // 100 
        console.log(max)
        console.log(Math.max(...arr))
    </script>

```



##### `bind()`

`bind()`方法不会调用函数，但是能改变函数内部`this`指向

`fun.bind(thisArg,arg1,arg2,...)`

1. **`thisArg`**
   - 在 `fun` 函数运行时指定的 `this` 值。
   - 即：调用函数时，`this` 指向的对象。
2. **`arg1, arg2, ...`**
   - 传递给函数的预设参数（可选）。
   - 这些参数会被“绑定”到新函数中，在调用时自动传入。

 **返回值**：

- 返回一个**由指定 `this` 值和初始参数改造后的原函数拷贝（新函数）**。
- 这个新函数在调用时会使用绑定的 `this` 和参数。

**使用场景**：

当我们**只想改变 `this` 指向，但不立即调用函数**时，可以使用 `bind`。

```js
document.querySelector('button').addEventListener('click', function () {
    // 禁用按钮
    this.disabled = true;

    // 使用 setTimeout 延迟 2 秒后启用按钮
    window.setTimeout(function () {
        // 在这个普通函数里面，我们要将 this 由原来的 window 改为 btn
        this.disabled = false;
    }.bind(this), 2000);
});
```

1. **`this` 的问题**
   - 外层事件回调函数中的 `this` 指向按钮元素（DOM 对象）。
   - 但 `setTimeout` 中的回调是普通函数，其 `this` 默认指向 `window`，导致无法正确操作按钮。
2. **使用 `.bind(this)` 解决**
   - `.bind(this)` 将 `setTimeout` 回调函数中的 `this` 绑定到外层的 `this`（即按钮元素）。
   - 这样在定时器执行时，`this.disabled = false` 能正确作用于按钮。
3. **效果**
   - 点击按钮 → 立即禁用（`disabled = true`）
   - 2 秒后 → 自动启用（`disabled = false`）



#### **`call`、`apply` 和 `bind` 的对比总结**

------

##### ✅ **相同点：**

- 都可以**改变函数内部的 `this` 指向**。

------

##### 🔍 **区别点：**

1. **`call` 和 `apply` 会调用函数，并且改变函数内部 `this` 指向。**
   - 执行函数并立即运行。
2. **`call` 和 `apply` 传递参数的方式不同：**
   - `call`：参数以 **逗号分隔的形式** 传递（如 `arg1, arg2, ...`）。
   - `apply`：参数必须以 **数组形式** 传递（如 `[arg1, arg2, ...]`）。
3. **`bind` 不会调用函数，但可以改变函数内部 `this` 指向。**
   - 返回一个**绑定好 `this` 和参数的新函数**，需手动调用。

------

##### 🎯 **主要应用场景：**

- **`call`**
   → 调用函数并传递参数，适用于需要立即执行且参数为独立值的场景。

- **`apply`**
   → 经常与数组配合使用，例如借助 `Math.max()` 或 `Math.min()` 求数组的最大/最小值：

  ```js
  const nums = [1, 5, 3, 9];
  Math.max.apply(null, nums); // 等价于 Math.max(1, 5, 3, 9)
  ```

- **`bind`**
   → 不调用函数，但希望提前绑定 `this` 上下文。
   → 常用于：

  - 改变定时器内部的 `this` 指向
  - 事件处理中保持上下文
  - 创建“预设”函数对象





### 面向对象编程（oop）

定义：面向对象是把事务分解成为一个个对象，然后由对象之间分工与合作

说明：在面向对象程序开发思想中，每一个对象都是功能中心，具有明确分工 

功能：面向对象是以对象功能来划分问题，而不是步骤

面向对象的特性：封装性，继承性，多态性

 

#### **面向过程编程**

**优点：**

性能比面向对象高

适合与硬件联系紧密的系统，例如单片机就采用面向过程编程

**缺点：**

不如面向对象易维护、易复用、易扩展

------

#### **面向对象编程**

**优点：**

易维护、易复用、易扩展

具有封装、继承、多态等特性

可设计出低耦合的系统，使系统更加灵活、易于维护

**缺点：**

性能比面向过程低

| 特性         | 面向过程编程                     | 面向对象编程               |
| ------------ | -------------------------------- | -------------------------- |
| **性能**     | 高                               | 相对较低                   |
| **适用场景** | 硬件相关、嵌入式系统（如单片机） | 复杂应用、大型软件系统     |
| **可维护性** | 差                               | 好（封装、继承、多态支持） |
| **复用性**   | 差                               | 好                         |
| **扩展性**   | 差                               | 好                         |

> JS实现面向对象需要借助**构造函数**来实现
>
> 构造函数存在浪费内存的问题





### 原型

#### 原型

公共的属性写到构造函数里；公共的方法写到原型对象身上

**定义**：是一个对象，将prototyoe称为**原型对象**

**作用**：共享方法；可以把那些不变的方法，直接定义在prototype对象上

构造函数和原型里面的this指向：实例化的对象

```js
let that;
function Person(name) {
    this.name = name;
    that = this;
}
const o = new Person();
console.log(that === o); // true
```

```js
let that;
function Person(name) {
    this.name = name;
}
Person.prototype.sing = function () {
    that = this;
}
const o = new Person();
o.sing();
console.log(that === o); // true
```



案例：给数组方法，求最大值，最小值，求和

```js
// 最大值
const arr = [1, 2, 3]
Array.prototype.max = function (arr) {
    return Math.max(...this)
    // 原型函数里面的this指向 实例对象arr
}
console.log(arr.max())

// 最小值
Array.prototype.min = function () {
    return Math.min(...this)
}
console.log(arr.min())

// 求和
Array.prototype.sum = function () {
    return this.reduce((prev, item) => prev + item, 0)
}
console.log([1, 2, 3].sum())
```



#### constructor属性

作用：该属性指向该对象的构造函数。

![image-20251013091806428](./web-img/image-20251013091806428.png)

```js
function Star(){
}
const ni = new Star()
console.log(Star.prototype.constructor === Star)   // true
```

当为构造函数的原型对象（`prototype`）添加多个方法时，**推荐使用对象字面量形式赋值**，例如：

```js
Person.prototype = {
    method1: function() {},
    method2: function() {}
};
```

但这样会带来一个问题：
 👉 **原来的 `constructor` 属性会被覆盖**，导致 `Person.prototype.constructor` 不再指向 `Person` 构造函数，而是指向 `Object`。

------

🛠️ **解决方案**：

在重新赋值的原型对象中，**手动添加一个 `constructor` 属性**，使其指向原来的构造函数：

```js
Person.prototype = {
    constructor: Person, // 修复 constructor 指向
    method1: function() {},
    method2: function() {}
};
```

------

🔍 为什么重要？

- `constructor` 是用于识别对象是哪个构造函数创建的。
- 如果不修复，可能会导致类型判断或继承链出错。
- 特别是在使用 `instanceof` 或需要访问构造函数时，`constructor` 的正确性很重要。

---

案例：

```js
function Star(){
}
const ni = new Star()
console.log(Star.prototype.constructor === Star)   // true
console.log(Star.prototype)
Star.prototype = {
// 从新只会创造这个原型对象的构造函数
    constructor:Star,
    sing:function(){
        console.log('唱歌')
    },
    dance:function(){
        console.log('跳舞')
    }
}
console.log(Star.prototype)

```



#### 对象原型

**定义**：对象中都会有一个属性`_proto_`指向构造函数的`prototype`原型对象，之所以我们对象可以使用构造函数`prototype`原型对象的属性和方法，就是因为对象有对象原型的存在

**作用**：每一个对象都会有一个对象原型`_proto_`，对象原型指向的是该构造函数的原型对象`prototype`

![image-20251013101604902](./web-img/image-20251013101604902.png)



总结：

1. **`__proto__` 是非标准属性**
   - 它是浏览器实现中的一个“非标准”属性（虽然广泛支持），用于访问对象的原型。
   - 标准写法是通过 `Object.getPrototypeOf(obj)` 来获取原型。
2. **`[[Prototype]]` 与 `__proto__` 意义相同**
   - `[[Prototype]]` 是 JavaScript 引擎内部使用的、不可直接访问的机制。
   - `__proto__` 是它的**可访问表现形式**，两者都指向对象的原型对象。
3. **作用：指向实例对象的原型**
   - 每个对象都有一个 `__proto__`，它指向其构造函数的 `prototype` 对象。
   - 例如：`new Person()` 创建的对象，其 `__proto__` 指向 `Person.prototype`。
4. **`__proto__` 的原型中也有 `constructor` 属性**
   - 即：`obj.__proto__.constructor` 通常指向创建该对象的构造函数。
   - 例如：`p.__proto__.constructor === Person`，说明 `p` 是由 `Person` 构造函数创建的。

```js
function Star() { }

const ldh = new Star();

// 对象原型 __proto__ 指向构造函数的原型对象
console.log(ldh.__proto__);

// console.log(ldh.__proto__ === Star.prototype)

// 对象原型里面有 constructor 指向构造函数 Star
console.log(ldh.__proto__.constructor);
```



**原型对象、对象原型的区别 / 关系**

| 名称     | 对应属性                                          | 是什么？                                                     |
| -------- | ------------------------------------------------- | ------------------------------------------------------------ |
| 原型对象 | `构造函数.prototype`                              | 是一个普通的对象，由构造函数提供，用来存放所有实例共享的属性和方法。 |
| 对象原型 | `实例.__proto__` 或 `Object.getPrototypeOf(实例)` | 是每个对象内部的一个指针，指向它的“原型”，也就是它从哪里继承属性和方法。 |

关系：对象原型`__proto__`指向构造函数的原型对象`prototype`



#### 原型继承

定义：继承是面向对象编程的另一个特征，通过继承进一步提升代码封装的程度

案例：

```js
// 用构造函数写，new出来的对象，结构一样，但是对象不一样，另外两个构造函数的方法之间就互不影响
function People () {
    this.eyes = 2
    this.head = 1
    this.ears = 2
}
function Woman() {

}
// Woman 通过原型继承people
Woman.prototype = new People
// 原来的构造函数被覆盖，指回原来的构造函数
// 子类（子构造函数）；父类（父构造函数）
// 子类的原型 = new 父类
Woman.prototype.constructor = Woman
// 给Woman实例化
const woman = new Woman()
// 添加一个方法
Woman.prototype.baby = function(){
    console.log('baby')
}
console.log(woman)

function Man() {

}
// Man 通过原型继承people
Man.prototype = new People
// 原来的构造函数被覆盖，指回原来的构造函数
Man.prototype.constructor = Man
const man = new Man()
console.log(man)
```



#### **原型链**

定义：基于原型对象的继承使得不同构造函数的原型对象关联在一起，并且这种关联的关系是一种链状结构，我们将原型对象的链状结构关系称为原型链

每个对象都有一个内部属性 `[[Prototype]]`（可通过 `__proto__` 或 `Object.getPrototypeOf()` 访问）

<img src="./web-img/image-20251013163416623.png" alt="image-20251013163416623" style="zoom: 67%;" />

当访问一个对象的属性或方法时：

- 先在对象自身查找；
- 找不到就去它的原型（`__proto__`）上找；
- 还找不到，就继续往上找原型的原型，直到 `null` 为止。

这个链条就是 **原型链**。

规则：JavaScript 在访问属性时，会沿着对象 → 原型 → Object.prototype → null 的链路逐级查找，直到找到或结束，`__proto__` 是这条链的指针，`instanceof` 用于判断原型关系。



#### `instanceof`运算符

**定义**：`instanceof` 是 JavaScript 中的一个**二元运算符**，用于检测一个对象是否是某个构造函数（或类）的实例。它通过检查**原型链**来判断对象的类型。

```js
对象 instanceof 构造函数
// 如果该对象是这个构造函数的实例，返回 true
// 否则返回 false
```

**案例**：

```js
// 定义一个构造函数
function Person(name) {
    this.name = name;
}

const alice = new Person("Alice");

console.log(alice instanceof Person); // true
console.log(alice instanceof Object);  // true，因为所有对象都继承自 Object
```

**工作原理**：从左边的对象开始，沿着 `__proto__` 链向上查找，看是否能找到右边构造函数的 `prototype`。

```js
alice instanceof Person
// 等价于检查：
Person.prototype.isPrototypeOf(alice)
// 或者：alice.__proto__ === Person.prototype（或在其原型链中）
```

**注意**：

1. 只适用于对象和函数
2. 在多窗口或多框架页面中可能出错
3. Es6 `class` 也适用

**实际用途**：

1. 判断对象类型（比 `typeof` 更精确，尤其对数组、自定义对象）
2. 类型校验、错误处理、多态编程

**总结**：`instanceof` 是用来判断“**这个对象是不是由某个构造函数（或类）创建的**”，它通过原型链进行查找，是 JavaScript 中实现类型判断的重要工具。









### 对象

定义：对象是一种数据类型，一种无序的数据集合

* 是JavaScript里的**一种数据类型**

* 可以理解为一种**无序的数据集合**，注意数组是有序的数据集合
* 如果用多个变量保存则比较松散，用对象比较统一

**特点**:无序的数据集合，可以详细的描述某个事物



#### 创建对象

1. 利用对象字面量创建对象

```js
const obj = new Object()
obj.uname = '123'
console.log(obj)
```

2. 利用`new Object`创建对象，内置对象

```js
const i = new Object({name:'你好'})
console.log(i)
```

3. 利用构造函数创建对象

```js
```





#### 对象使用

##### 对象声明语法

```js
let 对象名 = {}
```

```js
let 对象名 = new Object()
```

空对象 `null === let obj = { }`

##### 对象由属性和方法组成

属性：信息或叫特征

方法：功能或叫行为

```js
let 对象名 = {
    属性名: 属性值,
    方法名: 函数
}
```

**定义**：描述对象特征的信息称为属性，通常是名词性（如姓名、年龄等）。

**特点**：

- 属性由**属性名和值**组成，用 `:` 分隔。
- 多个属性间用 `,` 分隔。
- 属性是依附在对象上的变量。

**命名规则**：

- 属性名可用 `""` 或 `''` 包裹，但一般省略。
- 特殊符号（如空格、中横线）需加引号。

```js
        let wjm = {
            uname:'wjm',
            age:18,
            gender:'nan'
        }
        console.log(wjm)        //{uname: 'wjm', age: 18, gender: 'nan'}
```



##### 操作对象的方式

###### 对象的增、删、改、查

**属性-查**

**定义**：声明对象并添加属性后，使用 `.` 可以获取对象中属性的值，称为属性访问。

**语法**：`对象名.属性`

**作用**：简单地获取对象内部的属性值。

```js
        let obj = {
            name : 'wjm',
            age:18,
            hobby:'dance'
        }
        console.log(obj.name)    //wjm
```

查的另外一种属性

```js
对象名['属性名']
console.log(obj['goods-name'])
```

**总结：**

1. 对象名 . 属性名
2. 对象名['属性名']



**属性-改**

**语法：**`对象名.属性 = 新值`

这表示可以通过 `对象名.属性` 的形式给对象的某个属性赋新值，从而修改该属性的值

```js
        let obj = {
            name : 'wjm',
            age:18,
            hobby:'dance'
        }

        obj.name = 'wzx'
        console.log(obj);     //{name: 'wzx', age: 18, hobby: 'dance'}
```



**属性-增**

**语法：对象名.新属性 = 新值**

这表示可以通过 `对象名.新属性 = 新值` 的形式给对象添加一个新属性，并为其赋值。

```js
        let obj = {
            name : 'wjm',
            age:18,
            hobby:'dance'
        }
        obj.gender = 'nan'
        console.log(obj)          //{name: 'wjm', age: 18, hobby: 'dance', gender: 'nan'}
```



**属性-删（了解**）

**语法**：`delete 对象名.属性`

```js
let person = {
    uname: 'pink老师',
    age: 18,
    gender: '女'
}

delete person.gender // 删除 gender 属性
console.log(person)    //{uname: 'pink老师', age: 18}
```



#### 属性和方法

```js
let person = {
  // 属性（描述对象的特征）
  name: "小明",
  age: 18,

  // 方法（对象能做的事）
  sayHello: function() {
    console.log("你好，我是" + this.name);
  }
};
```

##### 属性

定义：属性是对象中的**变量**，用来描述对象的“状态”或“特征”

格式：`键: 值`（key: value）

✅ 示例：

```js
let car = {
  brand: "丰田",     // 字符串
  year: 2022,        // 数字
  isUsed: true,      // 布尔值
  owner: null        // 空值
};
```

✅ 访问属性

```
console.log(car.brand);  // "丰田" —— 点语法
console.log(car["year"]); // 2022 —— 括号语法（可用于动态访问）
```

✅ 修改属性

```
car.year = 2023;
car.color = "红色"; // 添加新属性
```



##### 对象中的方法

**定义**：对象中描述行为的信息称为方法，通常是动词性（如跑步、唱歌），本质是函数。

**特点**

1. 方法由**方法名和函数**两部分构成，用 `:` 分隔。
2. 多个属性间用 `,` 分隔。
3. 方法是依附在对象中的函数。
4. 方法名一般省略引号，除非名称包含特殊符号（如空格、中横线等）。

```js
        let obj = {
            uname:'wjm',
            age:function(x,y){
                console.log(x+y)
            },
            gender:function(a){
                console.log(a*a)
            }
        }
        obj.age(2,7)    //9
        obj.gender(4)   //16
```

声明对象并添加方法后，可以通过 `.` 调用对象中的函数，称为**方法调用**。方法还可以包含形参和实参

这样可以执行对象内的特定功能，并传递参数。



#### 遍历对象

在 JavaScript 中，对象是由**键值对**组成的集合，但与数组不同，它不具备一些数组的特性，因此不能用 `for` 循环像遍历数组那样直接遍历对象。

🔹 **为什么不能像数组一样遍历对象？**

1. **没有 `length` 属性**：

   对象不提供 `length` 属性来表示属性的数量，无法通过下标或长度控制循环。

2. **无序的键值对**：

   对象中的键值对是无序的，没有固定的顺序或规律。这与数组不同，数组有按顺序排列的下标。

##### 遍历对象 for in

```js
        let obj = {
            uname:'wjm',
            age:18,
            gender:'女'
        }
        // 遍历对象
        for(let k in obj){
            // console.log(k)   //属性名  'uname' 'age' 'gender'
            // console.log(k.uname)    //undefined
            console.log(obj[k])   //因为 k === 'uname',所以要 [k]  // 输出属性值：'wjm', 18, '女'
        }
```





#### 内置对象

定义：JavaScript 语言本身提供的一些**自带的对象**，无需手动创建或引入，可以直接使用其属性和方法。

🔹 常见内置对象概览

| 内置对象   | 主要用途                                       |
| ---------- | ---------------------------------------------- |
| `Object`   | 所有对象的基类，用于操作键值对对象             |
| `Array`    | 数组操作（如 `push`, `map`, `filter` 等）      |
| `String`   | 字符串处理（如 `slice`, `indexOf`, `replace`） |
| `Number`   | 数值类型转换与判断（如 `isNaN`, `parseInt`）   |
| `Boolean`  | 布尔值封装对象（较少直接使用）                 |
| `Date`     | 处理日期和时间                                 |
| `Math`     | 提供数学常数和函数（静态方法）                 |
| `RegExp`   | 正则表达式匹配文本                             |
| `Error`    | 错误对象基类（如 TypeError, SyntaxError）      |
| `Function` | 函数对象，所有函数的实例                       |

> 注意：这些对象大多数是“构造函数”或“静态对象”，其中 **`Math` 是唯一一个不能用 `new` 创建实例的静态对象**。这些对象大多数是“构造函数”或“静态对象”，其中 **`Math` 是唯一一个不能用 `new` 创建实例的静态对象**。



##### 内置对象math

定义：`Math` 是一个**静态对象**，所有方法和属性都通过 `Math.xxx` 直接调用，**不能实例化**。

```js
Math.PI     // 圆周率 π ≈ 3.14159
Math.E      // 自然对数的底 e ≈ 2.718
```

常用方法

| 方法                | 功能说明                               | 示例                      |
| ------------------- | -------------------------------------- | ------------------------- |
| `Math.random()`     | 返回 `[0, 1)` 之间的随机数（含0不含1） | `Math.random()` → `0.342` |
| `Math.floor(x)`     | 向下取整（舍去小数）                   | `Math.floor(2.9)` → `2`   |
| `Math.ceil(x)`      | 向上取整（进一位）                     | `Math.ceil(1.1)` → `2`    |
| `Math.round(x)`     | 四舍五入                               | `Math.round(1.5)` → `2`   |
| `Math.max(a,b,...)` | 返回最大值                             | `Math.max(3, 5, 1)` → `5` |
| `Math.min(a,b,...)` | 返回最小值                             | `Math.min(3, 5, 1)` → `1` |
| `Math.pow(x, y)`    | 幂运算：x 的 y 次方                    | `Math.pow(2, 3)` → `8`    |
| `Math.abs(x)`       | 返回绝对值                             | `Math.abs(-5)` → `5`      |
| `Math.sqrt(x)`      | 开平方根                               | `Math.sqrt(16)` → `4`     |

> 案例：随机整数

```js
// 生成 [min, max] 范围内的随机整数
function getRandom(min, max) {
    return Math.floor(Math.random() * (max - min + 1)) + min;
}
console.log(getRandom(1, 10)); // 输出 1 到 10 之间的整数
```



##### 内置对象Date

定义：用于获取、设置、格式化当前或指定的时间。

```js
let now = new Date();           // 当前时间
let date = new Date("2025-04-05"); // 指定日期
```

获取时间的方法（基于本地时区）

| 方法            | 返回值          | 注意事项                       |
| --------------- | --------------- | ------------------------------ |
| `getFullYear()` | 年份（如 2025） | ✅ 推荐使用                     |
| `getMonth()`    | 月份（0–11）    | ⚠️ 需要 +1 才是实际月份         |
| `getDate()`     | 日期（1–31）    | —                              |
| `getDay()`      | 星期几（0–6）   | 0 表示周日，1~6 表示周一到周六 |
| `getHours()`    | 小时（0–23）    | —                              |
| `getMinutes()`  | 分钟（0–59）    | —                              |
| `getSeconds()`  | 秒（0–59）      | —                              |

其他常用方法

| 方法                                | 作用                                                        |
| ----------------------------------- | ----------------------------------------------------------- |
| `getTime()`                         | 返回自 1970年1月1日0:00:00 UTC 到现在的**毫秒数**（时间戳） |
| `toString()`                        | 将日期转为可读字符串                                        |
| `toLocaleString()`                  | 格式化为本地时间字符串（推荐显示用）                        |
| `toDateString()` / `toTimeString()` | 分别获取日期部分和时间部分                                  |

```js
let timestamp = new Date().getTime(); // 获取当前时间戳
console.log(timestamp); // 如：1748421120000
```

> 💡 小提示：`getMonth()` 和 `getDay()` 返回值从 0 开始，使用时注意转换





##### 随机数函数

定义：是用来**生成随机数**的函数

**常用方法：`Math.random()`**

###### 1. `Math.random()`

这是 JavaScript 内置的随机数生成函数，它返回一个 **大于等于 0 且小于 1** 的伪随机浮点数（由算法生成看起来是随机的小数）。

```
console.log(Math.random()); // 例如：0.844592375923759
```

- 返回值范围：**0 ≤ 结果 < 1**
- 是**伪随机数**（由算法生成，非真正随机）
- 不能单独使用，需结合其他数学运算生成指定范围的数

---

###### 2. 生成指定范围的随机数

**生成 [min, max) 之间的浮点数（包含 min，不包含 max）**

```js
function getRandomFloat(min, max) {
    return Math.random() * (max - min) + min;
}

console.log(getRandomFloat(1, 10)); // 例如：5.342
```

**生成 [min, max] 之间的整数（包含 min 和 max）**

```js
function getRandomInt(min, max) {
    min = Math.ceil(min);
    max = Math.floor(max);
    return Math.floor(Math.random() * (max - min + 1)) + min;
}

console.log(getRandomInt(1, 10)); // 例如：7
```

🔍 **解释**：

> - `Math.random() * (max - min + 1)`：生成 0 到 (max-min+1) 的数
> - `Math.floor(...)`：向下取整得到整数
> - `+ min`：将范围平移到 min 到 max 之间

----

###### 3. 常见用途示例

```js
// 随机颜色
function getRandomColor() {
    return `rgb(${getRandomInt(0, 255)}, ${getRandomInt(0, 255)}, ${getRandomInt(0, 255)})`;
}

// 随机布尔值（真假）
function getRandomBoolean() {
    return Math.random() >= 0.5;
}

// 从数组中随机选取一个元素
function getRandomItem(arr) {
    return arr[getRandomInt(0, arr.length - 1)];
}
```

------

###### ⚠️ 注意事项

- `Math.random()` 生成的是**伪随机数**，不适用于加密或安全敏感的场景。
- 如果你需要加密级安全的随机数，应使用 Web Crypto API 中的 `crypto.getRandomValues()`。

```js
// 安全的随机整数（用于加密等场景）
function getCryptoRandomInt(min, max) {
    const array = new Uint32Array(1);
    crypto.getRandomValues(array);
    return array[0] % (max - min + 1) + min;
}
```

----

> 案例：

如何随机生成0-10 的随机数

```js
        function getNum(){
            return Math.floor(Math.random() * (10 + 1))
        }
        console.log(getNum())
```

如何随机生成5-10 的随机数

```js
        function getnum(){
            return Math.floor(Math.random() * (5 + 1)) + 5
        }
        console.log(getnum())
```

取到N-M的随机整数

```js
        function getRandom(N,M){
            return Math.floor(Math.random() * (M - N + 1)) + N
        }
        console.log(getRandom(5,7))
```

随机点名

```js
        // 随机点名
        let uname = ['wjm','wzx','lx','gmy','zjq','hsj','jzh']
        let random = Math.floor(Math.random()*uname.length)
        console.log(uname[random])
```

猜数字游戏 

```js
        // 猜数字游戏
        function getRandom(N,M){
            return Math.floor(Math.random() *(M-N+1))+N
        }
        let random = getRandom(1,10)
        console.log(random)
        while(true){
            let num = +prompt('请输入你猜的数字：')
            if(num > random){
                alert('您猜大了')
            }else if(num < random){
                alert('您猜小了')
            }else{
                alert('猜对啦，真厉害')
                break
            }
        }
```

声称随机颜色

```js
        // 生成随机颜色
        function getcolor(flag){
            if(flag){

            }else{
                let r = Math.floor(Math.random()*256)
                let g = Math.floor(Math.random()*256)
                let b = Math.floor(Math.random()*256)
                return `rgb(${r},${g},${b})`
            }
        }
        console.log(getcolor(false))
```



### JavaScript 数据类型与内存机制

#### 核心术语解释

| 术语                     | 含义说明                                               | 示例                                                         |
| ------------------------ | ------------------------------------------------------ | ------------------------------------------------------------ |
| **关键字**               | 在 JS 中具有特殊语法意义的词，不能用作变量名或函数名   | `let`, `var`, `function`, `if`, `else`, `for`, `switch`, `break` 等 |
| **保留字**               | 当前未使用，但未来可能成为关键字的词，**建议避免使用** | `int`, `char`, `long`, `short`（来自其他语言）               |
| **标识符（Identifier）** | 变量名、函数名、属性名等的统称                         | 如 `userName`, `getData`, `obj`                              |
| **表达式（Expression）** | 能“产生一个值”的代码片段，常包含运算符                 | `10 + 5`, `age >= 18`, `x * y`, `"hello" + "world"`          |
| **语句（Statement）**    | 一段可执行的完整代码，通常以分号结束                   | `if (x > 0) { ... }`, `for(...)`, `let a = 10;`              |



#### JavaScript 数据类型概览

JS 数据类型分为两大类：

| 类型                         | 特点                                                     | 常见类型                                                     |
| ---------------------------- | -------------------------------------------------------- | ------------------------------------------------------------ |
| **基本数据类型（值类型）**   | 按值访问，存储在**栈内存**中，赋值是**值的拷贝**         | `String`, `Number`, `Boolean`, `Null`, `Undefined`, `Symbol`, `BigInt` |
| **复杂数据类型（引用类型）** | 按引用访问，实际数据在**堆内存**中，变量保存的是**地址** | `Object`, `Array`, `Function`, `Date`, `RegExp`, `Map`, `Set` |



##### 基本数据类型（值类型）

✅ 7 种原始类型（Primitive Types）

| 类型              | 说明                             | 示例                                  |
| ----------------- | -------------------------------- | ------------------------------------- |
| `String`          | 字符串                           | `"hello"`, `'world'`                  |
| `Number`          | 数字（整数和小数）               | `42`, `3.14`, `-10`                   |
| `Boolean`         | 布尔值                           | `true`, `false`                       |
| `Null`            | 空值（表示“无”）                 | `null`                                |
| `Undefined`       | 未定义（变量声明但未赋值）       | `let x; console.log(x)` → `undefined` |
| `Symbol` (ES6)    | 唯一且不可变的值，用于对象属性键 | `Symbol('id')`                        |
| `BigInt` (ES2020) | 表示任意精度的大整数             | `123n`, `BigInt(100)`                 |

- **值类型（简单类型）**：直接存储具体值，包括 `string`、`number`、`boolean`、`undefined` 和 `null`。例如：

  ```js
  let a = 5; // 存储的是数字5本身
  ```

- **不可变性**：基础类型的值不能被改变，任何“修改”都会创建新值。
- **按值比较**：两个基础类型变量比较的是它们的值。

```js
let a = 10;
let b = a;
b = 20;
console.log(a); // 10 → a 没有被改变

let str = "hello";
str[0] = "H"; // 无效，字符串不可变
console.log(str); // "hello"
```



##### 复杂数据类型（引用类型）

✅ 常见引用类型

| 类型         | 说明             | 示例                          |
| ------------ | ---------------- | ----------------------------- |
| `Object`     | 对象             | `{ name: "Tom" }`             |
| `Array`      | 数组             | `[1, 2, 3]`                   |
| `Function`   | 函数             | `function() {}` 或 `() => {}` |
| `Date`       | 日期对象         | `new Date()`                  |
| `RegExp`     | 正则表达式       | `/abc/`, `new RegExp("abc")`  |
| `Map`, `Set` | ES6 新增集合类型 | `new Map()`, `new Set()`      |

- **可变性**：对象的内容可以被修改。
- **按引用赋值**：赋值时赋值的是**引用地址**，而不是数据本身。
- **按引用比较**：`==` 或 `===` 比较的是引用地址，不是内容。

```js
let obj1 = { name: "Tom" };
let obj2 = obj1;
obj2.name = "Jerry";
console.log(obj1.name); // "Jerry" → obj1 被改变了！

let arr1 = [1, 2, 3];
let arr2 = arr1;
arr2.push(4);
console.log(arr1); // [1, 2, 3, 4] → arr1 也被改变了
```

```
// 即使内容相同，不同对象也不相等
console.log({} === {}); // false
console.log([1,2] == [1,2]); // false
```

示例代码和图解： 

```js
let usrObj = {}
```

```js
let b = new Array(); // 存储的是数组的地址，实际数组内容在堆内存中
```



#### 堆栈

##### 一、基本概念

JavaScript 的内存空间主要分为三种：

1. **栈（Stack）**：由操作系统自动分配和释放，用于存放**原始数据类型**和**函数调用上下文**。
2. **堆（Heap）**：用于存储**复杂数据类型（引用类型）**的对象，内存空间较大但管理更复杂。
3. **队列（Queue）**：主要用于事件循环（Event Loop），不在本篇重点。

> ⚠️ 注意：这里的“栈”和“堆”指的是**内存区域**，不是数据结构中的“栈”或“堆”。

------

##### 二、栈（Stack）

###### ✅ 特点

- **后进先出（LIFO）**
- 存取速度快
- 空间较小
- 自动分配和释放
- 存储**原始值（Primitive values）** 和**函数执行上下文**

##### ✅ 存储内容

1. **原始数据类型**：
   - `undefined`, `null`, `boolean`, `number`, `string`, `symbol`, `bigint`
   - 这些值直接存储在栈中
2. **函数调用栈（Call Stack）**：
   - 每次函数被调用时，会创建一个“执行上下文”（Execution Context）
   - 上下文包含变量、参数、this 等信息，压入调用栈
   - 函数执行完毕后，上下文从栈中弹出

##### ✅ 示例：原始值赋值（按值传递）

```
let a = 10;
let b = a;  // 复制的是值
b = 20;

console.log(a); // 10
console.log(b); // 20
```

> ✅ 变量 `a` 和 `b` 各自拥有独立的栈空间。

------

##### 三、堆（Heap）

###### ✅ 特点

- 动态分配内存
- 空间大，但访问速度较慢
- 用于存储**引用类型对象**
- 内存管理由垃圾回收机制（GC）负责

###### ✅ 存储内容

所有**引用类型（Reference Types）** 都存储在堆中：

- `Object`
- `Array`
- `Function`
- `Date`
- `RegExp`
- 等等

> 💡 实际上，**变量名（标识符）仍然在栈中**，它保存的是指向堆中对象的**引用地址**。

###### ✅ 示例：引用类型赋值（按引用传递）

```
let obj1 = { name: "Alice" };
let obj2 = obj1;        // 复制的是引用地址
obj2.name = "Bob";

console.log(obj1.name); // "Bob"
console.log(obj2.name); // "Bob"
```

> ❌ `obj1` 和 `obj2` 指向堆中同一个对象，修改一个会影响另一个。

------

##### 四、堆与栈的对比表

| 对比项   | 栈（Stack）                | 堆（Heap）             |
| -------- | -------------------------- | ---------------------- |
| 存储内容 | 原始类型、函数执行上下文   | 引用类型对象           |
| 分配方式 | 自动分配，快速             | 动态分配，较慢         |
| 管理方式 | 先进后出，函数结束自动释放 | 手动/垃圾回收（GC）    |
| 访问速度 | 快                         | 慢                     |
| 空间大小 | 小（有限）                 | 大（动态扩展）         |
| 数据共享 | 不共享                     | 多个变量可引用同一对象 |
| 赋值行为 | 按值传递                   | 按引用传递             |

------

##### 五、常见问题解析

###### 1. 为什么对象是引用传递？

因为对象实际存储在堆中，变量只是保存了它的“地址”。多个变量赋值时，复制的是地址，而非整个对象。

###### 2. 如何实现深拷贝？

避免引用共享，需手动创建新对象：

```js
// 方法1：JSON 序列化（仅适用于简单对象）
let newObj = JSON.parse(JSON.stringify(obj));

// 方法2：展开运算符（浅拷贝）
let newObj = { ...obj };

// 方法3：递归深拷贝函数（推荐处理复杂结构）
function deepClone(obj) {
  if (obj === null || typeof obj !== 'object') return obj;
  if (obj instanceof Date) return new Date(obj);
  if (obj instanceof Array) return obj.map(item => deepClone(item));
  if (typeof obj === 'object') {
    let cloned = {};
    for (let key in obj) {
      if (obj.hasOwnProperty(key)) {
        cloned[key] = deepClone(obj[key]);
      }
    }
    return cloned;
  }
}
```

------

##### 六、调用栈（Call Stack）示例

```js
function first() {
  console.log("First");
  second();
}

function second() {
  console.log("Second");
  third();
}

function third() {
  console.log("Third");
}

first();
// 输出：
// First
// Second
// Third
```

###### 调用过程：

1. `first()` 被调用 → 压入栈
2. `second()` 被调用 → 压入栈
3. `third()` 被调用 → 压入栈
4. `third()` 执行完 → 弹出
5. `second()` 执行完 → 弹出
6. `first()` 执行完 → 弹出

> 🔁 如果递归太深，会导致 **栈溢出（Stack Overflow）**

------

##### 七、总结

| 关键点                    | 说明                     |
| ------------------------- | ------------------------ |
| 原始类型 → 栈             | 直接存储值，赋值独立     |
| 引用类型 → 堆（引用在栈） | 存储对象，变量保存地址   |
| 赋值时注意引用共享        | 修改一个可能影响其他变量 |
| 深拷贝必要时使用          | 避免意外修改             |
| 调用栈管理函数执行顺序    | LIFO 结构，防止无限递归  |

------

📌 **一句话记住**：

> “**小而快的数据放栈里，大而复杂的对象放堆里，变量只是通往它们的钥匙。**”



### 拷贝

#### 浅拷贝

**定义**：

拷贝的是对象的第一层属性

简单数据类型：直接拷贝值

引用数据类型：拷贝的地址

**常见实现方式**

对象：`{...obj}`、`Object.assign({}, obj)`

数组：`[...arr]`、`arr.concat()`、`arr.slice()`

**特点**：

✅ 一层属性修改互不影响（基本类型）。

❌ 多层嵌套时，深层引用类型仍共享地址，修改会**相互影响**。、

**方法**：

1. `Object.create`：主要用于实现原型继承，但他也可以视为一种特殊的浅拷贝，新对象的原型被设置为原对象

   ```js
   let obj = {
       a:1
   }
   let obj2 = Object.create(obj)
   obj.a=2
   console.log(obj2.a);     // 输出2
   ```

   ```
   obj2
     └── [[Prototype]] → obj
                         └── a: 2   ← 被修改了
   ```

2. `Object.assign`：将源对象的可枚举属性复制到目标对象，适合合并多个对象

   ```js
   let obj={
       a:1,
       b:[1,2,3]
   }
   let obj1 = Object.assign({},obj)
   obj.b.push(4)
   console.log(obj1);      //输出{ a: 1, b: [ 1, 2, 3, 4 ] }
   ```

3. `Array的concat、slice、解构赋值`：如`[].concat(arr)`、`arr.slice(0)`、`[...arr]`，这三个方法都会返回一个新的数组，`[].concat(arr)`通过与空数组连接，`arr.slice(0)`对数组从0开始分割，`[...arr]`将数组解构重新赋值，都是对数组进行浅拷贝。

   ```js
   let arr=[1,2,3,{a:1}]
   let arr1=arr.slice(0)
   let arr2=[...arr]
   let arr3=[].concat(arr)
   arr[3].a=2
   console.log(arr1);//[ 1, 2, 3, { a: 2 } ]
   console.log(arr2);//[ 1, 2, 3, { a: 2 } ]
   console.log(arr3);//[ 1, 2, 3, { a: 2 } ]
   ```

4. `Array的toReversed().reverse()`: `arr.toReversed()`会将原数组倒序后返回一个新的数组，通过先反转再反转数组来实现浅拷贝，非直观但有效。

   ```js
   let arr=[1,2,3,{a:1}];
   let arr2=arr.toReversed().reverse();
   arr[3].a=2;
   console.log(arr2);//输出[ 1, 2, 3, { a: 2 } ]
   ```



#### 深拷贝

深拷贝拷贝的是对象，不是地址

实现一个深拷贝函数通常需要递归地检查每个属性，如果属性值是对象，则递归调用自身进行拷贝；否则，直接复制该属性值。这种方法灵活性高，可以处理更多特殊情况，但实现相对复杂。

**常用方法**：

1. 通过递归实现深拷贝
2. `lodash`，`cloneDeep`
3. 通过`JSON.stringify()`实现

**作用**：使得新对象与原对象完全独立，互不影响。

**注意**：使用 JSON.stringify() 和 JSON.parse() 进行深拷贝时，会忽略 undefined、Symbol 和函数等特殊值。

```js
let obj = {
    name: '我真的很困',
    like: {
        type: 'coding',
        a: undefined,
        b: null,
        c: function () {
            console.log('hello');
        },
        e: Symbol('hello'),
// acef都拷贝不了
    }
}
let newObj= JSON.parse(JSON.stringify(obj))
console.log(newObj);

```

![image-20251014095944707](./web-img/image-20251014095944707.png)



**`JSON.parse(JSON.stringify(obj))`**

1. **无法识别BigInt类型**：当对象中包含BigInt类型的值时，这个方法会将其转换为字符串，因为JSON标准不支持BigInt类型。因此，复制后的对象中的BigInt值不再是BigInt，而是字符串。

2. **无法拷贝`undefined`、`function`、`Symbol`属性**：

- `undefined`的属性值会被忽略，因为它不是JSON格式的一部分。
- 函数（`function`）作为对象的属性不能被序列化，所以在解析后会丢失。
- `Symbol`作为键或值同样不会被处理，因为JSON.stringify会忽略Symbol类型的键，且Symbol值也不能被直接序列化。

3. **无法处理循环引用**：如果对象结构中存在循环引用（即对象A的某个属性引用了对象B，同时对象B的某个属性又引用了对象A），`JSON.stringify`会抛出错误，因为它无法正确地序列化这样的结构。

```js
let obj={
    a:1,
    b:{n:2},
    c:'cc',
    d:true,
    e:undefined,
    f:null,
    g:function(){},
    h:Symbol(1)
}

let newObj=JSON.parse(JSON.stringify(obj))
console.log(newObj)//{ a: 1, b: { n: 2 }, c: 'cc', d: true, f: null }
obj.b.n=1
console.log(newObj)//{ a: 1, b: { n: 2 }, c: 'cc', d: true, f: null }
//实现了深度拷贝，但是没有拷贝`undefined`、`function`、`Symbol`
```



**`structuredClone(obj)`**

它能完美地克隆大多数值，包括循环引用，但兼容性需考虑。

```js
let obj={
    a:1,
    b:{n:1}
}

const newObj=structuredClone(obj);
obj.b.n=3
console.log(newObj);//{ a: 1, b: { n: 1 } }
```



**自定义deepCopy函数**

```js
let obj = {
    a: 1,
    b: { n: 2 },
    c: 'cc',
    d: true,
    e: undefined,
    f: null,
    g: function () { },
    h: Symbol(1),
    i: [1, 2, 3]
}
function deepCopy(obj) {
    let newObj = {}
    for (let key in obj) {
        if (obj.hasOwnProperty(key)) {
            //obj[key]是不是对象 typeof obj[key] === 'object'&& obj[key] !== null
            if (obj[key] instanceof Object) {
                newObj[key] = deepCopy(obj[key])
            } else {
                newObj[key] = obj[key]
            }
        }
    }
    return newObj
}
let obj2= deepCopy(obj);
console.log(obj2);
obj.i[0]=0
console.log(obj2);
/*输出结果：
{
  a: 1,
  b: { n: 2 },
  c: 'cc',
  d: true,
  e: undefined,
  f: null,
  g: {},
  h: Symbol(1),
  i: { '0': 1, '1': 2, '2': 3 }
}
{
  a: 1,
  b: { n: 2 },
  c: 'cc',
  d: true,
  e: undefined,
  f: null,
  g: {},
  h: Symbol(1),
  i: { '0': 1, '1': 2, '2': 3 }
}
*/
```



**js库 lodash 里面 cloneDeep 内部实现了深拷贝**

```js
const obj = {
    uname: 'pink',
    age: 18,
    hobby: ['篮球', '足球'],
    family: {
        baby: '小pink'
    }
}

// 语法：_.cloneDeep(要被克隆的对象)
const o = _.cloneDeep(obj)

console.log(o)
o.family.baby = '老pink'
console.log(obj)
```

- 使用 `_.cloneDeep()` 对对象 `obj` 进行**深拷贝**。
- 深拷贝会递归地复制所有嵌套的属性，包括数组和对象。
- 修改副本 `o` 中的 `family.baby` 不会影响原对象 `obj`。
- 因此，`console.log(obj)` 输出的 `baby` 仍然是 `'小pink'`。

`lodash.cloneDeep()`

能正确处理：

- 原始值（string, number, boolean）
- 数组、对象
- `BigInt`、`Date`、`RegExp`
- 循环引用（部分版本支持）



### 递归函数

**定义**：如果一个函数在内部可以调用其本身，那么这个函数就是递归函数

**理解**：函数在执行过程中调用自己，“自己调用自己”

**作用**：递归函数的作用与循环类似，常用于处理具有重复结构的问题

**注意**：递归容易导致“**栈溢出**”错误，因为每次调用函数都会压入调用栈；**必须设置退出条件**（通常通过`return`实现），否则会无限递归，最终报错

> **递归是函数调用自身，需有明确的退出条件，否则会导致栈溢出。**

错误案例：

```js
function fn() {
  fn(); // 没有退出条件
}
fn();
```

案例：

```js
let i = 1
function fn() {
    console.log(`这是第${i}次`)
    if(i >= 6){
        return
    }
    i++
    fn()
}
fn()

```



#### 函数递归

利用递归函数实现`setTimeout`模拟`setInterval`效果

```html
<body>
    <div></div>
    <script>
        function time(){
            document.querySelector('div').innerHTML = new Date().toLocaleString()
            setTimeout(time,1000)
        }
        time()
    </script>
</body>

```



### 异常处理

#### `throw`抛异常

**定义**：异常处理是指预估**代码执行过程中**可能发生的错误，然后最大程度的避免错误的发生导致整个程序无法继续进行

**特点**：

1. `throw`抛出异常信息，程序也会**终止执行**
2. `throw`后面跟的是错误提示信息
3. `Error`对象配合`throw`使用，能够设置更详细的错误信息

```js
function fn(x,y){
    if(!x || !y){
        throw new Error('参数不能为空')
    }
}
fn()
```



#### `try` /` catch` 捕获错误信息

浏览器提供

关键字：`try`,`catch`,`finally`

```js
        function fn(){
            try{
                // 可能发送错误代码，要写到try
                const p = document.querySelector('.p')
                p.style.color = ' red'
            }catch(err){
                // 拦截错误，提示浏览器提供的错误信息，但是不中断程序的执行
                console.log(err.message)
                throw new Erray('你看看')
                // 需要加return 中断程序
                // return
            }
            finally{
                // 不管程序对不对，一定会执行的代码
                console.log('321')
            }
            console.log('弹出对话框')
        }
        fn()
```

特点：

1. **`try...catch` 用于捕获错误信息**
   - `try...catch` 是 JavaScript 中处理异常的核心语法结构，用来捕获运行时发生的错误。
2. **将预估可能发生错误的代码写在 `try` 代码段中**
   - 把可能出错的代码（如文件读取、网络请求、类型转换等）放在 `try` 块中执行。
3. **如果 `try` 代码段中出现错误后，会执行 `catch` 代码段，并截获到错误信息**
   - 当 `try` 块中的代码抛出异常（如 `Error`、`TypeError` 等），程序不会崩溃，而是跳转到 `catch` 块。
   - `catch` 可以接收错误对象，例如：`catch(err)`，可获取错误类型和消息。
4. **`finally` 不管是否有错误，都会执行**
   - `finally` 块无论是否发生错误，都会被执行一次。
   - 常用于资源释放、关闭连接、清理操作等。



#### debugger

使用`debugger`语句，以便在调用函数时调用调试器

```js
function potentiallyBuggyCode() {
  debugger;
  // 做一些可能会出现错误的检查、单步调试等。
}
```

当 debugger 被调用时，执行暂停在 `debugger` 语句的位置。就像在脚本源代码中的断点一样。



### Web API基本

#### 变量声明

优先使用`const`

原因：能明确表示不可变、提升代码可读性，又能防止意外修改，是包括 React 在内的现代开发最佳实践。

1. **语义化更好**：`const`表明这个变量是一个常量，不会被重新赋值，这使得代码更易读和理解。
2. **避免不必要的修改**：很多变量在声明时就已经确定不会被更改，使用`const`可以防止意外的重新赋值，减少错误。
3. **实际开发中的最佳实践**：例如在React框架中，开发者普遍倾向于使用`const`来声明变量，除非明确需要改变。

特点：

1. `const` 声明的值不能更改，而且 `const` 声明变量的时候需要里面进行初始化。

2. 但是对于引用数据类型，`const` 声明的变量，里面存的不是值，而是地址。

```
const arr = [1, 2, 3];
```

解释：

1. 当使用 `const` 声明一个引用类型的变量（如数组、对象）时，`const` 确保的是这个变量所引用的内存地址不会改变。也就是说，你不能将 `arr` 重新赋值为另一个数组或对象。
2. 但是，你可以修改 `arr` 所指向的数组的内容，因为 `const` 只保护了引用本身，而不是引用所指向的数据。
3. 因为对象是引用类型，里面存储的是地址，只要地址不变，就不会报错

```js
const arr = [1, 2, 3];
arr.push(4); // 允许，因为修改的是堆中的数组内容
console.log(arr); // 输出: [1, 2, 3, 4]

arr = [4, 5, 6]; // 不允许，因为尝试改变 const 变量的引用地址
// 这将导致错误: TypeError: Assignment to constant variable.
```

> 建议数组和对象使用const来声明





#### API作用和分类

作用：就是使用JS去操作html和浏览器

分类：DOM（文档对象模型）、BOM（浏览器对象模型）

![image-20250919113708409](./笔记/web-img/image-20250919113708409.png)

#### DOM（Document Object Model）

定义：文档对象模型。是用来呈现以及与任意HTML或XML文档交互的API

解释：DOM是浏览器提供的一套用来**操作网页内容**的功能



##### DOM树

定义：

- 将 HTML 文档以树状结构直观地表现出来，我们称之为文档树或 DOM 树。
- 描述网页内容关系的名词。
- 作用：**文档树直观地体现了标签与标签之间的关系**。

![image-20250919114407472](C:\Users\32473\Desktop\笔记\web-img\image-20250919114407472-1759020297819-1.png)



##### DOM对象

定义：浏览器根据html标签生成的JS 对象

特点：

所有的标签属性都可以在这个对象上面找到。

修改这个对象的属性会自动映射到标签身上。

```html
<body>
  <div>123</div>
  <script>
    const div = document.querySelector('div')
    // 打印对象
    console.dir(div)  // dom 对象
  </script>
</body>
```

**核心思想：**把网页内容当作对象来写

**document 对象**

- 是 DOM 里提供的一个对象。
- 所以它提供的属性和方法都是用来访问和操作网页内容的。
  - 例：`document.write()`
- 网页所有内容都在 `document` 里面。





### 获取DOM对象

定义：查找元素DOM元素就是利用JS选择页面中标签元素



#### 根据CSS选择器来选择DOM元素

##### 选择匹配的**第一个**元素

```js
document.querySelector('css选择器')
```

```html
<body>
    <div class="box">导航栏</div>
    <script>
        const title = document.querySelector('.box')     //导航栏
    </script>
</body>

```

参数：**字符串**：包含一个或多个有效的 CSS 选择器，如 `'div'`, `'.class'`, `'#id'` 等。

返回值：**HTMLElement 对象**：返回与 CSS 选择器匹配的第一个元素。如果没有找到匹配的元素，则返回 `null`。



##### 选择匹配的**全部**元素

```js
document.querySelectorAll('css选择器')
```

```html
<body>
    <div class="box">导航栏</div>
    <div class="box1">头部</div>
    <div class="box2">内容</div>
    <script>
        const title = document.querySelectorAll('.box')     
    </script>

```

参数：包含一个或多个有效的 CSS 选择器 **字符串**

返回值：CSS 选择器匹配的 NodeList 对象集合

>  注意：`document.querySelectorAll` 返回的是一个**伪数组（类数组对象）

它具有以下特点：

- **有长度和索引号**：可以像数组一样通过索引访问元素。
- **没有数组方法**：不支持 `pop()`, `push()` 等数组方法。

要访问其中的每个对象，需要使用遍历（如 `for` 循环）来获取。例如：

```js
const elements = document.querySelectorAll('ul li');
for (let i = 0; i < elements.length; i++) {
    console.log(elements[i]);
}
```

简而言之，伪数组类似数组但缺少一些数组方法，需用循环访问其元素

> 哪怕只有一个元素，通过 querySelectorAll ()获取过来的也是一个**伪数组**，里面只有一个元素而已



##### 常用方法介绍

**getElementById()**

- 返回值：Element
- 功能：获取指定id的元素节点。
- 示例：`document.getElementById('box')`

**getElementsByName()**

- 返回值：NodeList/HTMLCollection

- 功能：获取相同name属性的元素集合。

- 示例：

  ```javascript
  document.getElementsByName('goods'); // 获取所有name为goods的元素
  document.getElementsByName('goods')[0]; // 获取第一个name为goods的元素
  ```

**getElementsByTagName()**

- 返回值：NodeList/HTMLCollection

- 功能：获取相同标签名的元素集合。

- 示例：

  ```javascript
  document.getElementsByTagName('*'); // 获取所有元素
  document.getElementsByTagName('li'); // 获取所有<li>元素
  document.getElementsByTagName('li')[0]; // 获取第一个<li>元素
  document.getElementsByTagName('li').length; // 获取<li>元素的数量
  ```

- 注：可通过下标访问元素，使用`.length`获取元素数量。

**getElementsByClassName()**

- 返回值：NodeList
- 功能：获取相同类名的元素集合。
- 参数：String类型，类名（多个类名用空格分隔）。
- 示例：`document.getElementsByClassName('example')`

##### 重点提示

- `getElementsByTagName()`不仅可以通过`document`对象调用，还可以通过元素节点`Element`来访问。

```js
// 注意，下面的方法都只需要定义一个字符串类型的参数即可

// document.getElementById(id值) 根据id值获取到页面的指定元素，id是唯一的，返回值类型为Element [HTMLXXXElement]
var div1Element = document.getElementById("div1"); // 获取得到id值为div1的元素节点
// div1Element 是元素节点，可以直接调用innerText
// alert(div1Element.innerText);

// document.getElementsByClassName(class值) 根据class属性值获取到页面的指定元素，返回值HTMLCollection
// 通过getElementsByClassName获取到0个或多个
var allCp = document.getElementsByClassName("cp"); // 获取到class值为cp的元素节点
// allCp不是元素节点，不能直接调用innerText
// 我们可以把HTMLCollection当成是数组来处理，通过下标获取到指定的元素节点
// alert(allCp[2].innerText);

// document.getElementsByName(name值) 根据name属性值获取到页面的指定元素，返回值HTMLCollection
var allPp = document.getElementsByName("pp");
// alert(allPp[0].innerText);

// document.getElementsByTagName(标签名) 根据标签名获取到页面的指定元素，返回值HTMLCollection
var allP = document.getElementsByTagName("p"); // 获取到页面中所有的p元素
// alert(allP[0].innerText);
// alert(allP.length);

// 这四个方法，其中getElementById()/getElementsByName()只能通过document来调用

// 但是 getElementsByClassName()和getElementsByTagName()不仅可以通过document来调用，也可以通过元素节点来调用
// 如果同document来调用这两方法，那么表示从文档中获取指定元素；如果通过元素节点来调用，那么表示获取指定元素节点里面的指定元素；
// 获取到div1里面的所有p标签元素，通过div1元素节点来调用和getElementsByTagName();
var div1AllP = div1Element.getElementsByTagName("p");
// alert(div1AllP.length);

// 获取第二个div里面的class为cp的元素
var allDiv = document.getElementsByTagName("div");
var towDiv = allDiv[1];
var div2Cp = towDiv.getElementsByClassName("cp");
// alert(div2Cp.length);

// Element 表示元素节点，代表的是一个元素节点
// HTMLCollection 表示元素节点集合，这个集合里面存储的都是元素节点，其实就是JS的数组，通过下标可以获取到指定的元素节点
// NodeList 表示节点列表，节点里面里面存储的可能是各种各样的节点，其实就是JS数组
// 扩展：元素节点.innerText 获取到元素节点的文本内容
```



### 操作元素内容

DOM 对象与标签：DOM 对象由标签生成，操作标签即操作 DOM 对象。

点语法：使用点语法操作对象。

#### 修改内容方式

##### 对象.innerText 属性

> 将文本内容添加/更新到任意标签位置
>
> 显示纯文本，不解析标签

```html
<body>
    <div class="box">导航栏</div>
    <div class="box1">头部</div>
    <div class="box2">内容</div>
    <script>
        const title = document.querySelector('.box')     
        console.log(title.innerText)
        title.innerText = '头部'
    </script>
</body>

```



##### 对象.innerHTML属性

> 将文本内容添加/更新到任意标签位置
>
> 会解析标签，多标签建议使用模板字符

```html
<body>
    <div class="box">导航栏</div>
    <div class="box1">头部</div>
    <div class="box2">内容</div>
    <script>
        const title = document.querySelector('.box')     
        console.log(title.innerText)
        title.innerHTML = '<strong>neirong</strong> '
    </script>
</body>

```



#### 常用属性修改

通过 JS 设置/修改标签元素属性

**最常见的属性：**

- `href`
- `title`
- `src`

语法：

```
对象.属性 = 值
```

举例说明：

```js
// 1. 获取元素
const pic = document.querySelector('img');

// 2. 操作元素
pic.src = './images/b02.jpg';
pic.title = '刘德华黑马演唱会';
```

解释：

使用 `document.querySelector` 方法获取页面中的 `<img>` 元素。

通过设置 `pic.src` 和 `pic.title` 属性来修改图片的源路径和标题。



#### 操作元素样式属性

通过 JS 设置/修改标签元素的样式属性

示例场景：

- 通过轮播图小圆点自动更换颜色样式。
- 点击按钮可以滚动图片，这是移动的图片的位置 `left` 等等。

**方法**：

1. **通过 style 属性操作 CSS**

> 注意：一定要加引号；小驼峰命名法（box.style.backgroundColor）

```html
    <style>
        .box{
            width: 200px;
            height: 200px;
            background-color: #778;
        }
    </style>
</head>
<body>
    <div class="box"></div>

    <script>
        const box = document.querySelector('.box')
        box.style.width = '300px'
        box.style.backgroundColor = 'red'
        box.style.border = '2px solid blue'
        box.style.backgroundImage = "src('./图片链接')"
    </script>
```

2. **操作类名 (className) 操作 CSS**

优势：可以同时修改多个属性

注意：className 会被覆盖元素原有的所有类

修改样式

如果修改的样式比较多，直接通过 `style` 属性修改比较繁琐，我们可以通过借助于 CSS 类名的形式。

语法：

```js
// active 是一个 CSS 类名
元素.className = 'active'
```

> 注意：

由于 `class` 是关键字，所以使用 `className` 去代替。

`className` 是使用新值替换旧值，如果需要添加一个类，需要保留之前的类名。

```html
    <style>
        div{
            width: 100px;
            height: 100px;
            background-color: #225;
        }
        .box{
            width: 200px;
            height: 200px;
            background-color: #778;
        }
    </style>
</head>
<body>
    <div></div>

    <script>
        const div = document.querySelector('div')
        div.className = 'box'
    </script>

```



3. **通过 classList 操作类控制 CSS**

**优点**：为了解决 className 容易覆盖以前的类名，我们可以通过 classList 方式追加和删除类名

语法：

```js
// 追加一个类
元素.classList.add('类名')

// 删除一个类
元素.classList.remove('类名')

//三个方法，注意加（）

// 切换一个类
元素.classList.toggle('类名')

//不替换以前的类名
```

解释：使用 `classList` 可以更灵活地管理元素的类名，避免直接使用 `className` 时可能覆盖原有类名的问题。

```html
    <style>
        .box {
            width: 200px;
            height: 200px;
            background-color: #778;
        }

        .active {
            width: 100px;
            height: 100px;
            background-color: #225;
        }
    </style>
</head>

<body>
    <div class="box"></div>

    <script>
        const div = document.querySelector('div')
        div.classList.add('active')
    </script>

```

**修改样式**

- `add()` 方法用于添加类名。
  * 追加类add()类名不加点，并且是字符串 `div.classList.add('active')`
- `remove()` 方法用于删除类名。
- `toggle()` 方法用于切换类名（如果类名存在则删除，不存在则添加）。



#### 操作表单元素属性

- 表单很多情况，也需要修改属性，比如点击眼睛，可以看到密码，本质是把表单类型转换为文本框
- 正常的有属性有取值的 跟其他的标签属性没有任何区别

> 获取: DOM对象.属性名
> 设置: DOM对象.属性名 = 新值

```js
表单.value = '用户名'
表单.type = 'password'
```

```html
//表单.value = '用户名'
<body>
    <input type="text" value="电脑">
    <script>
        const uname = document.querySelector('input')
        // 获取值 获取表单里面用的值 表单.value
        console.log(uname.value)
    </script>
</body>
```

```html
// 表单.type = 'password'
<body>
    <input type="text" value="电脑">
    <script>
        const uname = document.querySelector('input')
        // 获取值 获取表单里面用的值 表单.value
        // console.log(uname.value)
        // 设置表单的值
        uname.value = '你好'
        uname.type = 'password'
    </script>
</body>
```



表单属性中添加就有效果，移除就没有效果，一律使用布尔值表示。如果为 `true` 代表添加了该属性，如果是 `false` 代表移除了该属性。

比如：`disabled`、`checked`、`selected`

```html
<body>
    <input type="checkbox" name="" id="" checked>
    <button>点击</button>
    <script>
        const ipt = document.querySelector('input')
        // console.log(ipt.checked)     //只接受布尔值
        ipt.checked = true
        // ipt.checked = 'true'     //会选中，不提倡 有隐式转换
        const btn = document.querySelector('button')
        btn.disabled = true    //禁用按钮
    </script>
</body>

```

**修改表单属性**

1. **获取表单元素**：使用 `document.getElementById()`, `querySelector()` 等方法。
2. **修改其属性或属性值**：直接通过点语法（`.`）操作 DOM 对象的属性。



**点击轮播图侧边栏出现小箭头**

```js
academic.addEventListener('click', function () {
    arrow1.style.opacity = 0
    arrow2.style.opacity = 1
    arrow3.style.opacity = 0
    arrow4.style.opacity = 0
})
```



**修改背景图**

```js
    const Stu = document.querySelector('.Stu')
    Stu.style.backgroundImage = "url('../img/banner_bgc.png')"
    Stu.style.backgroundColor = ''; // 清空背景颜色

```



#### 自定义属性（`data-*`）

定义：在网页开发中，有时需要为 HTML 元素附加一些**私有数据**（如 ID、状态、配置等），但又不想影响标准属性。这时就可以使用 **自定义属性**。

---

##### 标准属性 vs 自定义属性

| 类型           | 定义                       | 示例                                  | 操作方式                           |
| -------------- | -------------------------- | ------------------------------------- | ---------------------------------- |
| **标准属性**   | HTML 标签原生支持的属性    | `id`, `class`, `title`, `src`, `href` | 可用点语法或 `getAttribute()` 操作 |
| **自定义属性** | 开发者自定义的数据存储属性 | `data-id`, `data-name`, `data-role`   | 推荐使用 `dataset` 操作            |

> ✅ **推荐使用 `data-\*`**：避免污染标准属性，符合 HTML5 规范，不会引起兼容性问题。

---

##### 自定义属性：`data-*`

###### ✅ 1. 定义与命名规则

- 所有自定义属性必须以 **`data-` 开头**，如：`data-id="1"`。
- 后续名称可自定义，建议使用小写字母、数字、连字符（`-`）。
- 支持多个自定义属性共存。

```html
<div 
  data-id="123" 
  data-user-name="小明" 
  data-age="20" 
  data-role="admin">
  用户信息
</div>
```

------

###### ✅ 2. 访问方式：`dataset` 属性

通过 JavaScript 的 DOM 对象，使用 `.dataset` 来读取或修改所有 `data-*` 属性。

> 🔍 **命名转换规则**：
>
> - HTML 中使用**短横线命名**（kebab-case）：`data-user-name`
> - JS 中通过**驼峰命名**（camelCase）访问：`dataset.userName`

📌 示例代码：

```js
const div = document.querySelector('div');

console.log(div.dataset.id);        // "123"
console.log(div.dataset.userName);  // "小明" （data-user-name → userName）
console.log(div.dataset.age);       // "20"
console.log(div.dataset.role);      // "admin"
```

> 💡 小技巧：
>  `dataset` 返回一个 `DOMStringMap` 对象，包含所有 `data-*` 属性。



##### 修改属性的方法

| 类别                     | 方法               | 语法示例                                                     | 适用场景                                                     | 优点                             | 缺点 / 注意事项                                      |
| ------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------------- | ---------------------------------------------------- |
| **普通 JavaScript 对象** | 点号语法 `.`       | `obj.property = value`                                       | 属性名为合法标识符（如 `name`, `favoriteColor`）             | 简洁、易读                       | 不支持含空格或特殊字符的属性名                       |
|                          | 方括号语法 `[]`    | `obj["property"] = value`                                    | 属性名含空格、连字符或动态字符串（如 `"first name"`, `"data-value"`） | 灵活，支持任意属性名             | 语法稍显冗长                                         |
|                          | 动态属性名         | `obj[dynamicKey] = value`                                    | 属性名在运行时确定（如变量 `key = "score"`）                 | 支持动态设置属性                 | 需确保变量有正确值                                   |
|                          |                    | `const key = "age"; obj[key] = 30;`                          |                                                              |                                  |                                                      |
| **HTML 元素（DOM）**     | `dataset` 属性     | `element.dataset.camelCase = value` （如 `data-user-id` → `userId`） | 修改 `data-*` 自定义属性                                     | 语义清晰、安全、自动驼峰转换     | 仅支持 `data-*` 属性，需现代浏览器支持               |
|                          | `setAttribute()`   | `element.setAttribute('attr-name', value)`                   | 修改任意 HTML 属性（包括 `data-*` 和非 `data-*`）            | 通用性强，兼容性好，可创建新属性 | 需注意属性名拼写，不自动转换命名                     |
|                          | 直接赋值（不推荐） | `element.customProp = value`                                 | 临时存储数据（仅 JS 层面）                                   | 操作简单                         | **不会反映在 HTML 标签上**，易与标准属性冲突，不可靠 |

`setAttribute()` 方法

```js
element.setAttribute(name, value);
```

- `name`：要设置的**属性的名称**（字符串）。
- `value`：要设置的**属性的值**（会被自动转换为字符串）。

✅ 示例 1：修改 `data-*` 属性（手动处理命名）

假设你有这样一个 HTML 元素：

```
<div id="box" data-user-id="123" data-page-name="Home">内容</div>
```

你想用 `setAttribute` 修改 `data-user-id` 和 `data-page-name`。

##### 正确写法：

```js
const element = document.getElementById('box');

// 必须原样写出带连字符的属性名
element.setAttribute('data-user-id', '456');
element.setAttribute('data-page-name', 'About');
```

✅ 结果：

```
<div id="box" data-user-id="456" data-page-name="About">内容</div>
```



----

##### 自定义属性的增删查改（CRUD）

###### 1️⃣ **查（Read）—— 获取属性值**

```js
console.log(div.dataset.id);        // 获取 data-id 的值
console.log(div.dataset.userName);  // 获取 data-user-name 的值
```

------

###### 2️⃣ **增（Create）与 改（Update）—— 添加或修改**

语法相同：直接赋值即可。

```js
// ✅ 添加新属性
div.dataset.role = "admin";              // → data-role="admin"
div.dataset.userEmail = "xiao@qq.com";   // → data-user-email="xiao@qq.com"

// ✅ 修改已有属性
div.dataset.age = "25";                  // 修改 data-age 为 "25"
```

> ✅ **自动转换**：JS 赋值时会自动转为 HTML 属性（驼峰 → 短横线）

------

###### 3️⃣ **删（Delete）—— 删除属性**

方法一：`delete` 操作符（✅ 推荐）

```js
delete div.dataset.userName;  // 删除 data-user-name 属性
```

方法二：赋值为 `null`

```js
div.dataset.age = null;       // 也会删除该属性
```

❌ 错误做法：赋值为 `undefined`

```js
div.dataset.id = undefined;   // ❌ 结果是 data-id="undefined"（字符串！）
```

> ⚠️ **切记**：`undefined` 会被转为字符串 `"undefined"`，**不会删除属性**！

---

> 案例

```html
<div data-id="1" data-user-name="张三" data-age="18">用户1</div>

<script>
  const userDiv = document.querySelector('div');

  // 查
  console.log(userDiv.dataset.id);         // "1"
  console.log(userDiv.dataset.userName);   // "张三"

  // 增 / 改
  userDiv.dataset.role = "vip";
  userDiv.dataset.age = "20";

  // 删
  delete userDiv.dataset.userName;

  // 最终 HTML: <div data-id="1" data-age="20" data-role="vip">用户1</div>
</script>
```





### 定时器

#### 定时器-间接函数

##### 什么是 `setInterval`？

`setInterval` 是 JavaScript 提供的一个**全局函数**，用于**重复执行**一段代码，每隔指定时间自动调用一次函数。

✅ 基本语法：

```js
let timerId = setInterval(函数, 间隔时间（毫秒）);
```

- **函数**：要执行的回调函数（不能加括号）
- **间隔时间**：单位是**毫秒**（1000 毫秒 = 1 秒）
- **返回值**：一个**数字类型的定时器 ID**，用于后续清除定时器



##### 基本用法示例

1. 使用匿名函数

```js
setInterval(function() {
    console.log('每秒打印一次');
}, 1000); // 每隔 1000ms（1秒）执行一次
```

2. 使用已定义的函数名（推荐）

```js
function fn() {
    console.log('打印');
}
setInterval(fn, 1000); // ✅ 正确：传函数名，不加 ()
```

> ❌ 错误写法：`setInterval(fn(), 1000)`
>  原因：`fn()` 会**立即执行**，传给 `setInterval` 的是 `fn` 的返回值（通常是 `undefined`），导致定时器失效。



##### 关闭定时器？

✅ 步骤：

1. 创建定时器时，**保存返回的 ID** 到一个变量。
2. 使用 `clearInterval(变量名)` 来停止定时器。

示例：

```js
let timer = setInterval(function() {
    console.log('hi~~');
}, 1000);

// 满足条件后停止（比如点击按钮、倒计时结束等）
clearInterval(timer);
```

> ⚠️ **重要**：不清除定时器会导致：

- 内存泄漏
- 无意义的代码持续执行
- 页面性能下降



#### 定时器-延时函数

##### 什么是 `setTimeout`？

`setTimeout` 是 JavaScript 提供的一个**全局函数**，用于**延迟执行一段代码**，且**只执行一次**。

✅ 基本语法：

```js
let timerId = setTimeout(回调函数, 延迟时间（毫秒）);
```

- **回调函数**：延迟后要执行的函数（不能加括号）
- **延迟时间**：单位是**毫秒**（1000 毫秒 = 1 秒）
- **返回值**：一个**数字类型的定时器 ID**，用于后续取消执行



##### 基本用法示例

```js
const div = document.querySelector('div');

setTimeout(function() {
    div.style.display = 'none'; // 3秒后隐藏 div
}, 3000); // 3000 毫秒 = 3 秒
```

> 💡 也可以使用箭头函数：

```js
setTimeout(() => {
    console.log('3秒后执行');
}, 3000);
```



##### 取消延时执行

使用 `clearTimeout(timerId)` 可以在延迟结束**前取消执行**。

✅ 步骤：

1. 调用 `setTimeout` 时，**保存返回的 ID**。
2. 在需要时调用 `clearTimeout(定时器ID)` 取消。

示例：

```js
let timer = setTimeout(() => {
    console.log('这行代码不会执行');
}, 2000);

// 在 1 秒后取消定时器
setTimeout(() => {
    clearTimeout(timer);
    console.log('定时器已取消');
}, 1000);
```

> 📌 应用场景：用户在倒计时跳转前进行了操作，取消跳转。





### 事件监听（绑定）

能够给DOM元素添加事件监听

定义：让程序检测是否有事件产生，一旦触发就调用函数响应。

术语: 绑定事件或注册事件。 

**示例**:

- 鼠标经过显示下拉菜单。
- 点击播放轮播图。

**语法**

```js
元素对象.addEventListener('事件类型', 要执行的函数)
```

**三要素**

1. **事件源**: 触发事件的 DOM 元素，获取DOM，（按钮）。
2. **事件类型**: 如 `click`, `mouseover` 等触发方式。
3. **事件处理函数**: 执行的具体操作。

* 注意：

> 事件类型要加引号
>
> 函数是点击之后再去执行，每次点击都会执行一次

```html
<script>
    // 数据数组
    const arr = ['马超', '黄忠', '赵云', '关羽', '张飞'];
    // 定时器的全局变量
    let timerId = 0;
    // 随机号要全局变量
    const random = 0;
    // 业务1. 开始按钮模块
    const qs = document.querySelector('.qs');
    // 1.1 获取开始按钮对象
    const start = document.querySelector('.start');
    // 1.2 添加点击事件
    start.addEventListener('click', function () {
        timerId = setInterval(function () {
            // 随机数
            random = parseInt(Math.random() * arr.length);
            // console.log(arr[random]);
            qs.innerHTML = arr[random];
        }, 35);
    });

    // 2. 关闭按钮模块
    const end = document.querySelector('.end')
    end.addEventListener('click', function () {
        clearInterval(timerId)
        // 结束了，可以删除掉当前抽取的那个数组元素
        arr.splice(random, 1)
        console.log(arr)
    })
</script>
```



#### 事件监听版本

- **DOM L0**
  - `事件源.on事件 = function() {}`
- **DOM L2**
  - `事件源.addEventListener(事件, 事件处理函数)`
- **区别**:
  - `on` 方式会被覆盖，`addEventListener` 方式可绑定多次，拥有事件更多特性，推荐使用。

```html
<body>
    <button>点击</button>
    <script>
        const btn = document.querySelector('button')
        btn.addEventListener('click',function(){
            alert(11)
        }) 
        btn.addEventListener('click',function(){
            alert(22)
        })
    </script>
</body>
```



#### 事件类型

定义：事件是 JavaScript 实现**交互功能**的核心机制。通过监听用户行为（如点击、输入、按键等），我们可以动态响应并更新页面内容。

---

##### 事件监听基础语法

```js
element.addEventListener('事件名', 回调函数);
```

- `element`：要监听的 DOM 元素
- `'事件名'`：如 `'click'`、`'input'` 等（字符串）
- `回调函数`：事件触发时要执行的代码

---

##### 1️⃣ 鼠标事件（Mouse Events）

| 事件         | 触发条件                | 特点                                    |
| ------------ | ----------------------- | --------------------------------------- |
| `click`      | 鼠标点击（按下 + 抬起） | 最常用，用于按钮点击等                  |
| `mouseenter` | 鼠标进入元素区域        | **不冒泡到子元素**，推荐用于 hover 效果 |
| `mouseleave` | 鼠标离开元素区域        | 与 `mouseenter` 配对使用                |

> ✅ 推荐使用 `mouseenter` 和 `mouseleave` 替代 `mouseover` / `mouseout`，避免子元素触发问题。

示例：

```js
const div = document.querySelector('div');

// 鼠标进入
div.addEventListener('mouseenter', function() {
    console.log('轻轻的我来了');
});

// 鼠标离开
div.addEventListener('mouseleave', function() {
    console.log('轻轻的我走了');
});
```

> 📌 应用场景：菜单展开/收起、按钮悬停效果、图片放大等。

---

##### 2️⃣ 焦点事件（Focus Events）

适用于表单元素（如 `<input>`、`<textarea>`、`<select>`）

| 事件    | 触发条件                                    | 特点               |
| ------- | ------------------------------------------- | ------------------ |
| `focus` | 元素获得焦点（如点击或 Tab 键进入）         | 常用于提示输入格式 |
| `blur`  | 元素失去焦点（如点击其他地方或 Tab 键离开） | 常用于验证输入内容 |

示例：

```js
const input = document.querySelector('input');

input.addEventListener('focus', function() {
    console.log('输入框获得了焦点');
});

input.addEventListener('blur', function() {
    console.log('输入框失去了焦点');
});
```

> 📌 应用场景：

- 输入框获得焦点时显示提示
- 失去焦点时验证邮箱、手机号格式

----

##### 3️⃣ 键盘事件（Keyboard Events）

| 事件      | 触发条件                 | 特点                   |
| --------- | ------------------------ | ---------------------- |
| `keydown` | 键盘按键**被按下时**触发 | 按住不放会**连续触发** |
| `keyup`   | 键盘按键**抬起时**触发   | 通常只触发一次         |

> ⚠️ 注意：`keydown` 在长按情况下会重复触发，而 `keyup` 只在释放时触发一次。

示例：

```js
const input = document.querySelector('input');

input.addEventListener('keydown', function() {
    console.log('键盘按下了');
});

input.addEventListener('keyup', function() {
    console.log('键盘抬起了');
});
```

> 📌 应用场景：

- 按 Enter 键提交表单
- 监听方向键控制游戏人物
- 限制输入内容（如只允许数字）

----

##### 4️⃣ 文本事件（Input Events）

| 事件     | 触发条件                                        | 特点                                     |
| -------- | ----------------------------------------------- | ---------------------------------------- |
| `input`  | **输入内容发生变化时**立即触发                  | 包括键盘输入、粘贴、剪切、拖拽等所有方式 |
| `change` | `change` 事件在控件**失去焦点前**都**不会**触发 |                                          |

> ✅ `input` 是监听输入最**全面、实时**的事件，推荐用于实时搜索、字数统计等。

示例：

```js
const input = document.querySelector('input');

input.addEventListener('input', function() {
    console.log('用户输入了内容');
    console.log('当前值：', this.value); // 获取输入框内容
});
```

> 📌 应用场景：

- 实时搜索（输入即搜索）
- 密码强度检测
- 字数统计（如微博、评论框）
- 表单内容预览



#### 事件对象

##### 定义：

> 事件对象是一个包含**事件触发**时相关信息的**对象**
>
> 事件绑定的回调函数的第一个参数是事件对象

使用场景包括：

- 判断用户按下的键，如按下回车键可以发布新闻。
- 判断鼠标点击了哪个元素，从而执行相应的操作。

##### 获取：

事件绑定的回调函数的**第一个参数**是事件对象，通常命名为 `event`、`ev` 或 `e`。

示例代码：

```js
元素.addEventListener('click', function (e) {
    // 处理点击事件
});
```

```html
<body>
    <button>点击</button>
    <script>
        const btn = document.querySelector('button')
        btn.addEventListener('click',function(e){
            console.log(e)
        })      //PointerEvent {isTrusted: true, pointerId: 1, width: 1, height: 1, pressure: 0, …}
    </script>
</body>
```

##### 一般通用属性（所有事件都可用）

| 属性名          | 类型      | 说明                                                         |
| --------------- | --------- | ------------------------------------------------------------ |
| `type`          | `string`  | 事件的类型（如 `"click"`、`"keydown"`、`"submit"`）。        |
| `target`        | `Element` | **事件最初触发的 DOM 元素**（即事件从哪里开始）。 ⚠️ 注意：不是 `this`，`this` 是绑定事件的元素。 |
| `currentTarget` | `Element` | **当前正在处理事件的元素**（通常等于 `this`）。 在事件冒泡/捕获中，`target` 和 `currentTarget` 可能不同。 |
| `eventPhase`    | `number`  | 事件当前所处的阶段： `0`=无，`1`=捕获，`2`=目标，`3`=冒泡。  |
| `bubbles`       | `boolean` | 该事件是否会**向上冒泡**（如 `click` 会，`focus` 不会）。    |
| `cancelable`    | `boolean` | 是否可以调用 `preventDefault()` 来阻止默认行为（如链接跳转、表单提交）。 |
| `timeStamp`     | `number`  | 事件触发时的时间戳（毫秒），从页面加载开始计算。             |
| `isTrusted`     | `boolean` | 表示事件是否由**用户真实操作**触发（`true`），还是由脚本触发（`false`） |

##### 鼠标事件持有属性

| 属性名                                     | 说明                                                         |
| ------------------------------------------ | ------------------------------------------------------------ |
| `clientX`, `clientY`                       | 鼠标指针相对于**浏览器可视窗口**的坐标（含滚动）。           |
| `pageX`, `pageY`                           | 鼠标指针相对于**整个网页文档**的坐标（含滚动）。             |
| `screenX`, `screenY`                       | 鼠标指针相对于**用户屏幕**的坐标。                           |
| `offsetX`, `offsetY`                       | 鼠标指针相对于**事件目标元素内容区域**的坐标（不含边框）。   |
| `button`                                   | 按下的鼠标按钮： `0`=左键，`1`=中键，`2`=右键。              |
| `buttons`                                  | 当前按下的所有鼠标按钮的组合值（用于多键同时按下）。         |
| `ctrlKey`, `shiftKey`, `altKey`, `metaKey` | 布尔值，表示 `Ctrl`、`Shift`、`Alt`、`Meta`（Mac 的 Command）键是否被按下 |



案例：事件对象，键盘类型，只有敲空格键Enter才能触发，其余的触发不了

```html
<body>
    <!-- <button>点击</button> -->
    <input type="text">
    <script>
        const input = document.querySelector('input')
        input.addEventListener('keyup',function(e){
            // console.log(11)
            console.log(e.key)
            if(e.key === 'Enter'){
                console.log('我按写了回车键')
            }
        })
    </script>
</body>
```



拓展：trim（）

去除字符串左右两边的 空格

```html
<body>
    <script>
        const str = '           red                '
        console.log(str.trim())      // 去除元素空格 
    </script>
</body>

```



####  环境对象 

##### `this` 的定义

- `this` 是一个**关键字**，在函数内部自动存在。
- 它指向**调用该函数的那个对象**，即函数运行时的执行上下文。
- **`this` 的值在函数调用时确定**，而不是定义时。

---

##### 常见调用方式与 `this` 指向

| 调用方式         | `this` 指向            | 说明                                 |
| ---------------- | ---------------------- | ------------------------------------ |
| **普通函数调用** | `window`（浏览器环境） | 非严格模式下；严格模式为 `undefined` |
| **对象方法调用** | 该对象本身             | 谁调用，`this` 就指向谁              |
| **构造函数调用** | 新创建的实例对象       | 使用 `new` 关键字创建对象时          |
| **事件处理函数** | 绑定事件的 DOM 元素    | 如按钮点击，`this` 是按钮元素        |
| **箭头函数**     | 外层作用域的 `this`    | 箭头函数没有自己的 `this`，继承外层  |

---

##### 详细场景解析

###### 1️⃣ 普通函数调用 → `this` 指向 `window`

```js
function fn() {
    console.log(this); // window
}
fn(); // 等价于 window.fn()
```

> ⚠️ 注意：
>
> - 在浏览器中，全局对象是 `window`
> - 在严格模式下（`'use strict'`），`this` 为 `undefined`

------

###### 2️⃣ 对象方法调用 → `this` 指向该对象

```js
const obj = {
    name: '张三',
    say() {
        console.log(this); // obj
        console.log(this.name); // '张三'
    }
};
obj.say(); // 调用者是 obj，所以 this 是 obj
```

> ✅ 关键：方法必须是**通过对象调用**，`this` 才指向该对象。

------

###### 3️⃣ 事件处理函数 → `this` 指向绑定的 DOM 元素

```js
const btn = document.querySelector('button');
btn.addEventListener('click', function() {
    console.log(this); // btn 元素
    this.style.color = 'red'; // 改变按钮颜色
});
```

> 💡 优势：可以直接用 `this` 操作当前触发事件的元素，无需再查询。

------

###### 4️⃣ 构造函数调用 → `this` 指向新创建的实例

```js
function Person(name) {
    this.name = name;
    console.log(this); // 新创建的 person 实例
}
const person = new Person('李四');
```

> ✅ `new` 关键字会创建一个新对象，并将 `this` 绑定到该对象。

------

###### 5️⃣ 箭头函数 → `this` 指向外层作用域

```js
const obj2 = {
    fn: () => {
        console.log(this); // window（外层是全局作用域）
    }
};
obj2.fn();

// 常见用法：在事件中保持外层 this
const user = {
    name: '小明',
    delayPrint() {
        setTimeout(() => {
            console.log(this.name); // '小明'（箭头函数继承外层 this）
        }, 1000);
    }
};
user.delayPrint();
```

> ⚠️ 注意：**箭头函数没有自己的 `this`**，它的 `this` 是继承定义时外层函数或全局作用域的 `this`。

----

##### 经典示例对比

```js
// 普通函数
function fn() { console.log(this); } // this → window

// 对象方法
const obj = { fn() { console.log(this); } }; // this → obj

// 事件处理
btn.addEventListener('click', function() {
    console.log(this); // this → btn
});

// 箭头函数
const obj2 = { fn: () => console.log(this) }; // this → window（外层）
```





#### 回调函数

##### 什么是回调函数？

✅ 定义：

**回调函数**是指将一个函数作为**参数**传递给另一个函数，并在某个事件发生或操作完成后，由外部函数来**调用这个函数**。

✅ 核心思想：

- 函数是一等公民，可以像数据一样被传递。
- 实现**延迟执行**或**定制行为**，提高代码的灵活性和复用性。

✅ 基本语法：

```js
function fn() {
    console.log('我是回调函数');
}

someFunction(fn); // 将 fn 作为参数传入
```

✅ 示例：

```js
function fn() {
    console.log('回调函数');
}
setInterval(fn, 1000); // fn 被 setInterval 在每秒后调用
```

> 💡 `fn` 没有立即执行，而是“等别人回头来调用它”。

------

##### 回调函数的分类

| 类型         | 执行时机 | 是否阻塞     | 典型例子                              |
| ------------ | -------- | ------------ | ------------------------------------- |
| **同步回调** | 立即执行 | ✅ 阻塞主线程 | `forEach`, `map`, `filter`            |
| **异步回调** | 延迟执行 | ❌ 不阻塞     | `setTimeout`, `setInterval`, 事件监听 |

----

##### 同步回调

✅ 定义：

在外部函数调用后**立即执行**的回调函数，中间没有异步任务（如定时器、网络请求、事件等待）。

🔑 核心特点：

| 特点              | 说明                             |
| ----------------- | -------------------------------- |
| **1. 立即执行**   | 回调函数传入后，马上被调用       |
| **2. 阻塞主线程** | 主函数必须等回调执行完才能继续   |
| **3. 顺序执行**   | 代码从上到下依次执行，顺序可预测 |

✅ 常见例子：

```js
function myCallback(item) {
    console.log("处理:", item);
}

[1, 2, 3].forEach(myCallback);
console.log("循环结束");
```

**输出顺序：**

```js
处理: 1
处理: 2
处理: 3
循环结束
```

> ✅ 所有操作是**同步、按序、立即执行**。

✅ 使用场景：

| 场景               | 示例                                                  |
| ------------------ | ----------------------------------------------------- |
| **数组方法**       | `forEach`, `map`, `filter`, `reduce`, `some`, `every` |
| **自定义逻辑封装** | 数据处理、格式转换                                    |
| **工具函数**       | 排序规则、验证函数等                                  |

```js
// 自定义函数中使用回调
function process(data, callback) {
    const result = data * 2;
    return callback(result); // 立即调用
}
```

---

##### 异步回调

✅ 定义：

回调函数**不会立即执行**，而是被注册，等待某个异步操作（如定时、事件、网络请求）完成后才执行。

> 📣 **“请记住我，当某件事发生时，再调用我。”**

🔑 核心特点：

| 特点                  | 说明                                 |
| --------------------- | ------------------------------------ |
| **1. 延迟执行**       | 回调被“排队”，稍后执行               |
| **2. 非阻塞**         | 不会卡住主线程，程序继续执行后续代码 |
| **3. 事件驱动**       | 由用户操作、定时器、网络响应等触发   |
| **4. 执行时机不确定** | 可能写在前面，但执行在后面           |

✅ 常见例子：

1. `setTimeout`

```js
console.log("第一步");
setTimeout(() => console.log("第三步"), 1000);
console.log("第二步");
```

**输出：**

```js
第一步
第二步
第三步
```

2. 事件监听

```js
btn.addEventListener('click', () => {
    console.log("按钮被点击了！");
});
```

> 点击时才执行，典型的异步回调。

3. 网络请求（`fetch`）

```js
console.log("开始请求");
fetch('/api/data').then(() => {
    console.log("数据返回了！");
});
console.log("继续做其他事");
```

> `.then()` 中的回调是异步的。





### 事件流

定义：事件完整执行过程中的流动路径

两个阶段：事件捕获，事件冒泡

-----

#### 事件捕获

**定义**：从DOM的根元素开始执行对应的事件（从外到里）。

**实现**：需要编写代码才能看到效果。

##### 代码示例

```javascript
DOM.addEventListener(事件类型, 事件处理函数, 是否使用捕获机制)
```

##### 参数说明

- 第三个参数传入 `true` 表示在捕获阶段触发（很少使用）。
- 传入 `false` 表示在冒泡阶段触发，默认值为 `false`。
- 使用 `LO` 事件监听时，只有冒泡阶段，没有捕获。

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .father {
            width: 400px;
            height: 400px;
            background-color: #550;
        }

        .son {
            width: 200px;
            height: 200px;
            background-color: #089;
        }
    </style>
</head>

<body>
    <div class="father">
        <div class="son"></div>
    </div>

    <script>
        const fa = document.querySelector('.father')
        const so = document.querySelector('son')
        document.addEventListener('click', function () {
            alert('nihao')
        },true)
        document.addEventListener('click', function () {
            alert('father')
        },true)
        document.addEventListener('click', function () {
            alert('son')
        },true)

    </script>
</body>

</html>
```

-----

#### 事件冒泡

定义：当一个元素的事件被触发时，同样的事件将会在该元素的所有祖先元素中依次被触发。这一过程叫做事件冒泡

- **简单理解**：当一个元素触发事件后，会依次向上调用所有父级元素的同名事件。
- **默认行为**：事件冒泡是默认存在的。
- **监听设置**：在L2事件监听中，`addEventListener` 的第三个参数默认为 `false`，表示使用冒泡阶段。
- **执行过程：**
  1. **触发起点**：事件从最内层的**目标元素**（触发事件的元素）开始。
  2. **向上冒泡**：事件会逐级向上传播，依次触发其**父元素、祖父元素……直到根元素（如 `document` 或 `window`）**。
  3. **顺序执行**：按照 DOM 层级从内到外（子 → 父 → 祖先）依次执行每个元素上绑定的**同类型事件处理函数**。

示例代码

```js
const father = document.querySelector('.father');
const son = document.querySelector('.son');

document.addEventListener('click', function() {
    alert('我是爷爷');
});

father.addEventListener('click', function() {
    alert('我是爸爸');
});

son.addEventListener('click', function() {
    alert('我是儿子');
});
```

-------

#### 阻止冒泡

- **问题**：默认存在冒泡模式，事件可能影响到父级元素。
- **需求**：若要将事件限制在当前元素内，需阻止事件冒泡。
- **前提**：阻止冒泡需要获取事件对象。
- **方法**：使用 `event.stopPropagation()`。

```js
element.addEventListener('click', function(event) {
    event.stopPropagation(); // 阻止事件冒泡
});
```

- **注意**：此方法不仅在冒泡阶段有效，在捕获阶段也有效

-----

#### 解绑事件

##### L0 事件移除解绑

on事件方式，直接使用null覆盖就可以实现事件的解绑

**语法**：

```js
// 绑定事件
btn.onclick = function () {
    alert('点击了');
}

// 解绑事件
btn.onclick = null;
```

这段代码展示了如何使用 `on` 事件绑定和解绑方法。通过将 `onclick` 属性设置为一个函数来绑定点击事件，然后将其设置为 `null` 来解除绑定。 

##### L2 事件移除解绑

addEventListener方式，必须使用：

```js
removeEventListener(事件类型, 事件处理函数, [获取捕获或者冒泡阶段])
```

**例如**：

```js
function fn() {
    alert('点击了');
}
// 绑定事件
btn.addEventListener('click', fn);
// 解绑事件
btn.removeEventListener('click', fn);
```

**注意**：匿名函数无法被解绑。

------

#### 鼠标经过的区别 

- `mouseover` 和 `mouseout` 会有冒泡效果。
- `mouseenter` 和 `mouseleave` 没有冒泡效果（推荐）。

##### 传统 `on` 注册 (L0)

- **覆盖问题**：同一对象，后注册的事件会覆盖前面的。
- **解绑方式**：直接将事件处理函数设为 `null`。
- **执行阶段**：都是在冒泡阶段执行。

##### 事件监听注册 (L2)

- **语法**：`addEventListener(事件类型, 事件处理函数, 是否使用捕获)`.
- **不覆盖**：后注册的事件不会覆盖前面的。
- **阶段选择**：通过第三个参数决定在冒泡或捕获阶段执行。
- **解绑方法**：必须使用 `removeEventListener(事件类型, 事件处理函数, 获取捕获或者冒泡阶段)`。
- **匿名函数限制**：匿名函数无法被解绑。

案例：

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .dad {
            width: 400px;
            height: 400px;
            background-color: #501;
        }

        .son {
            width: 300px;
            height: 300px;
            background-color: rgb(138, 102, 148);
        }
    </style>
</head>

<body>
    <div class="dad">
        <div class="son"></div>
    </div>

    <script>
        const dad = document.querySelector('.dad')
        const son = document.querySelector('.son')
        dad.addEventListener('mouseenter', function () {
            console.log('鼠标经过')
        })
        dad.addEventListener('mouselive', function () {
            console.log('鼠标离开')
        })
        son.addEventListener('mouseenter', function () {
            console.log('鼠标经过')
        })
        son.addEventListener('mouselive', function () {
            console.log('鼠标离开')
        })

    </script>
</body>

</html>
```

-----

#### 事件委托

**定义**：**事件委托**是利用**事件冒泡**机制，将子元素的事件监听绑定到其父元素上，通过判断 `event.target` 来执行对应操作的一种编程技巧。

**优点**：减少注册次数，可以提高程序性能

**原理**：利用事件冒泡的特点。

* 给**父元素**注册事件（委托给**父元素**），当子元素被触发时，事件会冒泡到父元素上，从而触发父元素的事件处理函数。

**语法**：通过 `event.target.tagName` 获取真正触发事件的元素

`e.target.tagName`

| 部分           | 含义                                                         |
| -------------- | ------------------------------------------------------------ |
| **`e`**        | 事件对象（event object） 当事件（如点击、输入等）发生时，浏览器自动传入的参数，包含事件的详细信息。 |
| **`.target`**  | 事件对象的属性 指向**真正触发事件的 DOM 元素**（也就是“事件源”）。 ✅ 例如：你点击了一个 `<button>`，`e.target` 就是这个 `<button>` 元素。 |
| **`.tagName`** | DOM 元素的属性 返回该元素的**HTML 标签名**，且**始终是大写字符串**。 |

```js
ul.addEventListener('click', function(){}); // 执行父级点击事件
```

```html
<body>
    <ul>
        <li>第1个孩子</li>
        <li>第2个孩子</li>
        <li>第3个孩子</li>
        <li>第4个孩子</li>
        <li>第5个孩子</li>
        <p>不变色</p>
    </ul>

    <script>
        //点击每个小li 当前li文字变成红色
        //1.获得父级
        const ul = document.querySelector('ul')
        ul.addEventListener('click',function(e){
            // this.style.color = 'pink'
            // console.log(e.target)
            // e.target.style.color = 'pink'
            // 我们只要点击li才会有效果
            if(e.target.tagName === 'LI'){
                e.target.style.color = 'pink'
            }
        })
</script>
</body>
```

---

#### 阻止默认行为

**需求**：在某些情况下需要阻止元素的默认行为，如阻止链接跳转或表单提交。

**方法**：使用 `e.preventDefault()`。

**示例代码**

```js
const form = document.querySelector('form');
form.addEventListener('click', function(e) {
    e.preventDefault(); // 阻止表单默认提交行为
});
```

这段代码阻止了表单的默认提交行为。



### 其他事件

#### 页面加载事件

1. **加载外部资源**：当图片、外联CSS和JavaScript等外部资源加载完毕时会触发的事件。
2. 为什么要学
   - 有时需要在页面资源全部加载完成后执行某些操作。
   - 老代码习惯将script写在head中，这时直接查找DOM元素可能找不到。
3. **事件名**：`load`
4. **触发对象**：`window`或 `document`
5. 监听页面所有资源加载完毕
   - 给window添加`load`事件

```js
// 页面加载事件   等待页面所有资源加载完毕，就回去执行回调函数
window.addEventListener('load', function () {
    // 执行的操作
});
```

> 注意：不光可以监听整个页面资源加载完毕，也可以针对某个资源绑定load事件

----

##### **DOM加载完成**

* **事件名**：DOMContentLoaded

>  为什么要这么做？
>
> **因为网页加载是分阶段进行的，开发者往往不需要等图片、样式全加载完，只想在 DOM 结构准备好后就立即操作页面。**
>
> 所以浏览器提供 `DOMContentLoaded` 事件，让 JS 能 **尽早执行**，提升性能和用户体验。

- 当初始的 HTML 文档被完全加载和解析完成之后，DOMContentLoaded 事件被触发，而无需等待样式表、图像等完全加载
- 监听页面DOM加载完毕：
  - 给 document 添加 DOMContentLoaded 事件

```js
document.addEventListener('DOMContentLoaded', function () {
    // 执行的操作
});
```

-----

#### 元素滚动事件

**事件名**：scroll

**定义**：滚动条在滚动的时候**持续触发**的事件

为什么要学？

- 很多网页需要检测用户把页面滚动到某个区域后做一些处理，比如固定导航栏，比如返回顶部

监听整个页面滚动：

```js
// 页面滚动事件
window.addEventListener('scroll', function () {
    // 执行的操作
});
```

```html
    <style>
        body{
            height: 3000px;
        }
    </style>
</head>
<body>
    <script>
        window.addEventListener('scroll',function(){
            console.log('我滚了')
        })
    </script>
</body>

```

-----

##### 获取位置

`scrollLeft` 和 `scrollTop` 是用于获取或设置元素被卷去的大小的属性，具体来说：

- **用途**：它们可以获取元素内容往左、往上滚出去看不到的距离。
- **可读写**：可以读取也可以修改。这两个值是可读写的，意味着你可以读取当前滚动位置，也可以设置新的滚动位置。

> 注意：尽量在scroll事件里面获取被卷去的距离

例如，你可以使用它们来控制页面或元素的滚动位置。

![image-20250924093812162](C:\Users\32473\Desktop\笔记\web-img\image-20250924093812162-1759024199639-3.png)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body{
            padding-top: 100px;
            height: 3000px;
        }

        div{
            overflow: scroll;
            margin: 100px;
            width: 200px;
            height: 200px;
            border: 1px solid #000;
        }
    </style>
</head>
<body>
    <div>
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
        我里面有很多文字
    </div>
    <script>
        // window.addEventListener('scroll',function(){
        //     // console.log('我滚了')
        // })
        const div = document.querySelector('div')
        div.addEventListener('scroll',function(){
            // console.log(11)
            // scrollTop 被卷去的头部
            console.log(div.scrollTop)
        })
    </script>
</body>
</html>
```



##### 滚动到指定的坐标

- `scrollTo()` 方法可把内容滚动到指定的坐标
- 语法：
  - 元素.scrollTo(x, y)

示例代码：

```js
// 让页面滚动到 y 轴1000像素的位置
window.scrollTo(0, 1000)
```

----------

##### 页面尺寸事件

- 当窗口尺寸改变时触发的事件：`resize`

- 监听窗口大小变化：

  ```js
  window.addEventListener('resize', function () {
    // 执行的代码
  });
  ```

- 检测屏幕宽度：

  ```js
  window.addEventListener('resize', function () {
    let w = document.documentElement.clientWidth;
    console.log(w);
  });
  ```



> 案例：电梯问题

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .content {
            margin: 0 auto;
        }

        .all {
            display: flex;
            justify-content: center;
        }

        .box {
            width: 300px;
        }

        .box1,
        .box2,
        .box3,
        .box4,
        .box5 {
            width: 300px;
            height: 400px;
            background-color: rgb(168, 181, 223);
            margin-bottom: 20px;
        }

        .btn {
            margin-left: 600px;
            margin-top: 200px;
            position: fixed;
        }

        .p1,
        .p2,
        .p3,
        .p4,
        .p5,
        .top {
            width: 40px;
            height: 40px;
            background-color: rgb(202, 178, 224);
            margin-bottom: 20px;
        }
    </style>
</head>

<body>
    <div class="all content">
        <div class="box ">
            <div class="box1">box1</div>
            <div class="box2">box2</div>
            <div class="box3">box3</div>
            <div class="box4">box4</div>
            <div class="box5">box5</div>
        </div>
        <div class="btn">
            <div class="p1">
                <a href="javaScript:;" id="p1">p1</a>
            </div>
            <div class="p2">
                <a href="javaScript:;" id="p2">p2</a>
            </div>
            <div class="p3">
                <a href="javaScript:;" id="p3">p3</a>
            </div>
            <div class="p4">
                <a href="javaScript:;" id="p4">p4</a>
            </div>
            <div class="p5">
                <a href="javaScript:;" id="p5">p5</a>
            </div>
            <div class="top">
                <a href="javaScript:;" id="backTop">顶部</a>
            </div>
        </div>
    </div>

    <script>
        const bt = document.querySelector('.top')
        window.addEventListener('scroll', function () {
            const n = document.documentElement.scrollTop

            if(n >= 300){
                bt.style.opacity = 1
            }else{
                bt.style.opacity = 0
            }
        })

        const backtop = document.querySelector('#backTop')
        backtop.addEventListener('click',function(){
            document.documentElement.scrollTop = 0
        })

        const p1 = document.querySelector('#p1')
        p1.addEventListener('click',function(){
            window.scrollTo(0,0)
        })

        const p2 = document.querySelector('#p2')
        p2.addEventListener('click',function(){
            window.scrollTo(0,400)
        })

        const p3 = document.querySelector('#p3')
        p3.addEventListener('click',function(){
            window.scrollTo(0,840)
        })

        const p4 = document.querySelector('#p4')
        p4.addEventListener('click',function(){
            window.scrollTo(0,1260)
        })

        const p5 = document.querySelector('#p5')
        p5.addEventListener('click',function(){
            window.scrollTo(0,1680)
        })
    </script>
</body>

</html>
```

-------------------



### 获取元素的 html 和 body 的元素写法

> 获取 html 的元素写法 `document.documentElement`

```html
<script>  
    window.addEventListener('scroll', function () {
            // 获取html的元素写法
            // document.documentElement
            console.log(document.documentElement)
            // 获取body的元素写法
            console.log(document.body)
</script>
```

```html
<script> 
    const div = document.querySelector('div')
    window.addEventListener('scroll', function () {
        // // 获取html的元素写法
        // // document.documentElement
        // console.log(document.documentElement)
        // // 获取body的元素写法
        // console.log(document.body)

        //可以知道页面到底滚动了多少，被卷去了多少，scrollTop
        // console.log(document.documentElement.scrollTop)
        const n = document.documentElement.scrollTop
        if(n >= 100 ){
            div.style.display = 'block'
        }else{
            div.style.display = 'none'
        }
    })
</script>
```

##### 



#### 元素尺寸与位置

使用场景：
 通过 JS 获取元素在页面中的位置，当页面滚动到该元素时自动触发操作，无需手动计算滚动距离，简化逻辑。

- **获取宽高**：

  - `offsetWidth` 和 `offsetHeight` 获取元素的可视宽高（含宽高、padding、border）
  - 返回数值，便于计算
  - 注意：元素隐藏时返回 0

- **获取位置**：

  1. 

  - `offsetLeft` 和 `offsetTop` 获取元素距离定位父元素的左 / 上距离
  - 只读属性

  2. **方法名称**：`element.getBoundingClientRect()`

  **功能描述**：返回元素的大小（宽高）及其相对于视口（浏览器窗口可见区域）的位置信息。

  **返回值**：一个包含 `left`, `right`, `top`, `bottom`, `width`, `height` 等属性的对象，用于精确计算元素在屏幕中的位置。

> 案例：**滚动吸顶效果**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .content {
            margin: 0 auto;
        }

        .head {
            position: fixed;
            width: 100%;
            height: 80px;
            background-color: rgb(88, 124, 160);
        }

        .body {
            width: 400px;
            height: 1900px;
            background-color: rgb(121, 179, 195);
        }

        .kill {
            width: 90px;
            height: 90px;
            background-color: rgb(212, 161, 228);
            /* position: absolute; */
            top: 400px;
        }
    </style>
</head>

<body>
    <div class="head"></div>
    <div class="body content">
        <div class="kill"></div>
    </div>

    <script>
        const head = document.querySelector('.head')
        const kill = document.querySelector('.kill')
        window.addEventListener('scroll',function(){
            const n = document.documentElement.scrollTop
            if( n >= kill.offsetTop){
                head.style.top = 0
            }else{
                head.style.top = '-80px'
            }
        })
    </script>
</body>

</html>
```



> 案例：**导航下划线跟随效果**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .content {
            margin: 0 auto;
        }

        .all {
            width: 900px;
            position: relative;
            /* 为 .line 定位提供参考 */
            padding-top: 20px;
        }

        .box {
            width: 900px;
            height: 70px;
            display: flex;
            justify-content: space-evenly;

        }

        .box1,
        .box2,
        .box3,
        .box4,
        .box5,
        .box5,
        .box6 {
            width: 60px;
            height: 60px;
            background-color: rgb(211, 211, 152);
            text-align: center;
            line-height: 60px;
            cursor: pointer;
        }

        .line {
            position: absolute;
            width: 60px;
            height: 20px;
            border-bottom: 2px solid #782ac7;
            transition: transform 0.3s ease;
      transform: translateX(0); /* 初始位置 */
        }
    </style>
</head>

<body>
    <div class="all content">
        <div class="box content">
            <div class="box1">
            </div>
            <div class="box2">
            </div>
            <div class="box3">
            </div>
            <div class="box4">
            </div>
            <div class="box5">
            </div>
            <div class="box6">
            </div>
        </div>
        <div class="line"></div>
    </div>


    <script>
        const line = document.querySelector('.line')
        const box = document.querySelector('.box')
        box.addEventListener('click', function (e) {
            if (e.target.tagName === 'DIV') {
                // console.log(11)
                line.style.transform = `translateX(${e.target.offsetLeft}px)`
            }
        })
    </script>
</body>

</html>
```

说明：

```
我们来一步步帮你理解：为什么 e.target.tagName === 'A' 时，就等于点击的是 <a> 标签？

🌟 关键点：e.target 是什么？
在事件处理中，e 是事件对象（event object），它包含了很多信息。其中：

e.target：表示实际被点击的元素（即触发事件的那个 DOM 元素）。
tagName：是这个元素的标签名，比如 'DIV'、'A'、'SPAN' 等。
✅ 举个例子
假设 HTML 结构如下：

html
深色版本
<ul class="tabs-list">
  <li><a href="#">首页</a></li>
  <li><a href="#">关于</a></li>
</ul>
你给 .tabs-list 添加了点击事件：

js
深色版本
list.addEventListener('click', function(e) {
  console.log(e.target.tagName); // 输出: "A"
});
当你点击“首页”这个链接时：

实际点击的是 <a> 标签。
所以 e.target 指向的就是那个 <a> 元素。
e.target.tagName 就是 'A'（大写）。
🔍 为什么要判断 === 'A'？
因为：

你可能点击的是 <a> 标签内部的文字，但你只想对 <a> 做操作。
如果你直接用 e.target 移动 .line，可能会误判点击了其他元素（比如 span 或 i）。
所以加一个判断：只有当点击的是 <a> 标签时才执行移动逻辑。
✅ 总结一句话：
e.target.tagName === 'A' 的意思是：“我点击的这个元素是不是一个 <a> 链接？如果是，就执行下面的操作。”

这确保了你的代码只响应 <a> 的点击，不会误触发其他元素。

💡 补充小知识：
tagName 返回的是大写字符串，所以要用 'A'，不是 'a'。
这种写法常用于「事件委托」，避免给每个 <a> 单独绑定事件。
希望这样解释清楚啦！✨
```

------------------

##### 📌 **DOM 元素尺寸与位置相关属性说明**

| 属性                            | 作用                                         | 说明                                                         |
| ------------------------------- | -------------------------------------------- | ------------------------------------------------------------ |
| `scrollLeft` 和 `scrollTop`     | 表示被卷去的头部和左侧（即滚动条滚动的距离） | 配合页面滚动使用，**可读写**                                 |
| `clientWidth` 和 `clientHeight` | 获取元素的可见宽度和高度                     | 不包含 `border`、`margin`，但包含 `padding` 和滚动条；用于 JS 获取元素大小，**只读属性** |
| `offsetWidth` 和 `offsetHeight` | 获取元素的总宽度和高度                       | 包含 `border`、`padding`、滚动条等，**只读属性**             |
| `offsetLeft` 和 `offsetTop`     | 获取元素距离其定位父级元素的左、上边距       | 用于获取元素在父容器中的相对位置，**只读属性**               |

##### ✅ 总结要点：

- **`client\*`**：不包含边框和外边距，适合计算可视区域。
- **`offset\*`**：包含边框和内边距，适合获取实际占位大小和位置。
- **`scroll\*`**：表示滚动偏移量，常用于滚动监听或定位。





### 日期对象

#### 实例化

- **实例化概念**：
   在代码中使用 `new` 关键字创建对象的操作称为 **实例化**。
- **创建时间对象并获取时间**：`new Date()`

##### 获取当前时间

```js
const date = new Date();
```

- 创建一个表示当前系统时间的 `Date` 对象。

##### 获取指定时间

```js
const date = new Date('2008-8-8');
console.log(date);
```

- 创建一个表示指定日期（如 2008 年 8 月 8 日）的 `Date` 对象。
- 可通过 `console.log()` 输出查看具体时间格式。

------

📌 **总结**：

- 使用 `new Date()` 实例化一个 `Date` 对象。
- 不带参数 → 当前时间；带字符串参数 → 指定时间。
- 是 JavaScript 中处理时间的基础方法

```html
    <script>
        // 得到当前的时间
        const date = new Date()
        console.log(date)
        // 指定时间
        const date1 = new Date('2025-9-24 16:38')
        console.log(date1)
    </script>

```

------------

#### 日期对象方法

| 方法            | 作用               | 说明                                                        |
| --------------- | ------------------ | ----------------------------------------------------------- |
| `getFullYear()` | 获取年份           | 返回四位数年份（如 2024）                                   |
| `getMonth()`    | 获取月份           | 取值范围为 `0 ~ 11`，需要`getMonth()+1`                     |
| `getDate()`     | 获取月份中的某一天 | 返回当月的日期（如 1~31），不同月份取值范围不同             |
| `getDay()`      | 获取星期           | 返回星期几，取值范围为 `0 ~ 6`，其中 0 表示周日，6 表示周六 |
| `getHours()`    | 获取小时           | 返回当前小时，取值范围为 `0 ~ 23`（24 小时制）              |
| `getMinutes()`  | 获取分钟           | 返回当前分钟，取值范围为 `0 ~ 59`                           |
| `getSeconds()`  | 获取秒             | 返回当前秒数，取值范围为 `0 ~ 59`                           |

------------

#### 时间戳

> 获取时间戳，是为了**把“时间”变成“数字”**，从而让程序能高效地**计算、比较、存储和控制时间相关逻辑**。

- **时间戳**：从 **1970年1月1日 00:00:00** 到现在的毫秒数（如：`1700000000000`）。
- **用途**：用于计算倒计时，比如未来时间 - 当前时间 = 剩余毫秒。
- 算法
  1. `未来时间戳 - 当前时间戳 = 剩余毫秒`
  2. 将毫秒转换为天、时、分、秒
- 示例
  - `2000ms - 1000ms = 1000ms`
  - `1000ms = 0小时0分1秒`

> 📌 时间戳是实现倒计时的核心工具。

##### 三种获取时间戳的方式

1. **使用 `getTime()` 方法**

   ```js
   const date = new Date();
   console.log(date.getTime());
   ```

   - 先创建 `Date` 实例，再调用 `.getTime()`

2. **简写：`+new Date()`**

   ```js
   console.log(+new Date());
   ```

   - 利用一元加号自动转换为时间戳
   - 无需实例化，更简洁

3. **使用 `Date.now()`**

   ```js
   console.log(Date.now());
   ```

   - 静态方法，直接返回当前时间戳
   - 无需创建对象，性能好

> 前两种可以返回指定时间的时间戳，第三种不行 只能得到当前的时间戳



> 案例：倒计时效果

用将来的时间戳减去现在的时间戳

**转换公式：**

- `d = parseInt(总秒数 / 60 / 60 / 24);` // 计算天数
- `h = parseInt(总秒数 / 60 / 60 % 24);` // 计算小时
- `m = parseInt(总秒数 / 60 % 60);` // 计算分钟
- `s = parseInt(总秒数 % 60);` // 计算当前秒数

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <div>
        <div class="offWork">一周年纪念日</div>
        <div class="clock">
            <span id="hour">00</span>
            <span id="minute">25</span>
            <span id="second">35</span>
        </div>
    </div>

    <script>
        // 封装函数
        function countColor() {
            // 获取当前时间戳
            const now = +new Date()
            // 获取将来的时间戳
            const fu = +new Date('2025-11-09 00:00:00')
            // console.log(now,fu)
            const count = (fu - now) / 1000
            console.log(count)

            d = parseInt(count / 60 / 60 / 24); // 计算天数
            h = parseInt(count / 60 / 60 % 24); // 计算小时
            h = h < 10 ? '0' + h : h
            m = parseInt(count / 60 % 60);// 计算分钟
            m = m < 10 ? '0' + m : m
            s = parseInt(count % 60); // 计算当前秒数
            s = s < 10 ? '0' + s : s
            console.log(d, h, m, s)

            // 把对应的事件写到对应的盒子里
            document.querySelector('#hour').innerHTML = h
            document.querySelector('#minute').innerHTML = m
            document.querySelector('#second').innerHTML = s
        }

        // 先调用一次
        // 开启定时器
        setInterval(countColor, 1000)
    </script>
</body>

</html>
```





### 节点操作

**DOM节点**

定义：DOM树里每一个内容都称之为**节点**

#### **节点类型**

- **元素节点**
  - 所有的标签，比如 `body`、`div`
  - `html` 是根节点
- **属性节点**
  - 所有的属性，比如 `href`
- **文本节点**
  - 所有的文本
- **注释节点**

![image-20250925091351275](C:\Users\32473\Desktop\笔记\web-img\image-20250925091351275-1759024436877-5.png)

#### 查找结点

##### 元素节点

###### 父节点查找： 

- **parentNode** 属性
  - 返回最近一级的父节点，找不到则返回 `null`

------

**语法示例：**

```js
子元素.parentNode
```

------

**说明：**
 `parentNode` 是 DOM 节点的一个属性，用于获取当前元素的直接父节点。如果该元素没有父节点（例如 `document` 节点），则返回 `null`。

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .parent {
            width: 300px;
            height: 300px;
            background-color: rgb(55, 19, 83);
        }

        .son {
            width: 100px;
            height: 100px;
            background-color: rgb(172, 142, 192);
        }
    </style>
</head>

<body>
    <div class="gf">
        <div class="parent">
            <div class="son"></div>
        </div>
    </div>

    <script>
        const baby = document.querySelector('.son')
        console.log(baby)
        console.log(baby.parentNode)   // 只能得到最近一级   // 得到父元素
        console.log(baby.parentNode.parentNode)  //得到祖先元素（爷爷）
    </script>
</body>

</html>
```



###### 子元素查询

- **childNodes**
   ✅ 获得所有子节点，包括文本节点（空格、换行）、注释节点等
- **children 属性（重点）**
   ✅ 仅获得所有元素节点（如 `<div>`、`<p>` 等标签）
   ✅ 返回的是一个伪数组（类数组对象）

------

**语法示例：**

```
父元素.children
```

------

**说明：**

- `childNodes` 返回包含所有类型的子节点（元素、文本、注释等）的 NodeList。
- `children` 只返回元素节点（即 HTML 标签），忽略文本和注释节点，常用于实际开发中获取子元素。
- `children` 返回的是一个“伪数组”，可以使用数组方法（如 `forEach`、`map`）但需注意兼容性或转换为真实数组。

```js
const ul = document.querySelector('ul')
console.log(ul.children)       // 得到的是伪数组 选择的是亲子元素
```





###### **兄弟关系查找：**

1. **下一个兄弟节点**
    → `nextElementSibling` 属性
    （获取当前元素的下一个同级元素节点）
2. **上一个兄弟节点**
    → `previousElementSibling` 属性
    （获取当前元素的上一个同级元素节点）

------

**说明：**

- `nextElementSibling` 和 `previousElementSibling` 仅返回**元素节点**，忽略文本节点、注释等非元素节点。
- 这两个属性常用于在 DOM 树中遍历相邻的兄弟元素。

```js
        const li2 = document.querySelector('ul li:nth-child(2)')
        console.log(li2.previousElementSibling) //上一个兄弟
        console.log(li2.nextElementSibling)   //下一个元素
```



##### 属性节点

###### 查找与操作方法

| 方法                    | 语法                                 | 作用                                                     | 示例                                                  |
| ----------------------- | ------------------------------------ | -------------------------------------------------------- | ----------------------------------------------------- |
| 1. `getAttribute()`     | `elem.getAttribute('name')`          | 获取指定属性的**字符串值**（保持原始 HTML 值）           | `link.getAttribute('href')` → `"https://example.com"` |
| 2. `hasAttribute()`     | `elem.hasAttribute('name')`          | 判断元素是否包含**某个属性**，返回 `true`/`false`        | `link.hasAttribute('target')` → `false`               |
| 3. `setAttribute()`     | `elem.setAttribute('name', 'value')` | 设置或**添加**一个属性                                   | `link.setAttribute('target', '_blank')`               |
| 4. `removeAttribute()`  | `elem.removeAttribute('name')`       | 移除指定属性                                             | `link.removeAttribute('class')`                       |
| 5. `element.attributes` | `elem.attributes`                    | 获取所有属性节点的**动态集合**（`NamedNodeMap`），可遍历 | `for (let attr of link.attributes) { ... }`           |
| 6. 直接属性访问         | `elem.name` 或 `elem.href`           | 快速访问标准 DOM 属性（注意：部分属性名不同）            | `link.href` → 完整 URL `link.id` → `'link1'`          |

###### 💡 使用建议

- 查值用：`getAttribute()`
- 判断是否存在用：`hasAttribute()`
- 修改用：`setAttribute()` / `removeAttribute()`
- 遍历所有属性用：`element.attributes`
- 快速读写标准属性（如 `id`, `src`, `href`）可用点语法（`elem.id`）



###### 作用

**`getAttribute()` —— 读取原始信息**

**🔧 作用：**获取 HTML 中写的原始属性值，常用于读取配置、自定义数据。

**💡 实际用途举例：** 读取自定义数据（`data-*`）

```html
<button data-user-id="1001" data-action="delete">删除</button>
```

```js
const btn = document.querySelector('button');
const userId = btn.getAttribute('data-user-id'); // "1001"
// 用于发送删除请求
fetch(`/api/user/${userId}`, { method: 'DELETE' });
```



**`hasAttribute()` —— 判断是否存在（开关式控制）**

**🔧 作用**：像“开关检测”一样，判断某个功能是否启用。

**💡 实际用途举例：** 表单验证：检查是否必填

```html
<input type="text" name="email" required>
```

```js
if (input.hasAttribute('required')) {
    if (!input.value) {
        alert('此项为必填');
    }
}
```



**`setAttribute()` —— 动态添加或修改功能**

🔧 作用：给元素“打标签”或“开功能”，是最常用的**动态控制手段**。

**💡 实际用途举例：** 添加 `class` 实现样式切换

```js
allExternalLinks.forEach(link => {
    link.setAttribute('target', '_blank');
    link.setAttribute('rel', 'noopener noreferrer'); // 安全性
});    //| 🔹 启用新窗口打开链接 |
```



**`removeAttribute()` —— 关闭功能或清理状态**

**🔧 作用**：“关掉开关”，恢复默认状态。

**💡 实际用途举例：** 关闭弹窗

```js
submitBtn.removeAttribute('disabled'); // 恢复可点击
```



**`element.attributes` —— 批量处理或调试**

**🔧 作用：**遍历所有属性，适合做**通用处理、日志、序列化**。

**💡 实际用途举例：**调试时查看元素有哪些属性



**直接属性访问（`elem.href`, `elem.id`）—— 快速高效读写**

**🔧 作用：**比 `getAttribute` 更快，且能获取**浏览器解析后的值**。

**💡 实际用途举例：** 获取完整 URL（自动解析）

```js
const a = document.querySelector('a');
console.log(a.href); // 输出 https://example.com/page
// 即使 HTML 写的是 "/page"，也能得到完整地址
```



#### 增加节点

##### 创建节点

创建一个指定标签名的**元素节点**



##### **创建元素节点方法：**

```js
// 创造一个新的元素节点
document.createElement('标签名')
```

------

**说明：**

- `document.createElement()` 是JavaScript中用于创建新元素节点的方法。
- 参数 `'标签名'` 是要创建的HTML标签名称，例如 `'div'`、`'p'`、`'span'` 等。
- 该方法返回一个**新的元素节点对象**，但不会自动添加到页面中，需通过 `appendChild()` 或其他插入方法将其加入DOM树。

```html
<script>
        // 创建节点
        const div = document.createElement('div')
        console.log(div)
</script>
```





#### 追加节点

- 插入到父元素的最后一个子元素：

  ```js
  // 插入到这个父元素的最后
  父元素.appendChild(要插入的元素)
  ```

- 插入到父元素中某个子元素的前面：

  ```js
  // 插入到某个子元素的前面
  父元素.insertBefore(要插入的元素, 在哪个元素前面)
  ```

------

**说明：**

- `appendChild()`：将指定节点添加为父元素的最后一个子节点。
- `insertBefore()`：将指定节点插入到父元素中某子元素的前面，第二个参数是目标参照元素。
- 新创建的节点必须通过这些方法插入 DOM 树，才能在页面上显示。

```js
        // 追加节点
        const ul = document.querySelector('ul')
        const li = document.createElement('li')
        li.innerHTML = '我是li'

        // insertBefore(插入的元素，放到那个元素的前面)
        ul.insertBefore(li,ul.children[0])
```





#### 克隆节点

- 使用 `元素.cloneNode(布尔值)` 复制一个已有节点。

- 参数说明：

  - `true`：克隆包含所有子节点（深克隆）。
  - `false`：仅克隆自身，不包含子节点（浅克隆）。

  > 深克隆是克隆节点本身和克隆其子节点
  >
  > 浅克隆是克隆节点本身

- 默认值为 `false`。

```html
<body>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>

    <script>
        const ul = document.querySelector('ul')
        // 克隆节点 元素.cloneNode
        const li1 = ul.children[0].cloneNode(true)
        // const li1 = document.querySelector('ul li:first-child')
        // 追加
        ul.appendChild(li1)
    </script>
</body>

```





#### 删除节点

- 在 JavaScript 原生 DOM 操作中，要删除元素必须通过**父元素删除**

- 语法：

  ```js
  父元素.removeChild(要删除的元素)
  ```

- 注：

  - ➤ 如不存在父子关系，则删除不成功

  - ➤ 删除节点与隐藏节点（

    ```css
    display: none
    ```

    ）有区别：

    - 隐藏节点仍存在于 DOM 中，只是不可见；
    - 删除节点则从 HTML 结构中彻底移除。

```html
<body>
    <ul>
        <li>nihao </li>
    </ul>

    <script>
        const ul = document.querySelector('ul')
        ul.removeChild(ul.children[0])
    </script>
</body>

```





### M端事件

移动端有其独特之处，例如**触屏事件 touch**（也称触摸事件），Android 和 iOS 均支持。

- **触屏事件 touch**：Android 和 iOS 都有
- **touch 对象**：代表一个触摸点，可能是手指或触控笔，用于响应用户对屏幕或触控板的操作

##### **常见的触屏事件**：

| 触屏 touch 事件 | 说明                            |
| --------------- | ------------------------------- |
| `touchstart`    | 手指触摸到一个 DOM 元素时触发   |
| `touchmove`     | 手指在一个 DOM 元素上滑动时触发 |
| `touchend`      | 手指从一个 DOM 元素上移开时触发 |

------

> ✅ 这些事件专为移动设备设计，常用于实现滑动、点击等交互行为。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div{
            width: 300px;
            height: 300px;
            background-color: rgb(155, 128, 119);
        }
    </style>
</head>
<body>
    <div></div>

    <script>
        const div = document.querySelector('div')
        div.addEventListener('touchstart',function(){
            console.log('开始了')
        })
        div.addEventListener('touchend',function(){
            console.log('结束了')
        })
        div.addEventListener('touchmove',function(){
            console.log('在移动')
        })
    </script>
</body>
</html>
```





### JS插件

- **插件**：别人写好的代码，我们只需复制对应代码，即可直接实现相应效果。
- **学习插件的基本过程**：
  - 熟悉官网，了解插件功能需求：
    https://www.swiper.com.cn/
  - 查看在线演示，找到符合需求的 demo：
    https://www.swiper.com.cn/demo/index.html
  - 查看基本使用流程：
    https://www.swiper.com.cn/usage/index.html
  - 查看 API 文档，配置自己的插件：
    https://www.swiper.com.cn/api/index.html
- **注意**：多个 Swiper 同时使用时，类名需注意区分，避免冲突。





### window对象

#### BOM（浏览器对象模型）

定义：是 JavaScript 操作浏览器的接口。

- 核心是 `window` 对象，它是全局对象，所有 JS 代码都在它的上下文中运行。
- `document`、`alert()`、`console.log()` 都是 `window` 的属性或方法。
- 全局变量和函数自动变成 `window` 的属性和方法。
- 调用时可以省略 `window`，比如 `alert()` 就等于 `window.alert()`。

👉 简单说：**`window` 是一切的起点，所有浏览器操作都从它开始。**

```html
    <script>
        console.log(document === window.document)
        function fn(){
            console.log(11)
        }
        window.fn()
        const num = 10
        console.log(window.num)
    </script>

```



#### js执行机制

JavaScript 是**单线程**的，意思是：**同一时间只能做一件事**。

- 比如添加和删除 DOM 元素，必须一个接一个来，不能同时进行。
- 所有任务排成队，前一个做完，后一个才开始。
- 如果某个 JS 代码执行太久，页面就会“卡住”，感觉不动了（阻塞渲染）。

👉 简单说：**JS 一次只能干一件事，干完才能干下一件，太慢会卡页面。**

解决：

为了解决这个问题，HTML5 引入了 **Web Worker**，可以让 JS 在后台开多个“线程”干活，不阻塞主线程。

于是就出现了：

- **同步**：按顺序执行，前面没完后面不能开始。
- **异步**：比如定时器、网络请求，可以“先走”，等结果回来再处理。

👉 简单说，本质区别：**这条流水线上各个流程的执行顺序不同。** 



##### 同步任务

 在主线程上按顺序执行，形成**“执行栈”**，一个接一个。

![image-20250925173738347](C:\Users\32473\Desktop\笔记\web-img\image-20250925173738347-1759024475138-7.png)

##### 异步任务：

 不阻塞主线程，通过回调函数实现。分三种：

1. **事件**：比如 `click`、`resize`
2. **资源加载**：比如 `load`、`error`
3. **定时器**：比如 `setTimeout`、`setInterval`

这些异步任务会先放进一个“任务队列”（也叫消息队列），等主线程空了，再依次执行。

👉 简单说：
 **同步：排队执行；异步：先放一边，等主线程空了再处理。**





##### 执行顺序：

1. 先执行 **执行栈** 中的同步任务（主车道）。
2. 异步任务（如 `setTimeout`）放入 **任务队列**（应急车道）。
3. 同步任务全部完成后，系统从任务队列中取出异步任务，依次执行。

👉 简单说：
 **先干完主线程的事，再处理“排队”的异步任务。**





#### 事件循环

##### 事件循环

定义：一个不断检查“是否有任务可执行”的机制，它连接了执行栈和任务队列，驱动整个异步流程



##### 执行栈

定义：JavaScript 执行代码的“主流程”，像一个函数调用的“栈”结构，先进后出。



##### 宏任务

定义：由浏览器或 Node.js 提供的异步操作，比如 `setTimeout`、`setInterval`、`I/O`、`UI 渲染` 等。



##### 微任务

定义：优先级更高的异步任务，比如 `Promise.then()`、`MutationObserver`、`process.nextTick`（Node.js）



##### 他们之间和事件循环的关系

执行栈 -->`同步任务 `/` 异步任务`

同步任务直接执行 ， 异步任务执行 --> `宏任务` / `微任务`

宏任务 -- > 宏任务队列  ， 微任务 -- > 微任务队列

微任务队列 将所有的 微任务 由`事件循环`推入执行栈中进行执行

全部执行完后

由浏览器决定渲染任务是否需要执行，不需要就算了，需要的话就由事件循环推入执行栈进行执行

这是一轮完成

第二轮

将宏任务队列里的排列第一的宏任务拿出来，由事件循环推入执行栈进行执行

开始第二轮执行

> 案例：

```js
console.log('1');

setTimeout(() => {
    console.log('2');
    Promise.resolve().then(() => {
        console.log('3');
    });
}, 0);

Promise.resolve().then(() => {
    console.log('4');
});

console.log('5');
```

输出结果：

```js
1
5
4
2
3
```





#### location对象

定义：`location` 对象是浏览器提供的，用来获取或修改当前页面的 URL。它既是 `window` 的属性，也是 `document` 的属性，可以直接使用。

主要用途：

1. **获取当前页面的 URL 信息**：如协议、主机名、端口、路径等。
2. **导航到新的页面**：通过修改 `location` 的属性或调用其方法，可以让浏览器跳转到另一个地址。
3. **重新加载当前页面**。
4. **操作 URL 的一部分而无需完全重定向**（例如使用 `replace()` 方法）。

> 案例：定时器并跳转

```html
<body>
    <a href="https://juejin.cn">支付成功<span>5</span>秒之后跳转</a>

    <script>
        const a = document.querySelector('a')
        let num = 5
        let timeID = setInterval(function(){
            num--
            a.innerHTML = `支付成功<span>${num}</span>秒之后跳转`
            if(num === 0){
                clearInterval(timeID)
                location.href = "https://juejin.cn"
            }
        },1000)
    </script>
</body>

```

##### 主要属性

假设当前页面的 URL 是：`https://www.example.com:8080/path/page.html?name=John&age=30#section1`

| 属性                      | 返回值                                                       | 说明                               |
| :------------------------ | :----------------------------------------------------------- | :--------------------------------- |
| `location.href`           | `"https://www.example.com:8080/path/page.html?name=John&age=30#section1"` | 完整的 URL                         |
| `location.protocol`       | `"https:"`                                                   | 使用的协议（包括冒号）             |
| `location.host`           | `"www.example.com:8080"`                                     | 主机名和端口号                     |
| `location.hostname`       | `"www.example.com"`                                          | 主机名（不包含端口）               |
| `location.port`           | `"8080"`                                                     | 端口号（如果未指定，则为空字符串） |
| `location.pathname`       | `"/path/page.html"`                                          | 路径部分                           |
| `location.search`         | `"?name=John&age=30"`                                        | 查询字符串（以 `?` 开头）          |
| `location.hash`           | `"#section1"`                                                | 哈希/锚点部分（以 `#` 开头）       |
| `location.reload`         |                                                              | 刷新                               |
| `location.reload（true）` |                                                              | 强制刷新                           |

```js
// 获取当前 URL 的各部分
console.log(location.href);        // 完整 URL
console.log(location.hostname);    // www.example.com
console.log(location.search);      // ?name=John&age=30

// 跳转到新页面
location.href = "https://www.google.com";
// 或者
location.assign("https://www.google.com");

// 替换当前页面（无历史记录）
location.replace("https://www.github.com");

// 重新加载页面
location.reload();

// 修改 hash，常用于单页应用路由
location.hash = "#profile";
```



##### 实际应用场景

- **前端路由**：现代 SPA（单页应用）框架（如 React Router、Vue Router）利用 `location.hash` 或 `history API` 配合 `location` 对象实现无刷新跳转。
- **URL 参数解析**：通过 `location.search` 提取查询参数。
- **页面跳转与重定向**：根据用户状态自动跳转登录页或主页。
- **安全检查**：验证当前页面是否运行在预期的域名下。





#### navigator对象

定义：`navigator` 对象是浏览器提供的一个内置 JavaScript 对象，用于**获取浏览器和设备的相关信息**。它属于 `window` 对象（即 `window.navigator`），在全局可以直接访问。

##### 常见属性（用于获取信息）

| 属性                      | 说明                                                         |
| ------------------------- | ------------------------------------------------------------ |
| `navigator.userAgent`     | 返回浏览器的用户代理字符串（如 Chrome、Firefox 版本及操作系统信息） |
| `navigator.platform`      | 返回运行浏览器的操作系统平台（如 `Win32`、`MacIntel`、`Linux x86_64`） |
| `navigator.language`      | 返回浏览器首选语言（如 `zh-CN`、`en-US`）                    |
| `navigator.languages`     | 返回用户可接受的语言数组（按优先级排序）                     |
| `navigator.cookieEnabled` | 返回布尔值，表示是否启用 Cookie                              |
| `navigator.onLine`        | 返回布尔值，表示设备是否联网（`true` 在线，`false` 离线）    |
| `navigator.plugins`       | 返回浏览器安装的插件列表（仅现代浏览器支持有限访问）         |
| `navigator.vendor`        | 返回浏览器厂商名称（如 `Google Inc.`）                       |

```js
console.log(navigator.userAgent); // 查看浏览器信息
console.log(navigator.language);  // 输出: zh-CN
console.log(navigator.onLine);    // 检查是否在线
```

##### 常见方法（用于功能检测或操作）

| 方法                                                         | 说明                                                         |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `navigator.geolocation.getCurrentPosition(success, error)`   | 获取用户当前位置（需用户授权），常用于地图或定位服务         |
| `navigator.clipboard.readText()`                             | 读取剪贴板中的文本（需 HTTPS 和用户权限）                    |
| `navigator.clipboard.writeText(text)`                        | 将文本写入剪贴板（实现“复制到剪贴板”功能）                   |
| `navigator.mediaDevices.getUserMedia({video: true, audio: true})` | 请求访问摄像头和麦克风（用于音视频通话、拍照等）             |
| `navigator.permissions.query()`                              | 查询某项权限（如地理位置、通知）的状态                       |
| `navigator.sendBeacon(url, data)`                            | 在页面卸载时异步发送少量数据到服务器（适合日志上报）         |
| `navigator.vibrate()`                                        | 控制设备振动（移动端有效，如 `navigator.vibrate(200)` 振动 200ms） |

> ⚠️ 注意：这些方法涉及隐私，通常需要用户授权。

```js
// 查看基本信息
console.log(navigator.userAgent);
console.log(navigator.language);
console.log(navigator.onLine ? '在线' : '离线');

// 复制文本到剪贴板
navigator.clipboard.writeText('Hello World').then(() => {
  alert('已复制！');
});

// 获取地理位置
if (navigator.geolocation) {
  navigator.geolocation.getCurrentPosition(position => {
    console.log(position.coords.latitude, position.coords.longitude);
  });
}
```



##### 实际用途

- **兼容性判断**：根据 `userAgent` 或特性检测适配不同浏览器。
- **功能检测**：判断是否支持某项 API（如地理定位）。
- **用户体验优化**：根据语言或网络状态调整页面行为。





#### history对象

定义：它是用来**操作浏览器会话历史记录**的对象。

解释：`history` 对象允许你在用户访问过的页面之间**前进、后退或跳转**，也可以在不刷新页面的情况下**修改历史记录**，常用于单页应用（SPA）中实现无刷新导航。

它属于 `window` 对象，所以可以直接使用：`window.history` 或简写为 `history`。

#####  常见方法

| 方法                | 说明                                                         |
| ------------------- | ------------------------------------------------------------ |
| `history.back()`    | 返回上一页（等同于点击浏览器“后退”按钮）                     |
| `history.forward()` | 前进到下一页（等同于点击“前进”按钮）                         |
| `history.go(n)`     | 跳转到历史记录中的某一页： - `go(-1)`：后退一页 - `go(1)`：前进一页 - `go(0)`：刷新当前页 |

##### 高级方法（HTML5 新增）——用于单页应用

| 方法                                      | 说明                                                         |
| ----------------------------------------- | ------------------------------------------------------------ |
| `history.pushState(state, title, url)`    | 在历史记录中添加一个新条目，**不刷新页面** — 常用于 SPA 添加路由 |
| `history.replaceState(state, title, url)` | 替换当前历史记录条目，**不会留下原页面记录**                 |
| `popstate` 事件                           | 当用户点击“前进/后退”按钮时触发，用于监听历史变化            |

##### 实际应用场景

- **单页应用（SPA）路由**：如 Vue Router、React Router 使用 `pushState` 实现 `/user`、`/profile` 等路径切换。
- **防止重复提交**：通过替换状态避免用户后退看到旧表单。
- **用户体验优化**：在动态加载内容后更新 URL，保持可书签性。

**注意事项**

- `pushState` 和 `replaceState` 不会触发页面刷新，但需要你自己处理页面内容变化。
- 出于安全考虑，不能读取历史记录中的具体 URL 列表（只能知道长度）。
- 操作 history 需确保目标 URL 与当前页面同源（协议 + 域名 + 端口相同）。

##### 实现路由跳转

 **核心方法**：`pushState()` 和 `replaceState()`

| 方法                                      | 作用                                           |
| ----------------------------------------- | ---------------------------------------------- |
| `history.pushState(state, title, url)`    | 添加一个新的历史记录条目（用户可后退）         |
| `history.replaceState(state, title, url)` | 替换当前历史记录条目（不新增记录），不刷新页面 |

> 📌 注意：这两个方法不会触发页面刷新，你需要自己更新页面内容。

语法：

```js
history.pushState(state, title, url);
```

- `state`：一个对象，用于存储该状态的相关数据（如页面标题、参数等），可为空 `{}`。
- `title`：页面标题（目前大多数浏览器忽略这个参数，可传空字符串 `""`）。
- `url`：新的 URL（可选，必须同源）。

##### `popstate` 事件

监听 `history` 对象的 `popstate` 事件非常简单，它是实现**单页应用（SPA）路由**的关键，用于响应用户点击**浏览器前进、后退按钮**时的 URL 变化。

**`popstate` 事件的特点**

1. **触发时机**：
   - 用户点击浏览器的 **后退（Back）** 按钮
   - 用户点击浏览器的 **前进（Forward）** 按钮
   - 调用 `history.back()`、`history.forward()`、`history.go()` 时
2. **`event.state` 是什么？**
   - 就是之前调用 `history.pushState(state, ...)` 或 `history.replaceState(state, ...)` 时传入的 `state` 对象。
   - 如果是普通页面跳转（非 pushState），`event.state` 为 `null`。

**监听 `popstate` 事件的步骤：**

1. 使用 `window.addEventListener('popstate', handler)`。
2. 在事件处理函数中，通过 `event.state` 获取之前保存的状态。
3. 根据 `location.pathname` 或 `event.state` 更新页面内容。

> 💡 **一句话**：`popstate` 是你实现“无刷新前进后退”的耳朵，专门听浏览器历史变化。



### 本地存储

本地存储是放在浏览器里面的

定义：本地存储（Local Storage）是现代Web浏览器提供的一种在用户本地设备上存储数据的技术。允许网站在用户的浏览器中保存相对大量的数据（通常每个域名可达5-10MB），并且这些数据没有过期时间，除非被显式删除或用户清除浏览器缓存。

> 注意：本地存储只能存字符串类型

#### 主要特点：

1. **持久性**：与会话存储（sessionStorage）不同，本地存储的数据不会因为关闭浏览器或重启电脑而丢失。数据会一直保留在用户的设备上，直到被程序删除或用户手动清除浏览器数据。
2. **同源策略**：本地存储遵循同源策略，即只有同源（相同的协议、域名和端口）的页面才能访问同一份本地存储数据。这保证了数据的安全性，防止跨站访问。
3. **客户端存储**：所有数据都存储在用户的浏览器中，不会随每次HTTP请求发送到服务器，这减少了网络传输的开销。
4. **数据类型**：本地存储只能存储字符串类型的数据。如果需要存储对象或数组，需要先使用`JSON.stringify()`将其转换为字符串，读取时再用`JSON.parse()`解析。

#### 常用方法（JavaScript）：

键值对：key : 键 		value : 值  

- `localStorage.setItem(key, value)`：存储数据。
- `localStorage.getItem(key)`：根据键获取数据。
- `localStorage.removeItem(key)`：删除指定键的数据。
- `localStorage.clear()`：清除所有数据。
- `localStorage.key(index)`：获取指定索引的键名。





#### 分类

##### 1. `localStorage`

- **生命周期**：**持久化**存储，除非主动清除，否则数据长期保留。

- **作用域**：同源策略下共享（所有同源窗口/标签页可访问）。

- **容量**：通常 5–10 MB。

- **使用场景**：用户设置、主题偏好、离线缓存等长期数据。

  

**语法：**（往里面存数值，会被转变为字符串）

存储数据：`localStorage.setItem(key, value)`：存储数据

获取数据：`localStorage.getItem(key)`：根据键获取数据

删除数据：`localStorage.removeItem(key)`：删除指定键的数据。

##### 2. `sessionStorage`

- **生命周期**：仅限当前会话。关闭标签页或窗口后**自动清除。**
- **作用域**：仅当前标签页会话内有效，不同标签页不共享。
- **容量**：与 `localStorage` 相当。
- **使用场景**：临时状态保存、表单数据防丢失、单次会话数据。

> ✅ 共同点：仅支持字符串存储，API 简洁（`setItem`, `getItem` 等）





#### 处理复杂数据类型

> 注意：JSON对象，属性和值有引号，而是引号统一是双引号

在浏览器的本地存储机制中，**原生仅支持字符串类型**的数据存储。因此，处理复杂数据类型（如对象、数组、日期、Blob、函数等）需要通过特定策略进行**序列化与反序列化**，或选择更高级的存储方案。

##### `localStorage` / `sessionStorage`：仅支持字符串，需手动序列化

**✅ 支持处理的复杂类型：**

- 对象（Object）
- 数组（Array）
- 嵌套结构
- 日期（需特殊处理）

**❌ 不支持直接存储：**

- `undefined`, `function`, `symbol`
- `Date` 对象（会转为字符串）
- `Map`, `Set`, `RegExp`, `Error`
- `Blob`, `File`, `ArrayBuffer`

**✅ 正确做法：使用 `JSON.stringify()` 和 `JSON.parse()`**

```html
<script>
const obj = {
  uname: 'pink老师',
  age: 18,
  gender: '女'
};

// 1. 复杂数据类型存储必须转换为 JSON 字符串存储
localStorage.setItem('obj', JSON.stringify(obj));
// → 存储的是字符串：{"uname":"pink老师","age":18,"gender":"女"}

// 2. 取出时需将 JSON 字符串转换回对象
const storedStr = localStorage.getItem('obj');
const restoredObj = JSON.parse(storedStr);
console.log(restoredObj); // { uname: 'pink老师', age: 18, gender: '女' }
</script>
```

```js
// 存储复杂对象
const user = {
  name: "Alice",
  age: 30,
  tags: ["developer", "web"],
  lastLogin: new Date() // 注意：Date 会被转为字符串
};

localStorage.setItem('user', JSON.stringify(user));

// 读取并还原
const stored = localStorage.getItem('user');
const userData = JSON.parse(stored);
console.log(userData.lastLogin); // 字符串，非 Date 对象
```



**`JSON.stringify()` 和 `JSON.parse()`的区别**

| 方法                    | 作用                                                         | 方向                          |
| ----------------------- | ------------------------------------------------------------ | ----------------------------- |
| `JSON.stringify(value)` | 将 JavaScript 值（对象、数组、字符串等）转换为 **JSON 格式的字符串**，转换为字符串（存） | ✅ 序列化（Object → String）   |
| `JSON.parse(string)`    | 将 **JSON 格式的字符串** 解析还原为对应的 JavaScript 值（对象、数组等），转换为对象 （取） | 🔙 反序列化（String → Object） |

```js
const obj = { name: "Alice", age: 25, city: "Beijing" };

// 1. 序列化：对象 → JSON 字符串
const jsonString = JSON.stringify(obj);
console.log(jsonString); // '{"name":"Alice","age":25,"city":"Beijing"}'
console.log(typeof jsonString); // "string"

// 2. 反序列化：JSON 字符串 → 对象
const parsedObj = JSON.parse(jsonString);
console.log(parsedObj); // { name: "Alice", age: 25, city: "Beijing" }
console.log(typeof parsedObj); // "object"
```

| 对比项           | `JSON.stringify()`                   | `JSON.parse()`            |
| ---------------- | ------------------------------------ | ------------------------- |
| 功能             | 序列化（对象 → 字符串）              | 反序列化（字符串 → 对象） |
| 输入             | JavaScript 值                        | JSON 字符串               |
| 输出             | JSON 字符串                          | JavaScript 值             |
| 关系             | “打包”                               | “拆包”                    |
| 必须配合使用场景 | `localStorage`、API 请求、消息传递等 |                           |





### 正则表达式

定义：是用于匹配**字符串**中**字符组合**的模式

作用：**验证数据格式**、**查找匹配内容**、**替换文本内容**、**提取结构化信息**

#### 定义正则表达式语法：

正则表达式使用：

1. 定义规则（使用字面量）

`const 变量名 = /表达式/`

其中 /  / 是正则表达式字面量

2. 是否匹配

`test()` 方法

用来查看正则表达式与指定的字符串是否匹配。

**语法：**

```
regObj.test(被检测的字符串)
```

**示例：**

```js
// 要检测的字符串
const str = 'IT培训,前端开发培训,IT培训课程,web前端培训,Java培训,人工智能培训';

// 1. 定义正则表达式，检测规则
const reg = /前端/;

// 2. 检测方法
console.log(reg.test(str)); // true
```

------

**说明：**

- `test()` 方法返回一个布尔值（`true` 或 `false`），表示字符串是否与正则表达式匹配。
- 在示例中，正则表达式 `/前端/` 在字符串中找到了匹配项，因此返回 `true`。





#### 语法

正则表达式的语法是一套由**普通字符**和**特殊元字符**（或称元字符、元符号）组成的规则

##### **.检索（查找）符合规则的字符串：**

**`exec()` 方法**

在一个指定字符串中执行一个搜索匹配。

##### **语法：**

```
regObj.exec(被检测字符串)
```

##### **示例：**

```js
// 要检测的字符串
const str = 'IT培训,前端开发培训,IT培训课程,web前端培训,Java培训,人工智能培训';

// 1. 定义正则表达式，检测规则
const reg = /前端/;

// 2. 检测方法
console.log(reg.exec(str)); // 返回的是数组
```

##### **输出结果：**

```js
[
  '前端', 
  index: 5, 
  input: 'IT培训,前端开发培训,IT培训课程,web前端培训,Java培训,人工智能培训', 
  groups: undefined
]
```

##### **说明：**

- 如果匹配成功，`exec()` 方法返回一个数组，包含匹配的文本、索引位置、原字符串等信息。
- 如果匹配失败，`exec()` 方法返回 `null`。

#### 判断是否符合规则的字符串

`test()` 方法只返回 `true` 或 `false`，不会给出具体的匹配内容。要**提取**内容，JavaScript 提供了其他方法，最常用的是 `exec()` 和 `match()`。

##### 1. 使用 `exec()` 方法提取内容

`exec()` 方法会返回一个数组，包含匹配结果和分组信息。

- **语法**：`regObj.exec(被检测的字符串)`
- 返回值
  - 如果找到匹配，返回一个数组。
    - `array[0]`：完整的匹配项。
    - `array[1], array[2], ...`：如果使用了括号 `()` 分组，这些是各分组的内容。
  - 如果未找到匹配，返回 `null`。

示例：提取课程名称

```js
// 要检测的字符串
const str = 'IT培训,前端开发培训,IT培训课程,web前端培训,Java培训,人工智能培训';

// 定义正则表达式，使用括号()来捕获我们想要的部分
// 这里捕获“培训”前面的所有文字
const reg = /(.+)培训/;

// 执行提取
const result = reg.exec(str);

console.log(result); // 输出: ['IT培训', 'IT'] (数组形式)
console.log(result[0]); // 输出: IT培训 (完整匹配)
console.log(result[1]); // 输出: IT (第一个分组捕获的内容)
```

> **注意**：`exec()` 只能找到**第一次**匹配。如果需要找所有匹配，可以循环使用或用 `match()`。





##### 2. 使用 `match()` 方法提取内容

`match()` 方法更常用于查找**所有**匹配项。

- **语法**：`字符串.match(正则表达式)`
- 返回值
  - 如果正则表达式有全局标志 `g`，返回一个包含所有匹配项的数组。
  - 如果没有 `g` 标志，行为类似于 `exec()`，返回一个包含第一个匹配项及其分组的数组。
  - 如果没有匹配，返回 `null`。

示例：提取所有以“培训”结尾的课程名

```js
// 要检测的字符串
const str = 'IT培训,前端开发培训,IT培训课程,web前端培训,Java培训,人工智能培训';

// 定义正则表达式，加上全局标志 g
const reg = /(.+)培训/g;

// 执行提取，获取所有匹配
const results = str.match(reg);

console.log(results); // 输出: ['IT培训', '前端开发培训', 'IT培训课程', 'web前端培训', 'Java培训', '人工智能培训']
```

示例：提取所有课程名称（不包括“培训”）

```js
// 使用 match() 并结合分组
const str = 'IT培训,前端开发培训,IT培训课程,web前端培训,Java培训,人工智能培训';
const reg = /(.+)培训/g;

const results = str.match(reg);
// 结果是一个数组，每个元素都是完整的匹配项，如 "IT培训"

// 如果只想提取括号内的部分，需要更复杂的处理（例如遍历结果数组并手动分割），或者使用 exec() 循环。
```

------

总结

| 方法      | 用途                     | 返回值                            |
| :-------- | :----------------------- | :-------------------------------- |
| `test()`  | **判断**是否匹配         | `true` 或 `false`                 |
| `exec()`  | **提取**单个匹配项及分组 | 数组（含匹配内容、分组）或 `null` |
| `match()` | **提取**所有匹配项       | 包含所有匹配项的数组，或 `null`   |

**结论**：

- 您图片中的 `test()` 方法是用来**判断**的，不是用来**提取**的。
- 如果您想**提取**字符串中的特定内容，应该使用 `exec()` 或 `match()` 方法。
- 在您的例子中，如果想提取出像 "IT"、"前端开发"、"IT培训课程" 等这些“培训”前面的文字，可以使用 `exec()` 或 `match()` 配合正则表达式 `/(.+)培训/` 来实现。





#### 元字符（特殊字符）

元字符写法：[ a-z ]

定义：元字符是一些具有特殊含义的字符，可以极大**提高灵活性**和**强大的匹配功能**

##### 边界符

(表示位置，开头和结尾，必须用什么开头，用什么结尾)

定义：正则表达式中的边界符用来提示字符所处的位置，主要有两个字符

- **`^`**：匹配输入字符串的**开始**位置（在多行模式下也匹配行首）。
- **`$`**：匹配输入字符串的**结束**位置（在多行模式下也匹配行尾）。

> 如果 ^ 和 $ 在一起，表示必须精确匹配

```js
console.log(/哈/.test('哈哈')) // true
console.log(/哈/.test('二哈')) // true
console.log('-------------------')

// 1. 边界符
console.log(/^哈/.test('哈'))   // true
console.log(/^哈/.test('哈哈')) // true
console.log(/^哈/.test('二哈')) // false
console.log(/^哈$/.test('哈'))  // true    只有这种情况为true 否则全是false
console.log(/^哈$/.test('哈哈')) // false

console.log('-------------------')
```



##### 量词

定义：量词用来**设定某个模式出现的次数**

| 量词    | 说明（其中不能包含其他任何元素） |
| ------- | -------------------------------- |
| `*`     | 重复零次或更多次                 |
| `+`     | 重复一次或更多次                 |
| `?`     | 重复零次或一次                   |
| `{n}`   | 重复 n 次                        |
| `{n,}`  | 重复 n 次或更多次                |
| `{n,m}` | 重复 n 到 m 次（包含 n 和 m）    |

```js
console.log('-------------------')
// 量词 * 类似 >=0 次
console.log(/^哈$/.test('哈')) // true
console.log(/^哈*$/.test('')) // true
console.log(/^哈*$/.test('哈')) // true
console.log(/^哈*$/.test('哈哈')) // true
console.log(/^哈*$/.test('二哈很傻')) // false
```

量词 + 类似 >=1 次

```js
// 量词 + 类似 >=1 次
console.log(/^哈$/.test('哈')) // true
console.log(/^哈+$/ .test('')) // false
console.log(/^哈+$/ .test('哈')) // true
console.log(/^哈+$/ .test('哈哈')) // true
console.log(/^哈+$/ .test('二哈很傻')) // false
console.log(/^哈+$/ .test('哈很傻')) // false
console.log(/^哈+$/ .test('哈很哈')) // false
```

量词 ? 类似 0 || 1 次

```js
// 量词 ? 类似 0 || 1 次
console.log(/^哈?$/.test('')) // true
console.log(/^哈?$/.test('哈')) // true
console.log(/^哈?$/.test('哈哈')) // true
console.log(/^哈?$/.test('二哈很傻')) // false
console.log(/^哈?$/.test('哈很傻')) // false
console.log(/^哈?$/.test('哈很哈')) // false
```

量词 {n} 写几，就必须出现几次

```js
// 量词 {n} 写几，就必须出现几次
console.log(/^哈{4}$/.test('哈'))
console.log(/^哈{4}$/.test('哈哈'))
console.log(/^哈{4}$/.test('哈哈'))
console.log(/^哈{4}$/.test('哈哈哈哈'))
console.log(/^哈{4}$/.test('哈哈哈哈哈哈'))
console.log('-------------------')
```

量词 {n,} >=n 次

```js
// 量词 {n,} >=n 次
console.log(/^哈{4,}$/.test('哈'))
console.log(/^哈{4,}$/.test('哈哈'))
console.log(/^哈{4,}$/.test('哈哈'))
console.log(/^哈{4,}$/.test('哈哈哈哈'))
console.log(/^哈{4,}$/.test('哈哈哈哈哈哈'))
console.log('-------------------')
```

量词 {n,m} 逗号左右**两侧千万不能有空格**  >=n && <=m

```js
// 量词 {n,m} 逗号左右两侧千万不能有空格  >=n && <=m
console.log(/^哈{4,6}$/ .test('哈'))
console.log(/^哈{4,6}$/ .test('哈哈'))
console.log(/^哈{4,6}$/ .test('哈哈'))
console.log(/^哈{4,6}$/ .test('哈哈哈哈'))
console.log(/^哈{4,6}$/ .test('哈哈哈哈哈哈'))
console.log(/^哈{4,6}$/ .test('哈哈哈哈哈哈哈'))
console.log('-------------------')
```



##### 字符类

**定义：**

- 使用方括号 `[]` 定义，表示匹配方括号内的任意一个字符。
- **核心概念：** 一次写多个字符，但只匹配其中“任意一个”。

**示例与说明：**

| 正则表达式 | 含义                                   |
| ---------- | -------------------------------------- |
| `[aeiou]`  | 匹配任一英文元音字母（a、e、i、o、u）  |
| `[0-9]`    | 匹配任一数字（0 到 9）                 |
| `[a-z]`    | 匹配任一小写英文字母                   |
| `[A-Z]`    | 匹配任一大写英文字母                   |
| `[a-zA-Z]` | 匹配任一英文字母（大小写均可）         |
| `[abc123]` | 匹配 a、b、c、1、2、3 中的任意一个字符 |

**注意事项：**

1. **仅匹配一个字符** - 如 `[abc]` 表示匹配 a 或 b 或 c 中的一个。
2. **使用 `-` 表示范围** - 如 `[a-z]` 表示从 a 到 z 的所有小写字母。
3. **特殊字符在 `[...]` 中通常失去特殊含义** - 如 `[.*?]` 匹配的是字面意义的 `.`, `*`, `?`。
4. **`^` 在开头表示“否定”** - 如 `[^abc]` 表示匹配非 a、b、c 的字符。
5. **`]` 和 `-` 的转义问题** - `]` 必须放在第一个或转义；`-` 可以放在开头或结尾。

#### 预定义类

**定义：**

- 某些常见模式的简写方式。

**示例与说明：**

| 预定义类 | 含义                                                       |
| -------- | ---------------------------------------------------------- |
| `\d`     | 匹配 0-9 之间的任一数字，相当于 `[0-9]`                    |
| `\D`     | 匹配所有 0-9 以外的字符，相当于 `[^0-9]`                   |
| `\w`     | 匹配任意的字母、数字和下划线，相当于 `[A-Za-z0-9_]`        |
| `\W`     | 匹配除字母、数字和下划线以外的字符，相当于 `[^A-Za-z0-9_]` |
| `\s`     | 匹配空格（包括换行符、制表符等），相当于 `[\t\r\n\v\f]`    |
| `\S`     | 匹配非空格的字符，相当于 `[^ \t\r\n\v\f]`                  |

**日期格式正则表达式的示例：**

```
^\d{4}-\d{1,2}-\d{1,2}
```

- 描述了形如

```
2024-12-25
```

的日期格式：

- `^`：匹配字符串的开始。
- `\d{4}`：匹配四位数字（年份）。
- `-`：匹配连字符。
- `\d{1,2}`：匹配 1 到 2 位数字（月份或日数）。



> 案例：输入语法

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>

    </style>
</head>

<body>
    <input type="text">
    <span></span>

    <script>
        const reg = /^[a-zA-Z0-9-_]{6,16}$/
        const input = document.querySelector('input')
        const span = input.nextElementSibling
        input.addEventListener('blur', function () {
            if (reg.test(this.value)) {
                span.innerHTML = '输入正确'
            } else {
                span.innerHTML = '请输入6-10位的英文数字下划线'
            }
        })

    </script>
</body>

</html>
```





#### 修饰符

**定义**：在正则表达式中，**修饰符**（也称 **标志**，英文：**flags**）是用于**控制匹配行为的可选参数**。它们不参与模式本身的字符匹配，而是**影响整个正则表达式的解释方式和搜索行为**，例如是否区分大小写、是否全局匹配等。

##### **作用：**

修饰符用于约束正则表达式的执行行为，如是否区分大小写、是否全局匹配等。

------

##### **语法：**

```
/表达式/修饰符
```

------

##### **常用修饰符：**

| 修饰符 | 含义                                                | 示例                           |
| ------ | --------------------------------------------------- | ------------------------------ |
| `i`    | **ignore**（忽略大小写） 匹配时字母不区分大小写     | `/a/i.test('A')` → `true`      |
| `g`    | **global**（全局匹配） 查找所有匹配项，而非仅第一个 | `/a/g.exec("aa")` 返回所有匹配 |

------

**示例说明：**

```
console.log(/a/i.test('a'))  // true
console.log(/a/i.test('A'))  // true
```

- 使用 `i` 修饰符后，`/a/i` 能同时匹配 `'a'` 和 `'A'`。
- 若没有 `i`，则 `/a/.test('A')` 返回 `false`。

------

✅ **小结：**

- `i`：忽略大小写，提升匹配灵活性。
- `g`：全局匹配，适用于需要提取多个结果的场景。
- 修饰符可组合使用，如 `/a/ig` 表示“全局且忽略大小写”。

-----

##### **`replace` 替换**

✅ 作用：

使用正则表达式或字符串，将原字符串中的匹配内容替换为指定文本。

------

🔧 语法：

```
字符串.replace(/正则表达式/, '替换的文本')
```

- `字符串`：要操作的原始字符串。
- `/正则表达式/`：用于匹配目标内容（支持修饰符如 `g`, `i`）。
- `'替换的文本'`：用于替换匹配部分的新内容。

关键点：

| 特性                       | 说明                                               |
| -------------------------- | -------------------------------------------------- |
| **默认只替换第一个匹配项** | 若需替换所有匹配项，必须加上 `g`（global）修饰符。 |
| **支持正则表达式**         | 可使用字符类、量词、分组等高级功能进行灵活匹配。   |
| **支持修饰符**             | 常用修饰符： - `i`：忽略大小写 - `g`：全局替换     |

```js
str.replace(/java/i, '前端') // 忽略大小写，但只替换第一个
str.replace(/java/gi, '前端') // 全局且忽略大小写
```





### 防抖

`debounce()`

单位时间内，频繁触发事件，只执行最后一次（只要被打断就要重新来）

手写防抖函数：

1. 核心是利用setTimeout定时器来实现
2. 每次鼠标移动（事件触发）的时候都要先判断是否有定时器，如果有先清除以前的定时器
3. 如果没有定时器，则开启定时器，存入到定时器变量里面
4. 定时器里面写函数调用

```js
function debounce(fn, t) {
    let timer;
    
    // 返回一个匿名函数
    return function () {
        // 2.3.4
        if (timer) clearTimeout(timer);
        timer = setTimeout(function () {
            fn(); // 加小括号调用 fn 函数
        }, t);
    }
}

// 使用示例：为 box 元素添加 mousemove 事件监听，使用防抖处理
box.addEventListener('mousemove', debounce(mouseMove, 500));
```





### 节流

`throttle`

单位时间内，频繁触发事件，只执行一次

`_.throttle(fun,时间)`

手写节流函数：

1.  声明一个定时器变量
2. 当鼠标每次滑动都先判断是否有定时器了，如果有定时器则不开启新定时器
3. 如果没有定时器则开启定时器，记得存到变量里面

4. 定时器里面调用执行的函数
5. 定时器里面要把定时器清空

```js
function throttle(fn, t) {
    let timer = null;
    return function () {
        if (!timer) {
            timer = setTimeout(function () {
                fn(); // 执行原函数
                // 清空定时器
                timer = null;
            }, t);
        }
    };
}

// 使用示例：为 box 元素添加 mousemove 事件监听，使用节流处理
box.addEventListener('mousemove', throttle(mouseMove, 3000));
```



| 性能优化             | 说明                                                         | 使用场景                                                     |
| -------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **防抖（Debounce）** | 在单位时间内频繁触发事件，**只执行最后一次**。若在时间间隔内再次触发，则重新计时。 | - 搜索框实时搜索输入 - 手机号、邮箱验证输入检测 - 表单提交前的校验等 |
| **节流（Throttle）** | 在单位时间内频繁触发事件，**最多只执行一次**。无论触发多少次，每隔固定时间执行一次。 | - 高频事件：`mousemove` - 页面尺寸变化：`resize` - 滚动条滚动：`scroll` |





## JS高级



### 浏览器内核

✅ 什么是浏览器内核？（Browser Engine / Rendering Engine）

**我们常说的“浏览器内核”，实际上是指“排版引擎”（Layout Engine），也就是负责把 HTML/CSS 渲染成可视页面的核心模块。常见的内核有 Gecko、Trident、WebKit 和 Blink，它们决定了浏览器如何解析和显示网页。**

我们常说的“浏览器内核”，实际上是指 **排版引擎（Layout Engine）**，也叫：

- 浏览器引擎（Browser Engine）
- 页面渲染引擎（Rendering Engine）
- 样版引擎

它的核心职责是：**将 HTML 和 CSS 渲染成用户可见的网页**。

🔍 主流浏览器内核对比

| 内核名称    | 开发者                | 使用浏览器                       | 特点                                           |
| ----------- | --------------------- | -------------------------------- | ---------------------------------------------- |
| **Gecko**   | Mozilla               | Firefox、Netscape（早期）        | 功能完整、兼容性强，但性能略低                 |
| **Trident** | 微软                  | IE4～IE11                        | 专有、兼容性差，已淘汰（新版 Edge 改用 Blink） |
| **WebKit**  | 苹果（基于 KHTML）    | Safari、旧版 Chrome（2008–2013） | 轻量、高效、稳定                               |
| **Blink**   | Google（WebKit 分支） | Chrome、Edge（新版）、Opera      | 高性能、模块化强、更新快                       |

> 💡 当前主流：**Blink（Chrome/Edge/Opera） + WebKit（Safari）**





四大主流浏览器内核

| 内核名称    | 开发者                   | 使用浏览器                       | 特点                                      |
| ----------- | ------------------------ | -------------------------------- | ----------------------------------------- |
| **Gecko**   | Mozilla                  | Firefox、Netscape（早期）        | 功能完整，兼容性强，但性能相对较低        |
| **Trident** | 微软                     | IE4~IE11                         | 专有，兼容性差，已淘汰（Edge 改用 Blink） |
| **WebKit**  | 苹果（基于 KHTML）       | Safari、旧版 Chrome（2008–2013） | 轻量、高效、稳定，影响广泛                |
| **Blink**   | Google（从 WebKit 分支） | Chrome、Edge（新版）、Opera      | 高性能、模块化强、更新快                  |





### 浏览器渲染过程

![image-20251027161620432](./web-img/image-20251027161620432.png)

浏览器将 HTML 文件变成你眼前看到的网页，经历以下五个阶段：

1. **加载资源**
    下载 HTML 文件和 CSS 样式表。
2. **构建 DOM 与样式规则**
   - 解析 HTML → 生成 **DOM 树**（页面结构）
   - 解析 CSS → 生成 **Style Rules**（样式规则）
3. **生成渲染树（Render Tree）**
    将 DOM 与样式规则结合，**只保留可见元素**，形成 Render Tree。
4. **布局（Layout / Reflow）**
    计算每个元素的**位置、大小**（考虑容器、margin、定位、字体等）。
5. **绘制与显示（Painting → Display）**
   - **Painting**：将元素绘制成像素（颜色、文字、边框等）
   - **Display**：最终呈现在屏幕上

> 🌟 **一句话总结**：
>  浏览器先解析 HTML 和 CSS，构建 DOM 与样式；合并成渲染树后，计算布局、绘制像素，最终显示网页。

解释：

浏览器首先下载 HTML 和 CSS 文件；接着，它一边解析 HTML 构建出表示页面结构的 **DOM 树**，一边解析 CSS 生成 **样式规则**；然后，把这两者结合起来，为每个可见元素配上样式，形成 **渲染树（Render Tree）**；再根据渲染树计算每个元素的位置和大小（这叫 **布局** 或 **重排**）；之后，把所有元素绘制成像素（这叫 **绘制** 或 **重绘**）；最后，把这些像素显示在屏幕上，你就看到了完整的网页。



**浏览器内核和JS 引擎的关系**

浏览器内核负责“渲染页面”，JavaScript 引擎负责“执行脚本”，两者通过 DOM/CSSOM 接口紧密协作——内核提供舞台，JS 引擎在舞台上“表演”，但最终画面由内核绘制。

- **浏览器内核**（如 Blink）：负责**渲染页面**（HTML/CSS 解析、布局、绘制）。
- **JavaScript 引擎**（如 V8）：负责**执行 JS 代码**。

🔗 二者如何协作？

- 内核在解析 HTML 时遇到 `<script>`，会**暂停解析**，调用 JS 引擎执行脚本。
- JS 引擎通过内核提供的 **DOM/CSSOM 接口** 操作页面（如 `document.getElementById`）。
- 页面更新后，内核**重新渲染**（可能触发重排/重绘）。

> 🎭 **比喻**：
>  内核是“舞台”，JS 引擎是“演员”。演员不能自己搭台，但可以在舞台上表演；最终画面由舞台呈现。



### V8引擎

定义：v8是用**C++**编写的谷歌开源高性能JS和WebAssembly引擎，用于谷歌和Node.JS

作用：将JS 代码直接转换为机器码以便计算机能真正理解代码，然后执行转换或编译后的代码

支持在以下系统上运行：

- Windows 7 或更高版本
- macOS 10.12 及以上版本
- 使用 x64、IA-32、ARM 或 MIPS 处理器的 Linux 系统

v8也可以独立运行，也可以嵌入到任何C++应用程序中

![image-20251027090218836](./web-img/image-20251027090218836.png)

![image-20251028114025509](./web-img/image-20251028114025509.png)

JavaScript 源代码首先经过**词法分析和语法分析**，被解析成一棵**抽象语法树（AST）**；然后由 **Ignition** 将 AST 编译为**字节码**并快速执行，同时收集运行时信息（如变量类型）；如果某段代码频繁执行，**TurboFan** 会根据这些信息将其优化为高效的**机器码**以提升性能；当运行时假设不成立时，会触发**去优化（Deoptimization）**，退回到字节码继续执行。整个过程实现了“快启动 + 高性能”的平衡。







四个关键组件：**Ignition、TurboFan、Orinoco 和 SparkPlug**

**Ignition：字节码解释器**

定义：

Ignition 是 V8 的**解释器**，它将 JavaScript 源代码先解析为**抽象语法树（AST）**，再编译成一种紧凑的**字节码（Bytecode）**，然后直接解释执行这些字节码。

作用：

Ignition 就是一个专门负责读取并执行字节码的解释器，它是 V8 实现快速启动和收集优化情报的关键部件。



**TurboFan：优化编译器**

定义：

TurboFan 是 V8 的**高级优化编译器**，负责将热点函数（频繁执行的代码）从字节码进一步编译为**高度优化的本地机器码**。

作用：

这是 TurboFan 最聪明的地方，它**不随意优化**，它的优化完全依赖于 Ignition 收集的性能反馈数据

负责把 JavaScript 那些高级、花哨的语法（如 async/await），在背后转换成扎实、高效的底层代码，让我们既能写得爽，又能跑得快

如果运行时假设错误（如变量类型变化），会触发 **deoptimization（去优化）**，回退到 Ignition 字节码继续执行。



**SparkPlug：快速编译器（介于 Ignition 与 TurboFan 之间）**

定义：

填补 Ignition 和 TurboFan 之间的性能鸿沟

作用： 

在 **“启动速度”** 和 **“执行速度”** 之间取一个非常好的平衡点。比纯解释执行快，又比等待深度优化编译要快得多。

代码运行起来非常稳定，永远不会因为猜错而退回重新执行。



 **Orinoco：并发垃圾回收器（GC）**

定义：

Orinoco 是 V8 的**新一代垃圾回收系统**，核心目标是**减少主线程停顿（stop-the-world）时间**，提升应用响应性（尤其对动画、游戏、实时应用至关重要）。

作用：

自动内存管理：回收不再使用的对象，防止内存泄漏。

并发 & 并行

- **并发（Concurrent）**：GC 工作与主线程同时进行（不阻塞 JS 执行）。
- **并行（Parallel）**：多个 GC 线程同时工作，加速回收。

支持多种 GC 算法：

- **Scavenger**：用于新生代（Young Generation），快速回收短命对象。
- **Mark-Compact**：用于老生代（Old Generation），处理长存活对象。



### JavaScript 执行过程

（执行上下文）

**后进先出**

```js
var name = "why";

foo(123);

function foo(num) {
  console.log(m); // 这里会报错？为什么？
  var m = 10;
  var n = 20;

  function bar() {
    console.log(name); // 查找 name 变量
  }

  bar();
}
```

关键点：

- `name` 是全局变量。
- `foo` 函数被调用时传入参数 `num = 123`。
- 在 `foo` 内部定义了局部变量 `m`, `n` 和嵌套函数 `bar`。
- `bar()` 调用了 `console.log(name)`，需要查找 `name`。

<img src="./web-img/image-20251028090458155.png" alt="image-20251028090458155" style="zoom:200%;" />

**中间：ECStack（调用栈）**

1. **GEC（全局执行上下文）**

- 包含全局变量对象 `GO`（Variable Object）
- 执行代码：`foo(123)` → 触发函数调用

2. **FEC（函数执行上下文） - foo**

- 当 `foo(123)` 被调用时，创建新的执行上下文并压入栈顶
- 包含：
  - `VO(AO)`：激活对象，存储函数内部变量和参数
  - `scope chain`: `AO + GO`（作用域链）
  - 正在执行：`console.log(name)`（来自 `bar()`）

> 💡 `bar()` 是在 `foo` 内部定义的，所以它的作用域链也继承自 `foo` 的上下文。



**右侧：对象与作用域关系**

**AO** (Activation Object) — `foo` 的激活对象

```js
{
  num: 123,
  m: undefined,  // 因为变量提升，先声明后赋值
  n: undefined,
  bar: 0xb00     // 指向 bar 函数的内存地址
}
```

- 参数 `num` 赋值为 `123`
- 局部变量 `m`, `n` 在声明前为 `undefined`
- `bar` 是一个函数引用

**GlobalObject**

```js
{
  name: "why",
  foo: 0xa00
}
```

- 存储全局变量 `name` 和全局函数 `foo`

**函数存储空间**

- `foo` 存储在内存地址 `0xa00`
- `bar` 存储在内存地址 `0xb00`
- 每个函数都有自己的 `[[scope]]` 链接父级作用域

**作用域链详解**

当 `bar()` 执行 `console.log(name)` 时，JavaScript 引擎如何查找 `name`？

1. 第一步：检查当前作用域（bar 的 AO）
   - `bar` 的 AO 中没有 `name`
2. 第二步：向上查找父级作用域（即 foo 的 AO）
   - `foo` 的 AO 也没有 `name`
3. 第三步：继续向上到全局作用域（GlobalObject）
   - 找到 `name: "why"`

✅ 最终输出：`"why"`



#### JS的执行过程

```
JS 源码
   ↓（解析）
词法分析 → 语法分析 → AST
   ↓
GEC(VO: GO;全局变量和函数声明)
   ↓
CEStack执行栈
   ↓
Ignition 编译 → 字节码 → 执行 + 收集反馈
   ↓（若为热点代码）
TurboFan 优化 → 机器码 → 高速执行
   ↓（若类型变化）
Deoptimization → 回退到字节码
   ↓
变量赋值，函数调用 → FEC(VO:AO ; 函数中的变量和函数声明)
   ↓
运行结束
```

JavaScript 代码先被解析为 AST，再由解释器（如 Ignition）编译成字节码并执行；热点代码会被优化编译器（如 TurboFan）转为高效机器码；若优化假设失败则回退；整个过程由垃圾回收器自动管理内存，并通过宿主环境（如浏览器）实现与外部世界的交互。



GEC（global excution context）全局执行上下文，执行全局代码

FEC（Function Execution Context）函数执行上下文，在调用函数的时候创建的执行环境

VO：每个执行上下文内部用于存储变量和函数声明的抽象容器

GO：全局执行上下文中的 VO，即全局对象（如浏览器中的 `window`）

AO：函数执行上下文中的 VO，用于存放形参、`arguments`、`var` 和函数声明



#### 变量环境

（Variable Environment）

> **ES2015（ES6）引入了更严谨的“词法环境”（Lexical Environment）模型**，将变量的管理分为两个部分：变量环境、环境记录

定义

变量环境是表示当前执行上下文中变量绑定的容器，它是执行上下文的一部分，用于存放通过 `var`、`function`、`let`、`const` 声明的变量。

特点

- 每个执行上下文都有自己的变量环境。
- 它不是直接可访问的对象，而是引擎内部使用的结构。
- 它包含一个指向环境记录（Environment Record）的引用。

#### 环境记录

（Environment Record）

**定义**

环境记录是**实际存储变量名**和**值的数据结构**，它记录了所有在当前作用域中声明的标识符（如变量、函数、参数等）。

**分类**

| 类型                           | 说明                                                         |
| ------------------------------ | ------------------------------------------------------------ |
| Object Environment Record      | 用于全局上下文，变量绑定到全局对象上（如 window）。          |
| Function Environment Record    | 用于函数上下文，包含形参、arguments、函数声明等。            |
| Declarative Environment Record | 用于 let、const、class 等块级作用域变量，不会提升到全局对象，且有“暂时性死区”（TDZ）保护。 |

**变量环境 vs 环境记录的关系**

变量环境是一个“容器”，它指向一个“环境记录”，而环境记录才是真正存储变量绑定的地方。

```
执行上下文
│
├── 变量环境（Variable Environment）
│   └── → 环境记录（Environment Record）
│       ├── 标识符：a, b, c, d ...
│       └── 值：1, 2, 3, 4 ...
│
└── 词法环境（Lexical Environment） ← 用于作用域链查找
```

**与旧概念的对应关系**

| 旧术语                  | 新术语                                      | 说明                                 |
| ----------------------- | ------------------------------------------- | ------------------------------------ |
| VO（Variable Object）   | Variable Environment + Environment Record   | 被拆分成了两个更清晰的部分           |
| GO（Global Object）     | Object Environment Record                   | 全局变量绑定到全局对象（如 window）  |
| AO（Activation Object） | Function Environment Record                 | 函数内的变量和参数存储在这里         |
| var 声明                | → 存入 Object / Function Environment Record | 会被提升，且挂到全局对象或函数上下文 |
| let/const 声明          | → 存入 Declarative Environment Record       | 不提升，有 TDZ，不会污染全局         |

**这个变化的重要性**

- 支持块级作用域：`let` 和 `const` 不再被提升到全局对象，避免污染。
- 支持暂时性死区（TDZ）：在声明前访问 `let/const` 会报错，提高安全性。
- 更清晰的作用域模型：区分了“变量绑定”和“作用域链”的不同层次。



```
执行上下文
│
├── 变量环境（Variable Environment）
│   └──→ 环境记录（Environment Record）
│       ├── Object Environment Record (全局)
│       ├── Function Environment Record (函数)
│       └── Declarative Environment Record (块级)
│
└── 词法环境（Lexical Environment）
    └──→ 父级词法环境（Parent Lexical Environment）
        └──→ ... (直到全局环境)
```





###  认识内存管理

定义：不管什么样的编程语言，在代码的执行过程中都是需要给他分配内存的，不同的是某些编程语言需要我们自己手动的管理内存，某些变成语言会可以自动帮助我们管理内存

**内存的生命周期**

不管什么程序语言，内存生命周期基本是一致的：

1. 分配你所需要的内存
2. 使用分配到的内存（读、写）
3. 不需要时将其释放

在所有语言中，第二点都是显式的。在底层语言中，第一点和第三点是显式的，但在高级语言中（如 JavaScript），大多数是隐式的。

**内存管理的两种模式对比**：

| 类型             | 代表语言                                 | 特点                                                         | 示例                                     |
| ---------------- | ---------------------------------------- | ------------------------------------------------------------ | ---------------------------------------- |
| **手动管理内存** | C、C++、早期 Objective-C                 | 需开发者显式申请和释放内存，使用如 `malloc` 和 `free` 等函数 | `malloc()` 分配，`free()` 释放           |
| **自动管理内存** | Java、JavaScript、Python、Swift、Dart 等 | 由运行时环境（如垃圾回收机制 GC）自动处理内存分配与释放      | 开发者无需手动释放，系统自动回收无用对象 |



### JS内存管理



#### 内存分配的基本概念

JavaScript 在定义变量时会自动为我们分配内存，但根据数据类型的不同，内存的分配方式也会有所不同。

#### JavaScript 数据类型与内存分配

##### **基本数据类型**（`string`、`number`、`boolean` 等）

**存储位置**：栈（Stack）

**特点**：值直接存于栈中

示例

```js
let name = "why";   // "why" 直接存栈
let age = 18;       // 18 直接存栈
```

##### **复杂数据类型**（对象、数组、函数等）

存储位置

- 实际数据 → 堆（Heap）
- 变量（引用）→ 栈中存指向堆的指针

**特点**：栈存引用，堆存内容

示例

```js
let obj = {name: "kobe", age: 40};   // 对象内容在堆，obj 在栈中存引用
let names = ["abc", "cba"];          // 数组内容在堆，names 在栈中存引用
```

 

### JS的垃圾回收

##### GC是什么？

`GC` 即 `Garbage Collection` ，程序工作过程中会产生很多 `垃圾`，这些垃圾是程序不用的内存或者是之前用过了，以后不会再用的内存空间，而 `GC` 就是负责回收垃圾的。

因为他工作在引擎内部，所以对于我们前端来说，`GC` 过程是相对比较无感的，这一套引擎执行而对我们又相对无感的操作也就是常说的 `垃圾回收机制` 了

当然也不是所有语言都有 `GC`，一般的高级语言里面会自带 `GC`，比如 `Java、Python、JavaScript` 等，也有无 `GC` 的语言，比如 `C、C++` 等，那这种就需要我们程序员手动管理内存了，相对比较麻烦



##### 为什么需要内存回收？

- 创建变量、对象、函数等都会占用内存。
- JavaScript 引擎自动分配内存，**我们不用手动管理**。
- 但当某些数据**不再被使用**时，如果不清理，内存会越占越多 → **内存泄漏** → 程序变慢甚至崩溃。

```js
let test = { name: "isboyjc" };  // test 引用一个对象（堆中）
test = [1, 2, 3, 4, 5];         // test 现在引用一个数组
```

> 原来的 `{ name: "isboyjc" }` **不再被任何变量引用**。
>
> 它变成“无用对象”，但还占着堆内存。



##### JavaScript 怎么清理无用对象？

- 使用 **垃圾回收机制（Garbage Collection, GC）**。

- 核心思想：**自动找出不再被引用的对象，释放其内存**。

- 最常用策略：

  可达性分析（Mark-and-Sweep）

  - 从“根对象”（如全局变量）出发，追踪所有能访问到的对象。
  - **无法到达的对象 = 垃圾 → 被回收**



##### 垃圾回收

- JavaScript **自动管理内存**，不需要手动释放。
- 当变量/对象 **不再被使用（不可达）**，引擎会自动回收其占用的内存。



##### 垃圾回收算法

######  **标记清除算法**（Mark-Sweep）✅ **主流方案**

定义：**通过两个主要阶段来回收内存：标记阶段，它从根对象（如全局对象、文档DOM树等）开始遍历，标记所有可达的对象；清除阶段，它会删除所有未被标记的对象，释放其内存空间**

标记阶段

1. **初始化标记**：垃圾回收器首先假设内存中的所有对象都是垃圾，并为它们打上“未标记”的标记（例如，在对象的某个二进制位上标记为“0”）。
2. **从根对象开始遍历**：从一组根对象（如全局 `window` 对象、文档DOM树等）开始，垃圾回收器会深度优先地遍历所有可达的对象。
3. **标记可达对象**：在遍历过程中，每访问到一个对象，就会将其标记为“可达”（例如，将标记改为“1”），表示这个对象是活动的，不会被回收。
4. **遍历引用的所有对象**：它会继续遍历被标记对象的引用，并将所有通过这些引用能够访问到的对象都标记为“可达”，以确保所有活动的引用链条上的对象都被标记。 

清除阶段

1. **回收未标记对象**：在标记阶段结束后，垃圾回收器会遍历整个内存空间。所有仍处于“未标记”状态的对象都被视为是不可达的垃圾。
2. **释放内存**：这些未被标记的对象所占用的内存空间将被回收并释放。
3. **重置标记**：最后，所有对象都会被重新标记为“未标记”（或“垃圾”），为下一轮的垃圾回收做准备。 

算法优点与缺点

- **优点**：
  - **处理循环引用**：它能有效地处理循环引用的情况，这是引用计数算法的一个主要缺点。
  - **简单易实现**：算法本身相对简单。
- **缺点**：
  - **性能影响**：在执行时可能会产生一个较长的“停止一切”（stop-the-world）暂停，对程序性能造成影响。
  - **现代引擎的优化**：现代JavaScript引擎通常会使用增量标记-整理算法等优化技术来缓解标记清除算法的暂停问题。 





### 闭包

#### 定义

1. 在计算机科学里
   - **闭包**（英语：Closure），又称**词法闭包**（Lexical Closure）或**函数闭包**（function closures）；
   - 是在支持**头等函数**的编程语言中，实现**词法绑定**的一种技术；
   - 闭包在实现上是一个结构体，它存储了一个函数和一个关联的环境（相当于一个符号查找表）；
   - 闭包跟函数最大的区别在于，当捕捉闭包的时候，**它的自由变量会在补充时被确定，这样即使脱离了捕捉时的上下文，它也能照常运行。**

2.  对 JavaScript 闭包的解释：
   - **一个函数**和对其**周围状态**（lexical environment，词法环境）的引用**捆绑在一起**（或者说函数被引用包围），这样的组合就是**闭包**（closure）；
   - 也就是说，闭包让你可以在一个内层函数中访问到其外层函数的作用域；
   - 在 JavaScript 中，**每当创建一个函数，闭包就会在函数创建的同时被创建出来。**

 

```js
function foo(){
	function bar(){
		console.log("bar")
	}
	return bar
}
var fn = foo() 
fn() 
```

理解闭包：

其实可以用一句话说明闭包：JS中一个函数，可以访问外层作用域的变量，那么他就是一个闭包

- 一个普通的函数 function，如果它可以**访问外层作用域**的自由**变量**，那么这个函数就是一个闭包；
- 从广义的角度来说：JavaScript 中的函数都是闭包；
- 从狭义的角度来说：JavaScript 中一个函数，如果**访问了外层作用域**的**变量**，那么它是一个闭包。



#### 闭包的表现形式

##### 返回一个函数

当一个函数内部定义了另一个函数，并将这个内部函数作为返回值返回时，就形成了一个闭包。返回的这个函数可以访问外部函数中的变量，即使外部函数已经执行完毕并且其内部变量已经被销毁。

```js
function outer() {
  var count = 0;
  function inner() {
    count++;
    console.log(count);
  }
  return inner;
}
var closure = outer();
closure(); // 输出1
closure(); // 输出2
closure(); // 输出3

```

在这个例子中，函数 outer 内部定义了一个函数 inner，并将其返回。变量 count 也定义在 outer 函数内部。
执行 outer 函数会返回函数 inner，将其赋值给变量 closure。
然后调用 closure 函数，由于 closure 函数是由 outer 函数返回的 inner 函数，所以它可以访问 outer 函数内部的变量 count。因此每次调用 closure 函数都会输出一个累加的数值。

##### 定义一个函数

在 JavaScript 中，通过定义一个函数并在该函数内部定义另一个函数，也可以形成一个闭包。这时需要将内部函数作为返回值返回，以便在外部调用。

```js
function makeCounter() {
  var count = 0;
  function counter() {
    count++;
    console.log(count);
  }
  return counter;
}
var closure = makeCounter();
closure(); // 输出1
closure(); // 输出2
closure(); // 输出3

```

在这个例子中，函数 makeCounter 内部定义了函数 counter，并将其返回。变量 count 也定义在 makeCounter 函数内部。
执行 makeCounter 函数会返回函数 counter，将其赋值给变量 closure。
然后调用 closure 函数，由于 closure 函数是由 makeCounter 函数返回的 counter 函数，所以它可以访问 makeCounter 函数内部的变量 count。因此每次调用 closure 函数都会输出一个累加的数值。



#### 闭包的内存泄漏 

#####  闭包的缺点

大量使用闭包，造成内存占用空间增大，有内存泄露的风险

##### 如何避免闭包引起的内存泄漏

1. 在退出函数之前，将不使用的局部变量**赋值为null**;

```js
 这段代码会导致内存泄露
    window.onload = function(){
        var el = document.getElementById("id");
        el.onclick = function(){
            alert(el.id);
        }
    }
    解决方法为
    window.onload = function(){
        var el = document.getElementById("id");
        var id = el.id;                                      //解除循环引用
        el.onclick = function(){
            alert(id); 
        }
        el = null;                                          // 将闭包引用的外部函数中活动对象清除
    }

```

2. 避免变量的循环赋值和引用。 （示例如上）

循环引用引起的内存泄漏，是因为IE 的bug，循环引用无法自动判断，所以通过拷贝值，把内外引用脱钩，这样就可回收。IE9及其以后已修复。

3. 利用Jquery释放自身指定的所有事件处理程序。

**由于jQuery考虑到了内存泄漏的潜在危害，所以它会手动释放自己指定的所有事件处理程序。** 只要坚持使用jQuery的事件绑定方法，就可以一定程度上避免这种特定的常见原因导致的内存泄漏。

```js
这段代码会导致内存泄露
$(document).ready(function() {
    var button = document.getElementById('button-1');
    button.onclick = function() {
         console.log('hello');
         return false;
    };
});
当指定单击事件处理程序时，就创建了一个在其封闭的环境中包含button变量的闭包。而且，现在的button也包含一个指向闭包（onclick属性自身）的引用。这样，就导致了在IE中即使离开当前页面也不会释放这个循环。

用jQuery化解引用循环
$(document).ready(function() {
    var $button = $('#button-1');
    $button.click(function(event) {
        event.preventDefault();
        console.log('hello');
    });
});

```



##### js闭包引用的自由变量销毁

```js
function foo(){
	var name = 'why'
	var age = 18
	
	function bar(){
		debugger
		console.log(name)
		console.log(age)
	}
	return bar
}
var fn = foo()
fn()
```

**AO对象不会被销毁时，并非里面所有的属性都不会被销毁。**

name和age都是闭包的父级[作用域](https://so.csdn.net/so/search?q=作用域&spm=1001.2101.3001.7020)里的变量，形成闭包后，name一定不会被销毁，但age会被销毁（js v8引擎为了性能，会销毁不使用的属性）



#### 闭包常见应用场景

##### 柯里化函数

为了避免频繁地调用具有相同参数的函数，可以将一个多参数的函数转化为一个单参数的函数，
其实就是一个高阶函数

```js
//普通函数
function getArea(w,h){
    return w * h;
}
const area1 = getArea(10,20);
const area2 = getArea(10,30);
const area3 = getArea(10,40);

//柯里化函数
function getArea(w){
    return function(h){
        return w * h;
    }
}
const getTenArea = getArea(10);

const area1 = getTenArea(20);
const area2 = getTenArea(30);
const area3 = getTenArea(40);
```

##### 通过闭包实现变量/方法的私有化

```js
function funOne(i){
    function getTwo(){
        console.log('参数：', i)
    }
    return getTwo;
}
const fa = funOne(100); 
const fb = funOne(200); 
const fc = funOne(300); 
```

##### 匿名执行函数

```js
var funOne = (function(){
    var num = 0;
    return function(){
        num++;
        return num;
    }
})()

console.log(funOne());   // 1
console.log(funOne());   // 2
console.log(funOne());   // 3 


```

##### 缓存一些结果

比如：外部函数定义一个变量，内部函数可以获取或修改这个变量的值，从而就延长了这个变量的生命周期

```js
function parent(){
    let list = [];
    function son(i){
        list.push(i);
    }
    return son;
}

const fn = parent();

fn(1);
fn(2);
fn(3);


```





###  JS函数的this指向

#### JS函数中this的指向

JS函数的 `this` 指向取决于函数是如何被调用的，而不是定义时。在**对象方法**中，`this` 指向调用该方法的对象；在**普通函数**调用中，`this` 指向全局对象（非严格模式下是 `window`）；在**箭头函数**中，`this` 继承自其外层作用域。此外，`apply()`、`call()` 和 `bind()` 方法可以显式地改变函数的 `this` 指向。 

```js
// 从某些角度来说，开发中如果没有this，很多的问题我们也是有解决方案
// 但是没有this，会让我们编写代码变得非常的不方便

var obj100 = {
    name: "why",
    eating: function() {
        console.log(this.name + "在吃东西")
    },
    running: function() {
        console.log(this.name + "在跑步")
    },
    studying: function() {
        console.log(this.name + "在学习")
    }
}

var info = {
    name: "why",
    eating: function() {
        console.log(this.name + "在吃东西")
    },
    running: function() {
        console.log(this.name + "在跑步")
    },
    studying: function() {
        console.log(this.name + "在学习")
    }
}
```



1. 方法调用模式下，this 总是指向调用它所在方法的对象，this 的指向与所在方法的调用位置有关，而与方法的声明位置无关（箭头函数特殊）；

2. 函数调用下，this 指向 window ,调用方法没有明确对象的时候，this 指向 window，如 setTimeout、匿名函数等；

3. 构造函数调用模式下，this 指向被构造的对象；

4. apply,call,bind 调用模式下，this 指向第一个参数；

5. 箭头函数，在声明的时候绑定this，而非取决于调用位置；

6. 严格模式下，如果 this 没有被执行环境（execution context）定义，那 this是 为undefined；





#### 绑定规则

##### 默认绑定

- **规则：** 函数被独立调用时，`this`指向全局对象。在严格模式下，`this`会绑定到`undefined`。

- **场景：** 单独调用一个函数，例如

  ```js
   function greet() { 
       console.log(this); 
   } greet();
  ```

##### 隐式绑定

- **规则：** 当函数被作为对象的方法调用时，`this`指向该对象。

- **场景：** 调用一个对象的方法，例如

  ```js
   let obj = { 
   	name: 'Alice', 
       sayHello: function() { 
           console.log(this.name); 
       } 
   }; 
  obj.sayHello();
  ```

##### 显示绑定

- **规则：** 使用 [call()](https://www.google.com/search?q=call()&sca_esv=f5b5a348d766e74b&authuser=0&biw=1536&bih=730&sxsrf=AE3TifMO1n1XXignLWznGiXe9HN7RxqS6A%3A1761792109887&ei=bdACadj0NYCq5NoPgsHLKA&ved=2ahUKEwjqwIrC9MqQAxXTsVYBHZqrI7EQgK4QegQIBxAB&uact=5&oq=this的绑定规则&gs_lp=Egxnd3Mtd2l6LXNlcnAiE3RoaXPnmoTnu5Hlrprop4TliJkyCBAAGIkFGKIEMgUQABjvBTIFEAAY7wUyBRAAGO8FMgUQABjvBUjdQFCbCFiIPXACeACQAQGYAYECoAGiKqoBBjAuMjMuNrgBA8gBAPgBAZgCFqAC7ByoAgrCAgoQABhHGNYEGLADwgIEECMYJ8ICBRAAGIAEwgIKEAAYgAQYigUYQ8ICBxAjGOoCGCfCAgcQLhjqAhgnwgIIEAAYgAQYsQPCAhEQLhiABBixAxiDARjHARjRA8ICCxAAGIAEGLEDGIMBwgIOEC4YgAQYigUYsQMYgwHCAg4QABiABBiKBRixAxiDAcICCxAuGIAEGMcBGNEDwgIFEC4YgATCAggQABiABBjLAcICChAAGIAEGMsBGArCAgoQLhiABBjLARgKwgIIEAAYgAQYogSYAwSIBgGQBgqSBwYyLjE2LjSgB-tfsgcGMC4xNi40uAfiHMIHBjEuMTUuNsgHLg&sclient=gws-wiz-serp&mstk=AUtExfDktaeqTmupKCKV_jMau-gjinuFl59toy7A2tvMhIZ2WkwtBDhiNs7cmHLTCI6YK7ZF4IGw7rHOZwtn8rjf03HETGjTTktZcWEOfqbPXHbjjk4SLSKgfhy3SMxhfnIZRbwrPGjBvmp3VHjW-b4PNOREbTDJwA2RegYMVndslW5KnEed6dj9E144JhcXm6PesyVi8bkrTFwxa_0kbyJsWo32wEFdUkJQ5N6SgXUJ7p6xMpkjM91UHzxyeYHG9pp4ydHnF5vjlVRQVvXGxMGU_9zVIgnZXt1tBtUYHJ6gMFjL0Q&csui=3)、[apply()](https://www.google.com/search?q=apply()&sca_esv=f5b5a348d766e74b&authuser=0&biw=1536&bih=730&sxsrf=AE3TifMO1n1XXignLWznGiXe9HN7RxqS6A%3A1761792109887&ei=bdACadj0NYCq5NoPgsHLKA&ved=2ahUKEwjqwIrC9MqQAxXTsVYBHZqrI7EQgK4QegQIBxAC&uact=5&oq=this的绑定规则&gs_lp=Egxnd3Mtd2l6LXNlcnAiE3RoaXPnmoTnu5Hlrprop4TliJkyCBAAGIkFGKIEMgUQABjvBTIFEAAY7wUyBRAAGO8FMgUQABjvBUjdQFCbCFiIPXACeACQAQGYAYECoAGiKqoBBjAuMjMuNrgBA8gBAPgBAZgCFqAC7ByoAgrCAgoQABhHGNYEGLADwgIEECMYJ8ICBRAAGIAEwgIKEAAYgAQYigUYQ8ICBxAjGOoCGCfCAgcQLhjqAhgnwgIIEAAYgAQYsQPCAhEQLhiABBixAxiDARjHARjRA8ICCxAAGIAEGLEDGIMBwgIOEC4YgAQYigUYsQMYgwHCAg4QABiABBiKBRixAxiDAcICCxAuGIAEGMcBGNEDwgIFEC4YgATCAggQABiABBjLAcICChAAGIAEGMsBGArCAgoQLhiABBjLARgKwgIIEAAYgAQYogSYAwSIBgGQBgqSBwYyLjE2LjSgB-tfsgcGMC4xNi40uAfiHMIHBjEuMTUuNsgHLg&sclient=gws-wiz-serp&mstk=AUtExfDktaeqTmupKCKV_jMau-gjinuFl59toy7A2tvMhIZ2WkwtBDhiNs7cmHLTCI6YK7ZF4IGw7rHOZwtn8rjf03HETGjTTktZcWEOfqbPXHbjjk4SLSKgfhy3SMxhfnIZRbwrPGjBvmp3VHjW-b4PNOREbTDJwA2RegYMVndslW5KnEed6dj9E144JhcXm6PesyVi8bkrTFwxa_0kbyJsWo32wEFdUkJQ5N6SgXUJ7p6xMpkjM91UHzxyeYHG9pp4ydHnF5vjlVRQVvXGxMGU_9zVIgnZXt1tBtUYHJ6gMFjL0Q&csui=3) 或 [bind()](https://www.google.com/search?q=bind()&sca_esv=f5b5a348d766e74b&authuser=0&biw=1536&bih=730&sxsrf=AE3TifMO1n1XXignLWznGiXe9HN7RxqS6A%3A1761792109887&ei=bdACadj0NYCq5NoPgsHLKA&ved=2ahUKEwjqwIrC9MqQAxXTsVYBHZqrI7EQgK4QegQIBxAD&uact=5&oq=this的绑定规则&gs_lp=Egxnd3Mtd2l6LXNlcnAiE3RoaXPnmoTnu5Hlrprop4TliJkyCBAAGIkFGKIEMgUQABjvBTIFEAAY7wUyBRAAGO8FMgUQABjvBUjdQFCbCFiIPXACeACQAQGYAYECoAGiKqoBBjAuMjMuNrgBA8gBAPgBAZgCFqAC7ByoAgrCAgoQABhHGNYEGLADwgIEECMYJ8ICBRAAGIAEwgIKEAAYgAQYigUYQ8ICBxAjGOoCGCfCAgcQLhjqAhgnwgIIEAAYgAQYsQPCAhEQLhiABBixAxiDARjHARjRA8ICCxAAGIAEGLEDGIMBwgIOEC4YgAQYigUYsQMYgwHCAg4QABiABBiKBRixAxiDAcICCxAuGIAEGMcBGNEDwgIFEC4YgATCAggQABiABBjLAcICChAAGIAEGMsBGArCAgoQLhiABBjLARgKwgIIEAAYgAQYogSYAwSIBgGQBgqSBwYyLjE2LjSgB-tfsgcGMC4xNi40uAfiHMIHBjEuMTUuNsgHLg&sclient=gws-wiz-serp&mstk=AUtExfDktaeqTmupKCKV_jMau-gjinuFl59toy7A2tvMhIZ2WkwtBDhiNs7cmHLTCI6YK7ZF4IGw7rHOZwtn8rjf03HETGjTTktZcWEOfqbPXHbjjk4SLSKgfhy3SMxhfnIZRbwrPGjBvmp3VHjW-b4PNOREbTDJwA2RegYMVndslW5KnEed6dj9E144JhcXm6PesyVi8bkrTFwxa_0kbyJsWo32wEFdUkJQ5N6SgXUJ7p6xMpkjM91UHzxyeYHG9pp4ydHnF5vjlVRQVvXGxMGU_9zVIgnZXt1tBtUYHJ6gMFjL0Q&csui=3) 方法**明确**指定函数中的`this`指向。

- **场景**

  ```js
  function greet() { 
      console.log(this); 
  } 
  greet.call({ 
      name: 'Bob' 
  });
  ```

##### `new`绑定

- **规则：** 当使用 `new` 操作符调用函数时，会创建一个新对象，并且函数内部的`this`被绑定到这个新对象上。

- **场景：** 使用 `new` 创建一个对象实例，例如

  ```js
  function Person(name) { 
      this.name = name; 
  } 
  let person = new Person('Charlie');
  ```

```js
var obj = {
    name: "obj",
    foo: function() {
        console.log(this)
    }
}

var f = new obj.foo()
console.log(f) // 输出新创建的对象实例
```

理解：new就是在堆中创建了一个对象，然后将构造函数中的this指向了这个对象并且在对象中添加了对象原型指回构造函数的原型对象，并且继承来constructor属性指回构造函数，之后调用构造函数，相当于我们手动使用对象名.属性名 = 属性值这样，巧妙地利用了new会修改this的指向，使用 new创建的对象.属性名 = 属性值，new创建的对象.方法名 = 函数 这样来为实例化的对象创建和构造函数一样解构的属性名和属性值，然后再将new创建的对象的地址赋给引用数据类型的变量，如果我new一次后打印构造函数的this值，那指向的应该是刚刚创建的对象



##### 箭头函数绑定

- **规则：** 箭头函数不绑定自己的`this`，它会捕获其所在作用域的`this`值。

-  **场景：** 在普通函数中使用箭头函数，箭头函数的`this`与外部普通函数相同，例如

  ```js
  function Outer() { 
      this.name = 'Outer'; 
      setTimeout(() => { 
          console.log(this.name); 
      }, 1000); 
  } 
  new Outer();
  ```

  

####  规则优先级

优先级从高到低是：new绑定 > 显示绑定 > 隐式绑定 > 默认绑定

当多种绑定规则同时存在时，优先级高的规则会覆盖优先级低的规则

优先级规则

- **最高优先级：`new` 绑定**
  - 当使用 `new` 关键字调用函数时，`this` 会指向新创建的对象，这是最高优先级的规则。
- **次高优先级：显式绑定**
  - 通过 `call()`、`apply()` 和 `bind()` 方法手动指定 `this` 的值，优先级高于隐式绑定和默认绑定。
  - `new` 绑定不能与 `call` 和 `apply` 同时使用，而 `new` 绑定可以与 `bind` 结合使用，但 `new` 绑定优先级更高，它会忽略掉 `bind` 的绑定。
- **中间优先级：隐式绑定**
  - 当函数作为对象的方法调用时（例如 `obj.foo()`），`this` 会指向该对象 `obj`。
- **最低优先级：默认绑定**
  - 当函数作为普通函数独立调用时（例如 `foo()`），`this` 默认指向全局对象（浏览器中的 `window` 对象，或在严格模式下是 `undefined`）。 



#### 特殊绑定

##### 箭头函数 

箭头函数不会绑定this、arguments属性；箭头函数不能作为**构造函数**来始用

由三部分组成：1. （）：参数 ； 2.  => 箭头  ； 3.  {} ：函数的执行体

> 高阶函数在使用时，可以传入箭头函数

```js
var num = [10,20,30,40,50]
nums.forEach((item,index,arr) => {})
```

箭头函数有一些常见的简写

1. 如果参数只有一个，（）可以省略

```js
nums.forEach(item => {
	console.log(item)
})
```

2. 如果函数执行体只有一行代码，那么{}可以省略

```js
nums.forEach(item => console.log(item))
```

3. 如果一个箭头函数，只有一行代码，并且返回一个对象，这个时候如何编写简写

```js
var bar = () => {
    return {name:"why",age:19}
}

// 简写,箭头右边加小括号，是把小括号内部的内容当成一个整体
var bar = () => ({name:"why",age:19})
```



##### 忽略显示绑定

如果在显示绑定中，我们传入一个null或者undefined，那么这个显示绑定会被忽略，使用默认规则

```js
    <script>
        function fn() {
            console.log(this);
        }
        fn.apply({name:'wc'}) //{name:'wc'}

        fn.apply(null);//window
        fn.apply(undefined);//window
        var gn = fn.bind(null);
        gn();//window
    </script>

```



##### 间接函数引用

 间接调用是通过函数引用、apply、call 等方式调用其他方法

```js
    <script>
        var obj = {
            name:'wc',
            fn:function(){
                console.log(this);
            }
        }
        var obj2 = {
            name:'xq'
        };
        ;(obj2.gn = obj.fn)();//obj2.gn();
        ;(function(){console.log(this);}())
    </script>

```



####  实现 `apply`,`call`,`bind`

 在JavaScript中，`call`,`apply`和`bind`是三种非常重要的函数方法，它们都可以用来改变函数执行时*this*的指向。这些方法在实际开发中非常有用，尤其是在处理对象和函数时。

##### call方法

`call`方法允许在特定上下文中调用一个函数。它的语法是`function.call(context,arg1,arg2,...)`,其中`cntext`是`this`要指向的对象`arg1`, `arg2`, ...是传递给函数的参数。例如，如果你有一个对象`obj`和一个方法`greeting`，你可以这样使用`call`方法：

```js
const obj = {
 name: 'Alice',
 greeting: function() {
   console.log(`Hello, my name is ${this.name}`);
 }
};
const person = {
 name: 'Bob'
};
obj.greeting.call(person); // 输出 "Hello, my name is Bob"
```

在这个例子中，`greeting`方法原本是`obj`对象的一部分，但是通过使用`call`方法，我们可以让这个方法在`person`对象的上下文中执行



##### apply方法

`apply`方法和`call`方法非常相似，但是他接受参数数组。它的语法是：`function.apply(context,[argsArray])`

这里的`context`同样是this的指向，而`argsArray`是一个参数数组。如果你有一个接受多个参数的函数，可以使用`apply`方法

```js
const obj = {
 name: 'Alice',
 greeting: function(city, country) {
   console.log(`Hello, my name is ${this.name} and I am from ${city}, ${country}`);
 }
};
obj.greeting.apply(person, ['London', 'UK']); // 输出 "Hello, my name is Bob and I am from London, UK"
```



##### bind方法

`bind`方法与`call`和`apply`不同，它不会立即执行函数，而是返回一个新的函数，当这个新函数被调用时，原函数会在指定的上下文中执行。它的语法是`function.bind(thisArg, arg1, arg2, ...)`, 其中`thisArg`是this的指向，`arg1`,` arg2`, ...是传递给函数的参数。例如：

```js
const boundGreeting = obj.greeting.bind(person, 'London');
boundGreeting('UK'); // 输出 "Hello, my name is Bob and I am from London, UK"
```

在这个例子中，我们使用`bind`方法创建一个新的函数`boundGreeting`，他将`greeting`方法绑定到`person`对象上，并预设了一个参数`'London'`。当我们调用`bound Greeting('UK')`时，他会以`person`对象为上下文执行



### `arguments`

#### 认识`arguments`

`arguments`是一个对应于**传递给函数的参数**的**类数组（array-like）对象**

`array-like`意味着他不是一个数组类型，而是一个对象类型：

* 但是它却拥有数组的一些特性，比如说length，比如可以通过index索引来访问
* 但是它却没有数组的一些方法，比如forEach、map等

```js
function foo(num1,num2,num3){
    console.log(arguments)
    console.log(num1,num2,num3)
}
foo(10,20,30,40,50)
```

根据上面的案例，常见的对arguments的操作有三个：

1. 获取参数的长度

```js
console.log(arguments.length)
```

2. 根据索引值获取某一个参数

```js
console.log(arguments[2])
console.log(arguments[3])
console.log(arguments[4])
```

3. 

```js
console.log(arguments.callee)
```



#### `arguments`转数组

```js
function foo(num1,num2){
    var newArr = []
    for(var i = 0 ; i < arguments.length ; i++){
        newArr.push
    }
    console.log(newArr) 
}
foo(10,20,30,40,50)
```



```js
// 2. arguments转成array类型

// 2.1. 自己遍历arguments中所有的元素

// 2.2. Array.prototype.slice将arguments转换为数组
var newArr2 = Array.prototype.slice.call(arguments);
console.log(newArr2);

var newArr3 = [].slice.call(arguments);
console.log(newArr3);

// 2.3. 展开运算符转换为数组
var newArr4 = Array.from(arguments);
console,log(newArr4)
var newArr5 = [...arguments]
console.log(newArr5)
```



#### 箭头函数中没有`arguments`

```js
function fn (){
    var bar = () =>{
        console.log(arguments)
    }
    return bar
}
var foo = fn(123)
foo()
```

剩余参数

```js
var foo = (num1,num2,...args) =>{
    console.log(args)    //  [30, 40, 50]
}
foo(10,20,30,40,50)

```





### JS函数式编程

#### 纯函数

函数式编程中有一个非常重要的概念叫纯函数，js符合函数式编程的范式，所以也有纯函数的概念

在`react`中组件就被要求像是一个纯函数（为什么像，因为还有class组件），`redux`中有一个`reducer`的概念，也是要求必须是一个纯函数

![image-20251101092640428](./web-img/image-20251101092640428.png)

定义：

在程序设计中，一个函数被称为**纯函数**，需满足以下三个条件：

1. **确定性输出**：对于相同的输入值，总是产生相同的输出。
2. **无外部依赖**：函数的输出不依赖于输入值以外的隐藏信息、状态或I/O设备的外部输出。
3. **无副作用**：函数不能产生可观察的**副作用**，例如触发事件、修改外部数据、输出到设备等。

**简要总结**：
 纯函数是**只依赖输入、输出可预测、无副作用**的函数，具有高度可测试性和可复用性，常用于函数式编程。



（拓展）副作用：在计算机中，也引用了副作用的概念，表示在执行一个函数时，除了**返回函数值**之外，还对调用函数产生了附加的影响，比如**修改了全局变量**，**修改参数**或**改变外部的存储**

纯函数在执行过程中就是不能产生这样的副作用：副作用往往是产生bug的“温床”



纯函数的案例：

`slice`：`slice`截取数组时不会任何数组进行任何操作，而是生成一个新的数组

`splice`：`splice`截取数组，会返回一个新的数组，也会对原数组进行修改

splice就是一个纯函数，不会修改传入的参数

```js
  var names = ["abc","bhu","hui","ooi"]
// slice只要给他传入一个start/end，那么对于同一个数组来说，他会给我们返回确定的值
// slice函数本身他是不会修改原来的数组的
// slice ->this
// slice函数本身就是一个纯函数
// var newName1 = names.slice(0,3)
// console.log(newNames)
// console.log(names)

//  ["abc","bhu","hui","ooi"]
// solice在执行时，有修改调用的数组对象本身额，修改的这个操作就是产生的副作用
// splice不是一个纯函数
var newName2 = names.splice(2)
console.log(newName2)    // ['hui', 'ooi']
console.log(names)       // ['abc', 'bhu']

```



纯函数的优势：

- 相同输入始终返回相同输出，行为可预测；
- 不依赖也不修改外部状态，无副作用；
- 易于测试、并行执行和缓存，提升代码质量与开发效率。





### JS柯里化

#### 定义

柯里化是一种函数的转换，它是指将一个函数从可调用的`f(a,b,c)`转换为可调用的`f(a)(b)(c)`。柯里化不会调用函数，他只是**对函数进行转换**。

例子：

我们将创建一个辅助函数 `curry(f)`，该函数将对两个参数的函数 `f` 执行柯里化。换句话说，对于两个参数的函数 `f(a, b)` 执行 `curry(f)` 会将其转换为以 `f(a)(b)` 形式运行的函数：

```js
function curry(f) { // curry(f) 执行柯里化转换
  return function(a) {
    return function(b) {
      return f(a, b);
    };
  };
}

// 用法
function sum(a, b) {
  return a + b;
}

let curriedSum = curry(sum);

alert( curriedSum(1)(2) ); // 3
```

正如你所看到的，实现非常简单：只有两个包装器（wrapper）。

- `curry(func)` 的结果就是一个包装器 `function(a)`。
- 当它被像 `curriedSum(1)` 这样调用时，它的参数会被保存在词法环境中，然后返回一个新的包装器 `function(b)`。
- 然后这个包装器被以 `2` 为参数调用，并且，它将该调用传递给原始的 `sum` 函数。



#### 理解

举例来说，一个接收3个参数的普通函数，在进行柯里化后， 柯里化版本的函数接收一个参数并返回接收下一个参数的函数， 该函数返回一个接收第三个参数的函数。 最后一个函数在接收第三个参数后， 将之前接收到的三个参数应用于原普通函数中，并返回最终结果。

```js
// 数学和计算科学中的柯里化：

//一个接收三个参数的普通函数
function sum(a,b,c) {
    console.log(a+b+c)
}

//用于将普通函数转化为柯里化版本的工具函数
function curry(fn) {
  //...内部实现省略，返回一个新函数
}

//获取一个柯里化后的函数
let _sum = curry(sum);

//返回一个接收第二个参数的函数
let A = _sum(1);
//返回一个接收第三个参数的函数
let B = A(2);
//接收到最后一个参数，将之前所有的参数应用到原函数中，并运行
B(3)    // print : 6
```



我们Javascript实际应用中的柯里化函数，可以传递一个或多个参数

```js
//普通函数
function fn(a,b,c,d,e) {
  console.log(a,b,c,d,e)
}
//生成的柯里化函数
let _fn = curry(fn);

_fn(1,2,3,4,5);     // print: 1,2,3,4,5
_fn(1)(2)(3,4,5);   // print: 1,2,3,4,5
_fn(1,2)(3,4)(5);   // print: 1,2,3,4,5
_fn(1)(2)(3)(4)(5); // print: 1,2,3,4,5
```

对于已经柯里化后的 _fn 函数来说，当接收的参数数量与原函数的形参数量相同时，执行原函数； 当接收的参数数量小于原函数的形参数量时，返回一个函数用于接收剩余的参数，直至接收的参数数量与形参数量一致，执行原函数。



#### 作用

让一个函数处理的问题尽可能单一，而不是将一大堆的处理过程交给一个函数来处理

柯里化实际是把简单的问题复杂化，但是在复杂的同时，在使用函数时拥有了更加多的自由度。柯里化本质上是降低通用性，提高适用性

```js
// 假如在程序中,我们经常需要把5和另外一个数字进行相加
// console.log(sum(5, 10))
// console.log(sum(5, 14))
// console.log(sum(5, 1100))
// console.log(sum(5, 555))

function makeAdder(count) {
    return function(num) {
        return count + num
    }
}

// 修正调用方式：应该用圆括号()而不是方括号[]
var result = makeAdder(5)(10)
console.log(result) // 输出: 15

// 实际使用示例：
var add5 = makeAdder(5)
console.log(add5(10))   // 15
console.log(add5(14))   // 19  
console.log(add5(1100)) // 1105
console.log(add5(555))  // 560 
```



柯里化优化

```js
// 柯里化的优化
var log = date => type => message => {
    console.log(`[${date.getHours()}:${date.getMinutes()}][${type}]: [${message}]`)
}

// 如果我现在打印的都是当前时间的日志
var nowLog = log(new Date())
nowLog("DEBUG")("查找到轮播图的bug")
nowLog("FEATURE")("新增了添加用户的功能")

var nowAndDebugLog = log(new Date())("DEBUG")
nowAndDebugLog("查找到轮播图的bug")
nowAndDebugLog("查找到轮播图的bug") 
nowAndDebugLog("查找到轮播图的bug")
nowAndDebugLog("查找到轮播图的bug")
```



**案例**

我们工作中会遇到各种需要通过正则检验的需求，比如校验电话号码、校验邮箱、校验身份证号、校验密码等， 这时我们会封装一个通用函数 checkByRegExp ,接收两个参数，校验的正则对象和待校验的字符串

```js
function checkByRegExp(regExp,string) {
    return regExp.test(string);  
}

checkByRegExp(/^1\d{10}$/, '18642838455'); // 校验电话号码
checkByRegExp(/^(\w)+(\.\w+)*@(\w)+((\.\w+)+)$/, 'test@163.com'); // 校验邮箱
```

上面这段代码，乍一看没什么问题，可以满足我们所有通过正则检验的需求。 但是我们考虑这样一个问题，如果我们需要校验多个电话号码或者校验多个邮箱呢？

我们可能会这样做：

```js
checkByRegExp(/^1\d{10}$/, '18642838455'); // 校验电话号码
checkByRegExp(/^1\d{10}$/, '13109840560'); // 校验电话号码
checkByRegExp(/^1\d{10}$/, '13204061212'); // 校验电话号码

checkByRegExp(/^(\w)+(\.\w+)*@(\w)+((\.\w+)+)$/, 'test@163.com'); // 校验邮箱
checkByRegExp(/^(\w)+(\.\w+)*@(\w)+((\.\w+)+)$/, 'test@qq.com'); // 校验邮箱
checkByRegExp(/^(\w)+(\.\w+)*@(\w)+((\.\w+)+)$/, 'test@gmail.com'); // 校验邮箱
```

我们每次进行校验的时候都需要输入一串正则，再校验同一类型的数据时，相同的正则我们需要写多次， 这就导致我们在使用的时候效率低下，并且由于    checkByRegExp 函数本身是一个工具函数并没有任何意义， 一段时间后我们重新来看这些代码时，如果没有注释，我们必须通过检查正则的内容， 我们才能知道我们校验的是电话号码还是邮箱，还是别的什么。

此时，我们可以借助柯里化对 checkByRegExp 函数进行封装，以简化代码书写，提高代码可读性。

```js
//进行柯里化
let _check = curry(checkByRegExp);
//生成工具函数，验证电话号码
let checkCellPhone = _check(/^1\d{10}$/);
//生成工具函数，验证邮箱
let checkEmail = _check(/^(\w)+(\.\w+)*@(\w)+((\.\w+)+)$/);

checkCellPhone('18642838455'); // 校验电话号码
checkCellPhone('13109840560'); // 校验电话号码
checkCellPhone('13204061212'); // 校验电话号码

checkEmail('test@163.com'); // 校验邮箱
checkEmail('test@qq.com'); // 校验邮箱
checkEmail('test@gmail.com'); // 校验邮箱
```



#### 封装柯里化函数

当柯里化函数接收到足够参数后，就会执行原函数

我们有两种思路：

1. 通过函数的 length 属性，获取函数的形参个数，形参的个数就是所需的参数个数
2. 在调用柯里化工具函数时，手动指定所需的参数个数



###  with语句

`with语句` 扩展一个语句的作用域链。

```js
var obj = {
    name: "hello world",
    age: 18
}

with(obj) {
    console.log(name)
    console.log(age)
}
```

不建议使用 `with` 语句，因为它可能是**混淆错误**和**兼容性问题**的根源。

- `with` 语句会将指定对象（如 `obj`）添加到作用域链中，使得在 `with` 块内可以直接访问该对象的属性（如 `name` 和 `age`），无需通过 `obj.name` 的方式引用。
- 尽管语法简洁，但 `with` 语句可能导致变量名冲突、代码可读性差、调试困难等问题。
- 现代 JavaScript（ES6+）中已不推荐使用 `with`，且在严格模式（`'use strict'`）下会被禁止使用。



### eval函数

`eval` 是一个特殊的函数，它可以将传入的字符串当做 JavaScript 代码来运行。

```js
var evalString = `var message = "Hello World"; console.log(message)`;
eval(evalString);

console.log(message);
```

**不建议在开发中使用 `eval` 的原因：**

- ❌ `eval` 代码的可读性非常差（代码的可读性是高质量代码的重要原则）；
- ❌ `eval` 是一个字符串，那么有可能在执行的过程中被刻意篡改，从而造成被攻击的风险；
- ❌ `eval` 的执行必须经过 JS 解释器，不能被 JS 引擎优化。

补充说明：

- `eval()` 函数会动态执行字符串形式的 JavaScript 代码，这虽然灵活，但带来了安全性和性能上的隐患。
- 在现代开发中，应尽量避免使用 `eval`，推荐使用更安全、可维护的方式，如 `Function` 构造函数（谨慎使用）、模板字符串或配置化逻辑等替代方案。



### 严格模式

定义：在 ECMAScript 5 标准中，JavaScript 引入了**严格模式（Strict Mode）**，这是一种具有限制性的 JavaScript 执行模式，旨在让代码从“懒散（sloppy）模式”转向更规范、更安全的编程方式。

 严格模式可以应用到整个脚本或个别函数中。不要在封闭大括弧 `{}` 内这样做，在这样的上下文中这么做是没有效果的。在 `eval` 、`Function`、[事件处理器](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Reference/Attributes#事件处理器属性)属性、[`setTimeout()`](https://developer.mozilla.org/zh-CN/docs/Web/API/Window/setTimeout) 方法中传入的脚本字符串，其行为类似于开启了严格模式的一个单独脚本，它们会如预期一样工作。

#### 为脚本开启严格模式

为整个脚本文件开启严格模式，需要在所有语句之前放一个*特定*语句 `"use strict";`（或 `'use strict';`）。

```js
// 整个脚本都开启严格模式的语法
"use strict";
const v = "你好！我是一个严格模式的脚本！";
```

#### 为函数开启严格模式

同样地，要给某个函数开启严格模式，得把*特定*语句 `"use strict";`（或 `'use strict';`）放在函数体所有语句之前。

```js
function myStrictFunction() {
  // 函数级别严格模式语法
  "use strict";
  function nested() {
    return "我也一样！";
  }
  return `你好！我是严格模式的函数！${nested()}`;
}
function myNotStrictFunction() {
  return "我不是严格模式的函数。";
}
```

#### 作用

**严格模式的核心特点**

1. **更严格的检测与执行**

   - 支持严格模式的浏览器在检测到代码启用严格模式后，会以更严格的方式进行语法检查和代码执行。

2. **消除“静默错误”（Silent Errors）**

   - 在非严格模式下，某些错误不会抛出异常，而是被“静默忽略”（如非法赋值、未声明变量等）。

   - 严格模式通过**抛出错误**来暴露这些原本被隐藏的问题，提高代码健壮性。

   - 示例：

     ```js
     123.name = "abc"; // 静默错误（非严格模式）
     var obj = {};
     Object.defineProperty(obj, "name", { writable: false });
     obj.name = "why"; // 抛出错误（严格模式下）
     ```

3. **提升性能优化**

   - JS 引擎在严格模式下可以进行更多优化，因为不需要处理一些特殊或不安全的语法行为。

4. **禁用未来可能使用的语法**

   - 严格模式禁用了某些在 ECMAScript 未来版本中可能定义的语法，防止兼容性问题。



#### 严格模式限制

强制要求**变量必须声明**，**禁止删除变量和函数**，**禁止使用 `with` 语句和八进制数**，**不允许对只读属性赋值**，**不允许同名函数参数**，以及**禁止 `this` 指向全局对象**等。这些限制是为了提高代码质量，减少潜在错误

1、变量声明

- **非严格模式：** 可以隐式声明变量，即没有使用 `var`、`let` 或 `const` 关键字 
- **严格模式：** 必须使用 `var`、`let` 或 `const` 关键字显式声明变量，否则会导致 ReferenceError

2、函数参数不能有同名属性，否则会报错

- **非严格模式：** 如果函数的参数重复了，**后面** 的参数会覆盖前面的参数
- **严格模式：** 这被认为是一个语法错误

3、不能使用`with`语句

- **非严格模式：** `with` 语句用于创建一个指定对象的作用域，延伸作用域链。但会导致代码可读性和性能问题，因此不推荐使用
- **严格模式：** 完全禁止使用 `with` 语句，会导致 `SyntaxError`

4、不能对只读属性赋值，否则会报错

- **非严格模式：** 对只读属性的赋值不会引发错误，但操作将被忽略
- **严格模式：** 对只读属性的赋值会导致 `TypeError`

5、禁止使用八进制字面量（前缀0）

- **非严格模式：** 八进制字面量（如 010，以0开头）会被解释为八进制数
- **严格模式：** 禁止使用八进制字面量，会导致 `SyntaxError`

6、禁止删除变量、函数和函数的形参

- **非严格模式：** 可以通过 `delete` 操作符删除变量、函数和函数的形参，不报错，但没有效果
- **严格模式：** 禁止使用 `delete` 操作符删除变量、函数和函数的形参，会报 `SyntaxError`，只能删除属性 `delete global[prop]`

7、`eval`中定义的变量和函数不会提升到外层作用域

8、`eval` 和 `arguments` 不能被重新赋值

- **非严格模式：** 可以被赋值
- **严格模式：** 不能被赋值

9、`arguments` 不会自动反映函数参数的变化

- **非严格模式：** 当你修改了函数参数的值，`arguments` 对象中对应的值也会同步更新；反向亦可影响。所以 `arguments` 可以看做是参数的别名，
- **严格模式：** 当你修改了函数参数的值，`arguments` 对象中对应的值不会变化；反向也不会变。相当于只保留初始值，后续变化不会互相影响

等.....我的天 太多了



### 面向对象

定义：面向对象是一种将**现实世界抽象为计算机模型的方法**；JS中的对象被设计成一组属性的无序集合，像是一个哈希表，有key和value组成；key是一个标识符名称，value可以是任意类型，也可以是其他对象或者函数类型；如果值是一个函数，那么我们可以称之为是对象的方法

面向对象如何模拟现实

- **将事物抽象为对象**：面向对象将现实中的事物（如人、车、银行账户等）抽象为具有特定属性和行为的对象。
  - **属性**：描述对象的特征，如汽车的颜色、品牌等。
  - **行为**：对象能做什么，如汽车的启动、停止、加速等方法。
- **通过对象交互解决问题**：在程序中，不再是按步骤执行函数，而是让这些对象通过调用自己的方法来完成任务。例如，一个“银行”对象可以通过调用其“取款”方法从另一个“账户”对象中减去金额。 

面向对象的优点：

* 更贴近现实：他以更自然的视角来组织代码，更容易理解和模拟现实世界中的复杂系统
* 更好的代码组织：将数据和操作数据的方法封装在一起，提高了代码的模块化程度
* 提高代码的可复用性：通过继承和多态，可以复用现有代码并扩展新功能
* 更易于维护和扩展：代码结构更加清晰，更容易进行修改和维护，尤其是大型项目

 

#### **对属性操作的控制**

- 在前面，我们的属性都直接定义在对象内部或者直接添加到对象内部的：
  - 但是这样做时，我们无法对属性进行一些限制，例如：
    - 这个属性是否可以通过 `delete` 删除？
    - 这个属性是否会在 `for-in` 遍历时被遍历出来？

```js
var obj = {
  name: "why",
  age: 18,
  height: 1.88
}
```

- 如果我们想要对一个属性进行更精准的操作控制，就可以使用属性描述符
  - 通过属性描述符可以**精准地添加或修改对象的属性**；
  - 属性描述符需要使用 `Object.defineProperty` 来对属性进行添加或修改。



##### **Object.defineProperty**

- `Object.defineProperty()` 方法会直接在一个对象上定义一个新属性，或者修改一个对象的现有属性，并返回此对象。

  ```js
  Object.defineProperty(obj, prop, descriptor)
  ```

- **可接收三个参数：**

  - `obj`：要定义属性的对象；
  - `prop`：要定义或修改的属性的名称或 Symbol；
  - `descriptor`：要定义或修改的属性描述符。

- **返回值：**

  - 被传递给函数的对象（即被修改的对象）。



#### **属性描述符分类**

- 属性描述符的类型分为两种：
  - **数据属性（Data Properties）描述符**
  - **存取属性（Accessor 访问器 Properties）描述符**

| 特性           | configurable | enumerable | value  | writable | get    | set    |
| -------------- | ------------ | ---------- | ------ | -------- | ------ | ------ |
| **数据描述符** | 可以         | 可以       | 可以   | 可以     | 不可以 | 不可以 |
| **存取描述符** | 可以         | 可以       | 不可以 | 不可以   | 可以   | 可以   |

------

**说明：**

- **数据描述符**：用于定义具有实际值的属性，可设置 `value` 和 `writable`。
- **存取描述符**：用于定义通过 getter 和 setter 方法访问的属性，必须提供 `get` 或 `set`。

> 注意：一个属性描述符不能同时是数据描述符和存取描述符（即不能同时存在 `value/writable` 和 `get/set`）。



#### 数据属性描述符

**数据属性描述符的四个特性**

- **[[Configurable]]**：表示属性是否可以通过 `delete` 删除，是否可以修改其特性，或是否可以将其改为存取属性描述符。
  - 当我们直接在一个对象上定义某个属性时，该属性的 `[[Configurable]]` 默认为 `true`；
  - 当我们通过属性描述符定义一个属性时，该属性的 `[[Configurable]]` 默认为 `false`。
- **[[Enumerable]]**：表示属性是否可以通过 `for-in` 循环或 `Object.keys()` 方法被枚举返回。
  - 当我们直接在一个对象上定义某个属性时，该属性的 `[[Enumerable]]` 默认为 `true`；
  - 当我们通过属性描述符定义一个属性时，该属性的 `[[Enumerable]]` 默认为 `false`。



#### **存取属性描述符**

存取属性描述符（Accessor Properties Descriptor）具有以下四个特性：

- **[[Configurable]]**：表示属性是否可以通过 `delete` 删除，是否可以修改其特性，或是否可以将其改为数据属性描述符。
  - 与数据属性描述符一致；
  - 当直接在对象上定义属性时，`[[Configurable]]` 默认为 `true`；
  - 当通过属性描述符定义属性时，`[[Configurable]]` 默认为 `false`。
- **[[Enumerable]]**：表示属性是否可以通过 `for-in` 或 `Object.keys()` 被枚举返回。
  - 与数据属性描述符一致；
  - 当直接在对象上定义属性时，`[[Enumerable]]` 默认为 `true`；
  - 当通过属性描述符定义属性时，`[[Enumerable]]` 默认为 `false`。
- **[[Get]]**：获取属性值时会执行的函数。默认为 `undefined`。
  - 用于定义 getter 方法。
- **[[Set]]**：设置属性值时会执行的函数。默认为 `undefined`。
  - 用于定义 setter 方法。



#### 定义多个属性描述符













































 













