# AJAX 笔记

### Axios - 查询参数

#### 语法

使用 `axios` 提供的 `params` 选项来传递查询参数。

##### 注意事项

- `axios` 在运行时会自动将参数名和值拼接到 URL 后面，格式为 `?参数名=值`。

**示例**

假设我们需要从服务器获取城市列表，并且需要通过省份名称进行过滤。我们可以使用以下URL：

```python
http://hmajax.itheima.net/api/city?pname=河北省
```

### 使用 `axios` 发送请求

#### 方法一：直接在URL中添加查询参数

```python
axios({
    url: 'http://hmajax.itheima.net/api/city?pname=河北省'
}).then(result => {
    // 对服务器返回的数据做后续处理
});
```

#### 方法二：使用 `params` 选项

```python
axios({
    url: 'http://hmajax.itheima.net/api/city',
    params: {
        pname: '河北省'
    }
}).then(result => {
    // 对服务器返回的数据做后续处理
});
```

**解释**

- **方法一** 直接在URL中添加查询参数，这种方式简单明了，但当参数较多或参数值包含特殊字符时，可能会导致URL过长或编码问题。
- **方法二** 使用 `params` 选项，`axios` 会自动处理参数的编码和拼接，更加灵活和安全。

**案例**：查询省份中的所有城市

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <p></p>

    <script src="http://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>

    <script>
        axios({
            url: 'http://hmajax.itheima.net/api/city',
            params: {
                pname: '安徽省'
            }
        }).then(result => {          //接受一下返回来的结果
            console.log(result.data.list)       // 城市的列表就拿到了
            document.querySelector('p').innerHTML =    // 获取标签给它插上内容
                result.data.list.join('<br>')
        })
    </script>
</body>

</html>
```

**案例**：**地区查询**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css"> -->
    <style>
        :root {
            font-size: 15px;
        }

        body {
            padding-top: 15px;
        }
    </style>
</head>

<body>
    <div class="container">
        <form id="editFrom" class="row">
            <!-- 输入省份名字 -->
            <div class="mb-3 col">
                <label for="from-label">省份名称:</label>
                <input type="text" value="北京" name="province" class="form-control" placeholder="请输入省份名称:">
            </div>
            <!-- 输入城市名称 -->
            <div class="mb-3 col">
                <label class="form-label">城市名称:</label>
                <input type="text" value="北京市" name="city" class="form-control city" placeholder="请输入城市名称:">
            </div>
        </form>
        <button type="button" class="btn btn-primary sel-btn">查询</button>
        <br><br>
        <p>地区列表：</p>
        <ul class="list-group">
            <!-- 示例地区 -->
            <li class="list-group-item">东城区</li>
        </ul>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>

    <script>
        document.querySelector('.sel-btn').addEventListener('click', () => {
            // 获取省份和城市的名字
            let pName = document.querySelector('input[name="province"]').value
            let cName = document.querySelector('.city').value

            // 基于axios请求地区列表数据
            axios({
                url: 'http://hmajax.itheima.net/api/area',
                params: {
                    pname: pName,
                    cname: cName
                }
            }).then(result => {
                let list = result.data.list
                console.log(list)
                // 映射一下 并用一个变量接受
                let theLi = list.map(areaName => `<li class="list-group-item">${areaName}</li>`).join('')
                console.log(theLi)
                // 地区列表请求回来然后渲染到页面上 
                document.querySelector('.list-group').innerHTML = theLi
            })
        })
    </script>
</body>

</html>
```

### Axios 请求配置

#### 1. **Axios 简介**

Axios 是一个基于 Promise 的 HTTP 客户端，可以用于浏览器和 Node.js。它允许开发者轻松地发送异步 HTTP 请求，并处理响应。

------

#### 2. **Axios 请求配置**

在使用 Axios 发送请求时，可以通过配置对象来指定请求的详细信息。以下是一些常用的配置项：

- **url**: 请求的目标 URL 地址。
- **method**: 请求的方法（如 GET、POST、PUT、DELETE 等）。GET 方法可以省略不写。
- **data**: 提交的数据，通常用于 POST、PUT 等方法中。

##### 示例代码

```js
axios({
    url: '目标资源地址',
    method: '请求方法',
    data: {
        参数名: 值
    }
}).then((result) => {
    // 对服务器返回的数据做后续处理
});
```

------

#### 3. **请求示例解析**

假设我们要向服务器发送一个 POST 请求，提交一些用户数据，并处理服务器返回的结果。

##### 示例代码

```js
axios({
    url: 'https://api.example.com/users',  // 目标资源地址
    method: 'POST',                        // 请求方法
    data: {                                // 提交的数据
        name: 'John Doe',
        email: 'john@example.com'
    }
}).then((result) => {
    console.log(result.data);              // 打印服务器返回的数据
}).catch((error) => {
    console.error('请求失败:', error);     // 处理请求错误
});
```

------

#### 4. **注意事项**

- **GET 请求参数**：对于 GET 请求，参数通常通过 URL 查询字符串传递，而不是 `data` 字段。可以使用 `params` 配置项来设置查询参数。

  ```js
  axios({
      url: 'https://api.example.com/users',
      method: 'GET',
      params: {
          id: 123,
          status: 'active'
      }
  }).then((result) => {
      console.log(result.data);
  });
  ```

- **错误处理**：使用 `.catch()` 方法来捕获并处理请求过程中可能出现的错误。

### Axios 错误处理

#### 1. **错误处理语法**

在使用 Axios 发送请求时，可以通过 `.catch()` 方法来捕获和处理可能出现的错误。`.catch()` 方法通常紧跟在 `.then()` 方法之后，用于定义当请求失败时应执行的操作。

##### 示例代码

```js
axios({
    // 请求选项
}).then(result => {
    // 处理数据
}).catch(error => {
    // 处理错误
});
```

------

#### 2. **错误处理流程**

- **发送请求**：首先通过 `axios({...})` 发送 HTTP 请求。
- **成功回调**：如果请求成功，会进入 `.then()` 方法中的回调函数，可以在此处处理返回的数据。
- **错误回调**：如果请求过程中出现错误（如网络问题、服务器返回错误状态码等），会跳过 `.then()` 方法，直接进入 `.catch()` 方法中的回调函数，在此处进行错误处理。

------

#### 3. **错误对象解析**

在 `.catch()` 方法中，传入的 `error` 参数是一个包含错误信息的对象。常见的属性包括：

- **`error.message`**：简短的错误描述。
- **`error.response`**：服务器响应的信息，包括 `status`（状态码）、`data`（响应体数据）等。
- **`error.request`**：请求配置信息。

##### 示例代码

```js
axios({
    url: 'http://example.com/api/data',
    method: 'get'
}).then(response => {
    console.log('请求成功:', response.data);
}).catch(error => {
    console.error('请求失败:', error.message);
    if (error.response) {
        console.error('服务器返回错误:', error.response.status, error.response.data);
    }
});
```

------

#### 4. **实际应用案例**

假设我们正在开发一个用户注册功能，需要防止用户重复注册。当用户尝试注册已存在的用户名时，服务器会返回相应的错误信息，此时可以通过弹框提示用户具体的错误原因。

##### 示例代码

```js
document.querySelector("#btn").addEventListener('click', () => {
    axios({
        url: 'http://hmajax.itheima.net/api/register',
        method: 'post',
        data: {
            username: 'heima12345',
            password: '123456'
        }
    }).then(result => {
        console.log('注册成功:', result.data);
        alert('注册成功！');
    }).catch(error => {
        console.error('注册失败:', error);
        if (error.response && error.response.data.message) {
            alert('注册失败:' + error.response.data.message);
        } else {
            alert('注册失败，请稍后重试');
        }
    });
});
```



**常用请求方法+处理错误信息 案例代码**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <button id="btn">注册用户</button>
    <!-- 引入 Axios 库，用于发送 HTTP 请求 -->
    <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>


    <script>
        // 为按钮添加点击事件监听器
        document.querySelector("#btn").addEventListener('click', () => {
            // 使用 axios 发送 POST 请求到注册接口
            axios({
                // 请求的目标地址
                url: 'http://hmajax.itheima.net/api/register',
                // 指定请求方法为 POST
                method: 'post',
                // 提交的数据（用户名和密码）
                data: {
                    username: 'heima12345',
                    password: '123456'
                }
            }).then(result => {
                // 请求成功时打印返回结果到控制台
                console.log(result)
            }).catch(error => {
                // 处理错误信息
                console.log(error)
                console.log(error.response.data.message)
                alert(error.response.data.message)
            })
        })
    </script>
</body>

</html>
```

### 请求报文格式

#### 1. **请求报文的组成部分**

HTTP 请求报文由四个主要部分组成：

1. **请求行**：包含请求方法、URL 和协议版本。
2. **请求头**：以键值对的形式携带附加信息，如 `Content-Type`、`Accept` 等。
3. **空行**：用于分隔请求头和请求体，空行之后是发送给服务器的资源。
4. **请求体**：包含要发送的数据或资源。

------

#### 2. **示例解析**

以下是一个具体的 HTTP POST 请求示例及其各部分的详细说明：

##### 示例代码

```js
axios({
    url: 'http://hmajax.itheima.net/api/register',
    method: 'post',
    data: {
        username: 'itheima007',
        password: '7654321'
    }
});
```

##### 对应的请求报文

```js
POST http://hmajax.itheima.net/api/register HTTP/1.1
Host: hmajax.itheima.net
Connection: keep-alive
Content-Length: 46
Accept: application/json, text/plain, */*
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/107.0.0.0 Safari/537.36
Content-Type: application/json
Origin: http://127.0.0.1:5500
Referer: http://127.0.0.1:5500/
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9

{"username":"itheima007","password":"7654321"}
```

------

#### 3. **请求行详解**

- **请求方法**：`POST` 表示这是一个 POST 请求，通常用于提交数据。
- **URL**：`http://hmajax.itheima.net/api/register` 是请求的目标地址。
- **协议版本**：`HTTP/1.1` 表示使用 HTTP 1.1 协议。

------

#### 4. **请求头详解**

- **Host**：`hmajax.itheima.net` 指定目标服务器的域名。
- **Connection**：`keep-alive` 表示保持连接状态，以便后续请求复用该连接。
- **Content-Length**：`46` 表示请求体的长度为 46 字节。
- **Accept**：`application/json, text/plain, */*` 表示客户端可以接受的响应内容类型。
- **User-Agent**：描述了发起请求的客户端信息，包括浏览器类型、操作系统等。
- **Content-Type**：`application/json` 表示请求体的内容类型为 JSON 格式。
- **Origin**：`http://127.0.0.1:5500` 表示请求的来源地址。
- **Referer**：`http://127.0.0.1:5500/` 表示当前页面的 URL。
- **Accept-Encoding**：`gzip, deflate` 表示客户端支持的压缩编码方式。
- **Accept-Language**：`zh-CN,zh;q=0.9` 表示客户端首选的语言为简体中文。

------

#### 5. **请求体详解**

- **JSON 数据**：`{"username":"itheima007","password":"7654321"}` 包含了要提交的用户名和密码信息。

### HTTP 协议 - 响应报文

#### 1. **HTTP 协议概述**

HTTP（HyperText Transfer Protocol）协议定义了浏览器与服务器之间通信的规则和格式。它规定了浏览器如何发送请求以及服务器如何返回响应内容。

------

#### 2. **响应报文结构**

响应报文是服务器按照 HTTP 协议要求的格式，返回给浏览器的内容。一个完整的 HTTP 响应报文由以下四个部分组成：

1. **响应行（状态行）**：包含协议版本、HTTP 响应状态码和状态信息。
2. **响应头**：以键值对的形式携带附加信息，如 `Content-Type` 等。
3. **空行**：用于分隔响应头和响应体，空行之后是服务器返回的资源。
4. **响应体**：实际返回的资源数据。

------

#### 3. **示例解析**

假设客户端尝试再次注册用户名为 `itheima007` 的用户，服务器会返回相应的响应报文。

##### 

##### 对应的响应报文示例

```js
HTTP/1.1 400 Bad Request
Date: Tue, 15 Nov 2023 12:00:00 GMT
Server: Apache/2.4.41 (Ubuntu)
Content-Type: application/json; charset=utf-8
Content-Length: 67

{"message":"该用户名已存在，请使用其他用户名进行注册"}
```

------

#### 4. **响应行详解**

- **协议版本**：`HTTP/1.1` 表示使用的 HTTP 协议版本。
- **HTTP 响应状态码**：`400` 表示请求有误，通常是因为客户端发送的请求不符合服务器的要求。
- **状态信息**：`Bad Request` 是对状态码的描述，进一步说明请求的问题。

------

#### 5. **响应头详解**

- **Date**：`Tue, 15 Nov 2023 12:00:00 GMT` 表示服务器生成响应的时间。
- **Server**：`Apache/2.4.41 (Ubuntu)` 表示服务器软件的信息。
- **Content-Type**：`application/json; charset=utf-8` 表示响应体的内容类型为 JSON 格式，并且字符编码为 UTF-8。
- **Content-Length**：`67` 表示响应体的长度为 67 字节。

------

#### 6. **响应体详解**

- **JSON 数据**：`{"message":"该用户名已存在，请使用其他用户名进行注册"}` 包含了服务器返回的具体错误信息。

  ### HTTP 响应状态码笔记

  #### 1. **HTTP 响应状态码概述**

  HTTP 响应状态码用于表明请求是否成功完成。每个状态码都有其特定的含义，帮助客户端理解服务器对请求的处理结果。

  ------

  #### 2. **状态码分类**

  HTTP 状态码按照功能分为五类：

  | 状态码范围 | 说明                                                 |
  | ---------- | ---------------------------------------------------- |
  | `1xx`      | 信息性响应，表示请求已接收，继续处理。               |
  | `2xx`      | 成功响应，表示请求已被成功接收、理解、接受。         |
  | `3xx`      | 重定向消息，表示需要采取进一步的操作以完成请求。     |
  | `4xx`      | 客户端错误，表示请求包含语法错误或无法完成。         |
  | `5xx`      | 服务端错误，表示服务器在处理请求的过程中发生了错误。 |

  ------

  #### 3. **常见状态码示例**

  - **`404`**：服务器找不到资源。
  - **`200`**：请求成功，服务器返回了预期的数据。
  - **`301`**：永久重定向，请求的资源已永久移动到新位置。
  - **`400`**：坏请求，通常是因为客户端发送的请求有误。
  - **`500`**：内部服务器错误，服务器遇到意外情况，无法完成请求。

  ------

  #### 4. **状态码详解**

  ##### 1xx - 信息性响应

  - 表示请求已接收，继续处理。
  - 示例：`100 Continue`（继续），`101 Switching Protocols`（切换协议）。

  ##### 2xx - 成功响应

  - 表示请求已被成功接收、理解、接受。
  - 示例：`200 OK`（成功），`201 Created`（已创建），`204 No Content`（无内容）。

  ##### 3xx - 重定向消息

  - 表示需要采取进一步的操作以完成请求。
  - 示例：`301 Moved Permanently`（永久重定向），`302 Found`（临时重定向），`304 Not Modified`（未修改）。

  ##### 4xx - 客户端错误

  - 表示请求包含语法错误或无法完成。
  - 示例：`400 Bad Request`（坏请求），`401 Unauthorized`（未授权），`403 Forbidden`（禁止访问），`404 Not Found`（未找到）。

  ##### 5xx - 服务端错误

  - 表示服务器在处理请求的过程中发生了错误。
  - 示例：`500 Internal Server Error`（内部服务器错误），`501 Not Implemented`（尚未实现），`502 Bad Gateway`（错误网关），`503 Service Unavailable`（服务不可用）。

  **示例代码**

  ```html
  <!DOCTYPE html>
  <html lang="en">
  
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
  </head>
  
  <body>
      <button id="btn">注册用户</button>
      <!-- 引入 Axios 库，用于发送 HTTP 请求 -->
      <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
  
  
      <script>
          // 为按钮添加点击事件监听器
          document.querySelector("#btn").addEventListener('click', () => {
              // 使用 axios 发送 POST 请求到注册接口
              axios({
                  // 请求的目标地址
                  url: 'http://hmajax.itheima.net/api/registr',
                  // 指定请求方法为 POST
                  method: 'post',
                  // 提交的数据（用户名和密码）
                  data: {
                      username: 'heima12345',
                      password: '123456'
                  }
              }).then(result => {
                  // 请求成功时打印返回结果到控制台
                  console.log(result)
              }).catch(error => {
                  // 处理错误信息
                  console.log(error)
                  console.log(error.response.data.message)
                  alert(error.response.data.message)
              })
          })
      </script>
  </body>
  
  </html>
  ```

  ![image-20250524153726456](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250524153726456.png)

![image-20250524153743511](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250524153743511.png)

### 接口文档与接口调用

#### 1. **接口文档概述**

- **定义**：接口文档是描述接口的文章，通常由后端工程师编写。它详细说明了如何通过 AJAX 和服务器进行通讯时使用的 URL、请求方法以及参数。

- **作用**：帮助前端开发者了解如何正确地调用后端提供的服务，确保前后端之间的数据交互能够顺利进行。

- ##### 请求方法

  - **GET**：用于获取资源信息。

#### 2. **传送门 - API 文档链接**

- **链接**：https://www.apifox.cn/apidoc/project/163784/doc/1695440
- **说明**：点击该链接可以访问详细的 API 文档，了解更多接口的使用方法和参数说明。

**代码示例**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <button class="btn">登录</button>
    <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>

    <script>
        document.querySelector('.btn').addEventListener('click', () => {
            axios({
                url: 'http://hmajax.itheima.net/api/login',
                method: 'post',
                data: {
                    username: 'heima123456',
                    password: '123456'
                }
            }).then(result => {
                console.log(result)
            })
        })
    </script>
</body>

</html>
```

![image-20250524160256591](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250524160256591.png)

![image-20250524160307375](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250524160307375.png)

![image-20250524160320653](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250524160320653.png)

**登录案例**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <h3>欢迎-登录</h3>
    <div class="alert alert_success" role="alert">提示消息</div>

    <!-- 表单 -->
    <div class="form-wrap">
        <form>
            <div class="mb-3">
                <label for="username" class="form-label">账号名</label>
                <input type="text" class="form-control username">
            </div>
            <div class="mb-3">
                <label for="password" class="forrm-label">密码</label>
                <input type="password" class="form-control password">
            </div>
            <button type="button" class="btn btn-primary btn-login">登录</button>
        </form>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>

    <script>
        document.querySelector('.btn-login').addEventListener('click', () => {
            const alertBox = document.querySelector('.alert')

            const username = document.querySelector('.username').value
            const password = document.querySelector('.password').value
            // console.log(username, password)

            // 判断长度
            if (username.length < 8) {
                console.log('用户名必须大于等于8位', false)
                return
            }
            if (password.length < 6) {
                console.log('密码必须大于等于6位')
                return
            }

            // console.log('提交到服务器')
            axios({
                url: 'http://hmajax.itheima.net/api/login',
                method: 'post',
                data: {
                    username: username,
                    password: password
                }
            }).then(result => {
                console.log(result);
                console.log(result.data.message)
            })
        })
    </script>
</body>

</html>
```





### form-serialize 插件

#### 作用

- **快速收集表单元素的值**：`form-serialize`插件可以方便地将表单中的数据转换为JavaScript对象或字符串，便于后续处理和发送请求。

#### 示例

假设有一个简单的登录表单：

```js
<form class="example-form">
    <label for="username">账号名</label>
    <input type="text" id="username" name="username" value="itheima007">

    <label for="password">密码</label>
    <input type="password" id="password" name="password" value="7654321">
</form>
```

使用`form-serialize`插件可以轻松获取表单数据，并将其转换为JSON格式的对象。

#### 语法

```js
const form = document.querySelector('.example-form');
const data = serialize(form, { hash: true, empty: true });
console.log(data);
```

- `hash: true`：表示将表单数据转换为一个对象（哈希表），其中键是表单元素的`name`属性值，值是对应的输入值。
- `empty: true`：表示即使表单元素为空，也会包含在结果中。

#### 结果

执行上述代码后，控制台会输出如下内容：

```js
{
    "username": "itheima007",
    "password": "7654321"
}
```

#### 使用场景

- **表单提交**：在用户提交表单时，可以使用`form-serialize`插件快速收集表单数据，并将其作为请求体发送到服务器。
- **表单验证**：在进行表单验证时，可以先使用`form-serialize`插件获取表单数据，然后对数据进行检查和处理。