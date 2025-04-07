# Ajax        你好你好

### 一、Ajax

#### 1.1 什么是Ajax

Ajax 的全称是 Asynchronous Javascript And XML（异步 JavaScript 和 XML）。

通俗理解：在网页中利用 XMLHttpRequest 对象和服务器进行数据交互的方式，就是 Ajax。

#### 1.2 为什么要学Ajax

之前所学的技术，只能把网页做的更美观漂亮，或添加一些动画效果，但是，Ajax 能让我们轻松实现网页与服务器之间的数据交互。

![image-20250331204351938](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250331204351938.png)

- **用户**：通过浏览器与网页进行交互。
- **网页**：使用 Ajax 技术与服务器进行数据传输。
- **服务器**：处理请求并返回数据。

#### 1.3 Ajax的典型应用场景

- 用户名检测：注册用户时，通过 ajax 的形式，动态检测用户名是否被占用。
- 实时更新：如股票行情、新闻滚动等，无需刷新页面即可获取最新数据。
- 表单验证：提交表单前，通过 Ajax 验证表单数据的有效性。
- 异步加载：分页加载、懒加载图片等，提高用户体验。

![image-20250331205120949](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250331205120949.png)

![image-20250331205141228](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250331205141228.png)





### 二、jQuery中的Ajax

#### 2.1 了解jQuery中的Ajax

浏览器中提供的 XMLHttpRequest 用法比较复杂，所以 jQuery 对 XMLHttpRequest 进行了封装，提供了一系列 Ajax 相关的函数，极大地降低了 Ajax 的使用难度。

jQuery 中发起 Ajax 请求最常用的三个方法如下：

- `$get()`
- `$post()`
- `$.ajax()`

#### 2.2 `$get()` 函数的语法

jQuery 中 `$get()` 函数的功能单一，专门用来发起 get 请求，从而将服务器上的资源请求到客户端来进行使用。

`$get()` 函数的语法如下：

```js
$.get(url, [data], [callback])
```

- `url` 要请求的资源地址
- `data` 请求资源期间要携带的参数
- `callback` 请求成功时的回调函数

##### `$get()` 发起不带参数的请求

使用 `$get()` 函数发起不带参数的请求时，直接提供请求的 URL 地址和请求成功之后的回调函数即可，示例代码如下：

```js
$.get('http://localhost:3000/api/getbooks', function(res) {
    console.log(res); // 这里的 res 是服务器返回的数据
});
```

![image-20250331205338904](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250331205338904.png)

##### $.get()发起带参数的请求

使用 $.get() 函数发起带参数的请求时，示例代码如下：

```js
$.get('http://localhost:3000/api/getbooks', { id: 1 },function(res) {
	console.log(res)
})
```

![image-20250331205442186](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250331205442186.png)

### 2.3 `$post()` 函数的语法

#### 2.3.1 理解 `$post()` 函数

jQuery 中 `$post()` 函数的功能单一，专门用来发起 post 请求，从而向服务器提交数据。

#### 2.3.2 `$post()` 函数的语法

`$post()` 函数的语法如下：

```js
$.post(url, [data], [callback])
```

- `url` 提交数据的地址
- `data` 要提交的数据
- `callback` 数据提交成功时的回调函数

#### 2.3.3 使用 `$post()` 向服务器提交数据

使用 `$post()` 向服务器提交数据的示例代码如下：

```js
$.post(
    'http://localhost:3000/api/addbook', // 请求的 URL 地址
    { bookname: '水浒传', author: '施耐庵', publisher: '上海图书出版社' }, // 提交的数据
    function(res) { // 回调函数
        console.log(res)
    }
);
```

![image-20250331205726725](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250331205726725.png)

### 2.4 `$.ajax()` 函数的语法

#### 2.4.1 理解 `$.ajax()` 函数

相比于 `$get()` 和 `$post()`，jQuery 中提供的 `$.ajax()` 函数，是一个功能比较综合的函数，它允许我们对 Ajax 请求进行更详细的配置。

`$.ajax()` 函数的基本语法如下：

javascript

深色版本



```js
$.ajax({
    type: '', // 请求的方式，例如 GET 或 POST
    url: '', // 请求的 URL 地址
    data: {}, // 这次请求要携带的数据
    success: function(res) { // 请求成功之后的回调函数
        // 处理返回的数据
    }
});
```

#### 2.4.2 使用 `$.ajax()` 发起 GET 请求

使用 `$.ajax()` 发起 GET 请求时，只需要将 `type` 属性的值设置为 `'GET'` 即可：

```js
$.ajax({
    type: 'GET', // 请求的方式
    url: 'http://localhost:3000/api/getbooks', // 请求的 URL 地址
    data: { id: 1 }, // 这次请求要携带的数据
    success: function(res) { // 请求成功之后的回调函数
        console.log(res)
    }
});
```

#### 2.4.3 使用 `$.ajax()` 发起 POST 请求

使用 `$.ajax()` 发起 POST 请求时，只需要将 `type` 属性的值设置为 `'POST'` 即可：

```js
$.ajax({
    type: 'POST', // 请求的方式
    url: 'http://localhost:3000/api/addbook', // 请求的 URL 地址
    data: { // 要提交给服务器的数据
        bookname: '水浒传',
        author: '施耐庵',
        publisher: '上海图书出版社'
    },
    success: function(res) { // 请求成功之后的回调函数
        console.log(res)
    }
});
```

### 三、接口

#### 3.1 接口的概念

使用 Ajax 请求数据时，被请求的 URL 地址，就叫做数据接口（简称接口）。同时，每个接口必须有请求方式。

例如：

- `http://localhost:3000/api/getbooks` 获取图书列表的接口（GET 请求）
- `http://localhost:3000/api/addbook` 添加图书的接口（POST 请求）

#### 3.2 分析接口的请求过程

1. **通过 GET 方式请求接口的过程**

    

   ![image-20250331211037046](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250331211037046.png)

   - 用户与网页交互，希望从服务器获取数据。
   - 网页发起 GET 数据请求。
   - 服务器处理请求并响应 GET 请求。

2. **通过 POST 方式请求接口的过程**

    ![image-20250331211057026](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250331211057026.png)

   - 用户与网页交互，希望向服务器提交数据。
   - 网页发起 POST 数据请求。
   - 服务器处理请求并响应 POST 请求。

### 3.3 接口文档

#### 什么是接口文档

接口文档，顾名思义就是接口的说明文档。它是我们调用接口的依据。好的接口文档包含了对接口 URL、参数以及输出内容的说明。我们参照接口文档就能方便的知道接口的作用，以及接口如何进行调用。

#### 接口文档的组成部分

接口文档可以包含很多信息，也可以按需进行精简。不过，一个合格的接口文档，应该包含以下6项内容，从而为接口的调用提供依据：

- **接口名称**：用来标识各个接口的简单说明。如登录接口，获取图书列表接口等。
- **接口 URL**：接口的调用地址。
- **调用方式**：接口的调用方式，如 GET 或 POST。
- **参数格式**：接口需要携带的参数。每个参数必须包含参数名称、参数类型、是否必选、参数说明这4项内容。
- **响应格式**：接口的返回值的详细描述，一般包含数据名称、数据类型，说明3项内容。
- **返回示例（可选）**：通过对象的形式，举例服务器返回数据的结构。

![image-20250331211307768](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250331211307768.png)

​         ![image-20250331211319313](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250331211319313.png)