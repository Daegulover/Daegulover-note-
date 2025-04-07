# js大哥



### js使用方法

直接在body里面写

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <input type="button" value="按钮" onclick="alert('你好')">
</body>
</html>
```

![image-20250313103922104](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250313103922104.png)

写 script

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        alert('你好')
    </script>
</head>
<body>

</body>
</html>
```





### 变量

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        let name = '王佳敏'
        let age = 18
        let salay = 50000

        // 模板字符串
        alert(`我叫${name},今年${age}岁,工资有${salay}元`)
        
        // 变量名格式：大驼峰，小驼峰

        // 小驼峰：lastName,getPage
        // 大驼峰：LastName,GetPage
   </script>
</head>
<body>
    
</body>
</html>
```

小驼峰：lastName,getPage

 大驼峰：LastName,GetPage



### 获取字符串的长度

#### length

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        var str1 = 'sssssssssssssfffffffffffffffffffffffffffjjjjjjjjjjjjjjjjjjj'
        console.log(str1.length);
        
    </script>
</head>
<body>
    
</body>
</html>
```





### 查看数据类型

#### typeof

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=, initial-scale=1.0">
    <title>Document</title>
    <script>
        var str = 18
        console.log(typeof str);
        
    </script>
</head>
<body>
    
</body>
</html>
```





### var 和 let 的区别

var是全局变量，在任何地方都可以用到

let只在代码块中用到





### 变量

var 变量 = 内容

#### 同时声明多个变量

同时声明多个变量时，只需要写一个 var， 多个变量名之间使用英文逗号隔开。

```js
var age = 10,  name = 'zs', sex = 2;     
```

声明变量特殊情况

| 情况                           | 说明                    | 结果      |
| ------------------------------ | ----------------------- | --------- |
| var  age ; console.log (age);  | 只声明 不赋值           | undefined |
| console.log(age)               | 不声明 不赋值  直接使用 | 报错      |
| age   = 10; console.log (age); | 不声明   只赋值         | 10        |





###  变量命名规范

规则：

- 由字母(A-Za-z)、数字(0-9)、下划线(_)、美元符号( $ )组成，如：usrAge, num01, _name
- 严格区分大小写。var app; 和 var App; 是两个变量
- 不能 以数字开头。  18age   是错误的
- 不能 是关键字、保留字。例如：var、for、while
- 变量名必须有意义。 MMD   BBD        nl   →     age  
- 大驼峰命名法：第一个单词的第一个字母大写 LastName,GetPage
- 小驼峰命名法：第一个单词的第一个字母小写 lastName,getPage





### 数据类型

#### 简单数据类型

![image-20250314091946425](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250314091946425.png)

##### 数字型三个特殊值

- Infinity ，代表无穷大，大于任何数值

- -Infinity ，代表无穷小，小于任何数值

- NaN ，Not a number，代表一个非数值



##### isNaN

用来判断一个变量是否为非数字的类型，返回 true 或者 false

   ![](C:\Users\32473\Desktop\5. ECMA01\images\图片17.png)

   ```javascript
var usrAge = 21;
var isOk = isNaN(userAge);
console.log(isNum);          // false ，21 不是一个非数字
var usrName = "andy";
console.log(isNaN(userName));// true ，"andy"是一个非数字
   ```



##### 字符串型 String

​		字符串型可以是引号中的任意文本，其语法为 双引号 "" 和 单引号''

```js
var strMsg = "我爱北京天安门~";  // 使用双引号表示字符串
var strMsg2 = '我爱吃猪蹄~';    // 使用单引号表示字符串
// 常见错误
var strMsg3 = 我爱大肘子;       // 报错，没使用引号，会被认为是js代码，但js没有这些语法
```

​		因为 HTML 标签里面的属性使用的是双引号，JS 这里我们更推荐使用单引号。



1. 字符串引号嵌套

   ​		JS 可以用单引号嵌套双引号 ，或者用双引号嵌套单引号 (外双内单，外单内双)

   ```js
   var strMsg = '我是"高帅富"程序猿';   // 可以用''包含""
   var strMsg2 = "我是'高帅富'程序猿";  // 也可以用"" 包含''
   //  常见错误
   var badQuotes = 'What on earth?"; // 报错，不能 单双引号搭配
   ```

2. 字符串转义符

   ​		类似HTML里面的特殊字符，字符串中也有特殊字符，我们称之为转义符。

   ​		转义符都是 \ 开头的，常用的转义符及其说明如下：

   | 转义符 | 解释说明                          |
   | ------ | --------------------------------- |
   | \n     | 换行符，n   是   newline   的意思 |
   | \ \    | 斜杠   \                          |
   | \'     | '   单引号                        |
   | \"     | ”双引号                           |
   | \t     | tab  缩进                         |
   | \b     | 空格 ，b   是   blank  的意思     |

1. 字符串长度

   	字符串是由若干字符组成的，这些字符的数量就是字符串的长度。通过字符串的 length 属性可以获取整个字符串的长度。

   ```js
   var strMsg = "我是帅气多金的程序猿！";
   alert(strMsg.length); // 显示 11
   ```

2. 字符串拼接

   - 多个字符串之间可以使用 + 进行拼接，其拼接方式为 字符串 + 任何类型 = 拼接之后的新字符串

   - 拼接前会把与字符串相加的任何类型转成字符串，再拼接成一个新的字符串

     ```js
     //1.1 字符串 "相加"
     alert('hello' + ' ' + 'world'); // hello world
     //1.2 数值字符串 "相加"
     alert('100' + '100'); // 100100
     //1.3 数值字符串 + 数值
     alert('11' + 12);     // 1112 
     ```

     - ***+ 号总结口诀：数值相加 ，字符相连***

3. 字符串拼接加强

```js
console.log('小花' + 8);        // 只要有字符就会相连 
var age = 8;
console.log('小花age岁啦');      // 错误写法
console.log('小花' + age);         // 小花8
console.log('小花' + age + '岁啦'); // 小花8岁啦
```

- 经常会将字符串和变量来拼接，变量可以很方便地修改里面的值
- 变量是不能添加引号的，因为加引号的变量会变成字符串
- 如果变量两侧都有字符串拼接，口诀“引引加加 ”，删掉数字，变量写加中间



- 布尔型Boolean

  ​		布尔类型有两个值：true 和 false ，其中 true 表示真（对），而 false 表示假（错）。

  ​		布尔型和数字型相加的时候， true 的值为 1 ，false 的值为 0。

  ```js
  console.log(true + 1);  // 2
  console.log(false + 1); // 1
  ```

- Undefined和 Null

  ​		一个声明后没有被赋值的变量会有一个默认值undefined ( 如果进行相连或者相加时，注意结果）

  ```js
  var variable;
  console.log(variable);           // undefined
  console.log('你好' + variable);  // 你好undefined
  console.log(11 + variable);     // NaN
  console.log(true + variable);   //  NaN
  ```

  ​		一个声明变量给 null 值，里面存的值为空（学习对象时，我们继续研究null)

  ```js
  var vari = null;
  console.log('你好' + vari);  // 你好null
  console.log(11 + vari);     // 11
  console.log(true + vari);   //  1
  ```

### 



### 获取变量数据类型

- 获取检测变量的数据类型

  ​		typeof 可用来获取检测变量的数据类型

  ```js
  var num = 18;
  console.log(typeof num) // 结果 number      
  ```

  ​		不同类型的返回值

  ![](C:\Users\32473\Desktop\5. ECMA01\images\图片18.png)

- 字面量

  ​		字面量是在源代码中一个固定值的表示法，通俗来说，就是字面量表示如何表达这个值。

  **数字（Number）字面量** 可以是整数或者是小数，或者是科学计数(e)。

  - 例 数字字面量：8, 9, 10
  - **字符串（String）字面量** 可以使用单引号或双引号:
  - 例 字符串字面量：'大家好', "前端工程师们"
  - 布尔值字面量 可以是‘true' 'false'
  - 例 布尔字面量：true，false

### 数据类型转换

​		什么是数据类型转换？

​		使用表单、prompt 获取过来的数据默认是字符串类型的，此时就不能直接简单的进行加法运算，而需要转换变量的数据类型。通俗来说，就是把一种数据类型的变量转换成另一种数据类型，通常会实现3种方式的转换：

```
转换为字符串类型
转换为数字型
转换为布尔型
```

- 转换为字符串

  ![](C:\Users\32473\Desktop\5. ECMA01\images\图片19.png)

  - toString() 和 String()  使用方式不一样。
  - 三种转换方式，更多第三种加号拼接字符串转换方式， 这一种方式也称之为隐式转换。



隐式转换：加法





### 数组

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        // 获取数组arr里索引为2的值
        var arr = [1,2,3,4]
        console.log(arr[2]);
        
        // 替换数组里的值
        var arr2 = [1,2,3,4]
        arr2[3] = 7
        console.log(arr2)

        // 获取数组的长度
        var arr3 = [2,66,33,50,90]
        console.log(arr3.length)

        
        // 在页面上显示
        var arr4 = [34,89,99,24,11]
        arr4.push('3')
        // 反引号这个是模板字符串
        document.write(`arr4数组的长度为${arr4.length}`)
    </script>
</head>
<body>
    
</body>
</html>
```





### 对象

三种创造对象的方式

#### 第一种

```js
        // 第一种
        var p = new object()
        // p.name 是给p对象添加name 属性，p.name = 'zhangsan' 就是添加一个name属性并赋值给zhangsan , p.name说明p对象中的name属性
        p.name = 'zhangsan'
        p.age = 18
        console.log(p.name)
        // 不可以用alert打印， 看不到具体对象的内容

```

#### 第二种

```js
        // 第二种
        var p1 = {}
        p1.name = 'zhangsan'
        p1.age = 18

        varp2 = {
            name:'lisi',
            age:18,
            address:'hbsi'
        }

```

#### 第三种

```js
        // 第三种
        // 需要连属性一块套起来
        var p3 = new Object({
            name:'lisi',
            age:18,
            address:'hbsi'
        })

```



所有的对象都是基于object对象来的

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <!-- 由{}定义 -->
     <script>
        var info = {
            name : 'zs',
            age : 18,
            eat:function(){
                console.log('吃饭');
            }
        }
        // 获取对象的数据
        console.log(info.name)
        // 查找age的变量,如果不加引号，则是查找名为age的变量
        console.log(info['age'])
     </script>
</head>
<body>
    
</body>
</html>
```







### 运算符

#### 算术运算符

![image-20250320083414826](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250320083414826.png)

#### 三目运算符

如果表达式为真     执行问好右边的

如果表达式为假     执行冒号右边的

```js
var num = 1 > 2 ? 2 :1
```

1 > 2 是假  输出 1





### switch分支流程控制

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        var time = prompt('请输入时间:')
        switch(time){
            case'12点':
                alert('中午好！')
                break;
            case'18点':
                alert('傍晚好!')
                break;
            case'23点':
                alert('深夜好!')
                break;
            default:
                alert('抱一丝 都不好')
        }
    </script>
</head>
<body>
    
</body>
</html>
```





### while循环

先判断后执行

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        // 输出10次  abc
        var i = 0
        while(i < 10){
            i++
            console.log('abc');
        }
    </script>
</head>
<body>
    
</body>
</html>
```





### do-while循环

先执行后判断

```html
<script>
  let choice;
  do {
    console.log("请选择一个操作：");
    console.log("1. 查看信息");
    console.log("2. 编辑信息");
    console.log("3. 退出");
    choice = prompt("请输入你的选择(1-3):");

    switch (choice) {
      case "1":
        console.log("查看信息...");
        break;
      case "2":
        console.log("编辑信息...");
        break;
      case "3":
        console.log("退出...");
        break;
      default:
        console.log("无效的选择，请重新输入。");
        break;
    }
  } while (choice !== "3");
</script>
```









### for循环

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        var arr = [1,2,3,4,5,6,7,8,9,10,2,3,4,5,6,7,8,9,10,2,3,4,5,6,7,8,9,10]
        // 如果遇到很长很长的
        for(var i = 0 ; i < arr.length ; i++){
            console.log(arr[i])
        }
    </script>
</head>
<body>
    
</body>
</html>
```





### for in 语句

遍历数组或者遍历对象的语句



for（数组的索引 in 循环的数据）



这样输出来的是数组的索引

 console.log(index)

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        var arr = [1,2,3,4,5,6,7,8,9]
        // 数组的索引 in 循环的数据
        // 输出来的是数组的索引
        for(index in arr){
            console.log(index)
        }
    </script>
</head>
<body>
    
</body>
</html>
```



这个输出来的是数据 不是索引

console.log(arr2[index])

```js
        var arr2 = [1,2,3,4,5,6,7,8,9]
        // 输出来的是数据 不是索引
        for(index in arr2){
            console.log(arr2[index])
        }

```





```js
var arr3 = [1,2,3,4,5,6,7,8,9]
for(index in arr3){
    console.log(`输出的是${index} , 输出的是${arr[index]}`)
}
```







### 跳转语句

#### break

#### continue









## 函数

### 如何定义函数

#### 方式一：使用关键字 function 函数名（）{}

```js
function fn(){
    console.log()
}
fn()
```



#### 方式二：表达式的方法 var fn = function(){}

#### 方式三：es6 箭头函数写法

```html
const fn = () =>{

}
fn( )
```

```js
    // 用es6 去写
    // 函数体里面有一行代码 或者 一行返回值的话可以省略return关键字和{}
    const sum = (a,b) => a+b 
    console.log(sum(100,200))
```





### 无参函数 

无参函数就是函数名的小括号中不定义任何函数

```js
<script>
    function sayHello(){
    alert("Hello World!")
}
</script>
```



### 有参函数

function函数名（参数1 ， 参数2 ， 参数3.....）{

}

```js
function sum (a,b){
    console.log(a+b)
}

sum(100,200)
```

```js
    // 声明一个带参数的方法
    function myFunction(name, age){
        alert("姓名:" + name + " ,年龄 :" +age);
    }

    // 调用带参的方法
    myFunction("zhangsan" , 18)
    //其中的name和age就是用一个参数，在调用这个函数时
    //name的值是“zhangsan”,age的值是18

```



### js声明带有返回值的函数

在完成一个业务后，需要返回一个具体的值，这就要函数的返回值

```js
Function myFunction(参数){
函数代码块;
return语句;
}
```

### 局部变量和全局变量

#### 全局变量

在script内部声明的变量是全局变量

函数体内声明的变量，只能在函数体内使用

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        // 函数体内声明的变量，只能在函数体内使用
        function fn(){
            // 局部变量
            var num = 10
        }
        fn()
        console.log(num);
        // 报错
    </script>
</head>
<body>
    
</body>
</html>
```

需要注意的是，如果没有使用var声明变量，该变量将被自动作为全局变量声明。





### js变量的生命周期

js变量的生命周期从他们被声明的时间开始

局部变量会在函数运行以后被删除

全局变量会在页面关闭后被删除





### 全局变量和局部变量的区别

1. **声明位置不同**

   局部变量在函数的内部；

   全局变量声明在函数外部。

2. **作用域不一样**

   局部变量只在某一局部范围有效，比如函数内部；

   全局变量在整个页面有效，网页上的所有脚本和函数都能访问他。

3. **生命周期不同**

   局部变量会在运行以后被删除；

   全局变量会在页面关闭之后被删除。





### 匿名函数

所以总而言之，他没有名字。

一般的**有名函数**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        function myFun(a,b){
            console.log(a+b);
        }
        myFun(30,22)
    </script>

</head>
<body>

</body>
</html>
```

**匿名函数：**有关键字 function，有小括号，有大括号，就是没有函数名

```js
    <script>
        function(a,b){
            console.info(a+b)
        }

```

那...那咋办？

有5个方法！偷着乐叭 这么多



#### **方法一**：函数字面量 

把它放在一个变量里，这个变量就相当于一个函数名。这个匿名函数也就有名字了

```js
        // 方法一：函数字面量
        var myFun = function(a,b){
            console.log(a+b)
        }
        myFun(33,90)     //123
```



#### **方法二**：不要名字

咱不要名字了哈，做个无名的‘代码’，6，这么做可以在内部形成局部变量和局部函数，防止全局污染；

（然后科普一下  什么是**全局污染**？？）

”由于不当的变量或函数定义，导致它们意外地成为了全局作用域的一部分，从而与预期的作用域（如函数内部或模块内部）产生了冲突。“

如何解决全局污染？？

```js
// 方式1: 定义全局变量命名空间,只创建一个全局变量，并定义该变量为当前应用容器，把其他全局变
量追加在该命名空间下。
//我们可以把app这个全局变量当成一个命名空间,然后把其他的所有全局变量都放在它下面;
var my={}; //唯一的全局变量
my.name={
big_name:"zhangsan",
small_name:"lisi"
};
my.work={
school_work:"study",
family_work:"we are"
};
// alert(my.name.small_name);
// 方式2: 利用匿名函数将脚本包裹起来
(function(){
var temp = {};
//把两个变量赋值给temp
//temp.school_work = "study";
//temp.small_name = "李四";
small_name = "李四";
temp.getName = function(){
return small_name;
}
//把tmep赋值给全局变量test
window.test = temp;
}())
// alert(test.getName());
```



是这样的...看好了！

（匿名函数）()

(匿名函数（）)

```js
        // 方法二：不要名字
        (function(a,b){
            console.log(a*b)
        })(34,44)

		(function(a,b){
            console.log(a+b)
        }(54,9))
```

这个真的很方便！！好用反正



#### 方法三：利用事件调用

```js
        // 方法三：利用事件去调用
        var btn = document.getElementById("btn")   //找到页面的某个标签
        // 添加事件
        if(btn){
            btn.onclick = function(){
                console.log("你点到我啦")
        }
    }else{
        console.error("滚蛋吧")
    }

```





#### 方法四：作为对象去调用

我还不会...等会吧



#### 方法五：作为另一个函数的参数

还有方法五... 我也不会









### 构造函数

是来创造对象的

实例化对象的函数

构造函数可以生成一个对象

**关键字**：this

**创建对象关键字**：new



常见的构造函数：

```js
1. var arr = [];   为  var arr = new Array();    的语法糖。
2. var obj = {}  为  var obj = new Object();    的语法糖
3. var date = new Date();
4. ...
```



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        var obj = {
            name :'zhangsan',
            age :18
        }

        // 构造函数 构造函数可以生成一个对象
        function Star(name,age,sex){
            this.name = name
            this.age = age
            this.sex = sex
            //创建了一个新变量 eat 
            //eat方法被定义为一个匿名函数，当调用eat方法时，会在控制台打印出“吃饭”。
            this.eat = function(){
                console.log('吃饭')
            }
        }

        var cmm = new Star('cmm',2.5,'男')
        console.log(cmm)
    </script>
</head>
<body>
    
</body>
</html>
```









### 回调函数

**回调一个函数的参数，将这个函数作为参数传到另一个函数里面，当这个函数执行完之后在执行传进去的这个函数。这个过程就是回调**

主函数先干完，然后再回过头来调用传进来的函数

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        // 先定义主函数,回调函数作为参数
        function A(callback){
            callback();
            console.log('我是主函数')
        }

        // 定义回调函数
        function B(){
            setTimeout("console.log('我是回调函数')",7000)   //通过模仿耗时操作，您可以清楚地看到异步函数
        }
        A(B)
        //输出结果
        //我是主函数
        //我是回调函数
    </script>
</head>
<body>
    
</body>
</html>
```



setTimeout()    //定时器效果，隔多长时间执行一次，整个程序只执行一次

setInterval()     //定时器效果，隔多长时间执行一次（多次）





### 变量提升

1、所有声明都会被提升到作用域的最顶上；

2、同一个变量声明只进行一次，并且因此其他声明都会被忽略；

3、函数声明的优先级优于变量申明，且函数声明会连带定义一起被提升。

#### 变量提升：

​	把变量声明提升到函数的顶部，但是变量赋值不会提升

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>
        //把变量声明提升到函数的顶部,但是变量赋值不会变
        // console.log(a)
        // var a = 10
        // 输出undefined

        //与上例等价
        var a;
        console.log(a)
        a = 10
        //也输出undefined
    </script>
</body>
</html>
```

 注意：变量未声明，直接使用，输出‘变量 is not defined’。





#### 函数提升

函数提升会将函数声明连带定义一起提升

在js中函数有三种创建方式：函数声明，函数表达式（函数字面量），函数构造法（动态的）

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        test1();
        function test1(){
            console.log("可以被提升")
        }

        test2();
        var test2 = function(){
            console.log("不可以被提升")
        }

        console.log("不可以被提升")
        var test2 = function(){
            console.log("不可以被提升")
        }
    </script>
</head>
<body>
    
</body>
</html>
```

```js
//函数和变量一起提升
console.log(test3());
        function test3(){
            console.log('func');
            return 5;
        }
        var test3 = 'army'
```



### 对象的创造方法

1. 通过new运算符创建      var p = new Object();

   ```js
           var people = new Object();
           people.name = "zhangsan"
           people.age = 18
           people.eat = function(){
               console.log('xiagnjiao')
           }
           console.log(people)
   
   ```

2. new 关键字可以省略

   ```js
           var people = {};
           people.name = "lisi"
           people.sex = "男"
           people.age = function(){
               console.log(18)
           }
           console.log(people)
   
   ```

3. 通过构造函数创建

   ```js
           function Foo(name,age,sex){
               this.name = name;
               this.age = age;
               this.sex = sex;
           }
           var zs = new Foo("张三" , 18 , "男")
           console.log(zs)
   ```

4. 创建对象直接赋值

   ```js
           var p = {
               name :"张三",
               age : 18,
               sex : "男"
           }
           var p = new Object({
               name : "张三",
               age : 19,
               sex: "男",
               eat : function(){
                   console.log("香蕉")
               }
           })
           console.log(p)
   
   ```



补充：

**构造函数中的 this 代表的是当前的对象**

这样的话就会有一个缺点，每创建一个方法都会占用一些内存，所以js给构造函数设计一个prototype属性，用来存放对象的方法

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <script>
        function Student(name, age, id) {
            this.name = name;
            this.age = age;
            this.id = id;
        }
        Student.prototype = {
            work: function (skill) {
                alert(this.name + "做" + skill + "开发相关的工作");
            },
            classId: "Java1班"
        }
        var stu1 = new Student("李明", 18, 20221515);//得到的就是字面量对象
        var stu2 = new Student("王磊", 18, 20231000);//得到的就是字面量对象
        console.log(stu2.work == stu1.work);//true，节省了内存空间
        stu1.work("Java");
        stu2.work("PHP");
        console.log(stu1.classId);//20151515
        console.log(stu2.classId);//20141000
    </script>
</body>

</html>
```





### 对象的使用方法

对象属性的使用：

1. 可以用点符号访问对象属性值
2. 也可以通过数组的方式，即用【"属性名称"】

对象方法的使用：

​	可以使用对象名 . 方法名（）来调用





## js的内置对象

### Array 构造函数

```js
//new关键字创建空数组
var arr = new Array();
//new关键字创建包含元素的数组
var arr = new Array(值1,值2.....值N);
//new关键字创建指定元素个数的数组
var arr = new Array(数值);
//也可以使用[]直接创建数组
var arr = [];
var arr = [值1,值2.....值N];
//可以使用length属性获取数组的长度;并且可以给一个数组长度赋值。
```



### Array对象方法

程序运行时通常需要读取数组中的数据，有时需要对数据进行修改

1. 读取数据：可以使用索引查询和添加数组元素

   ```js
           var arr = [34,89,99,24,11,89,99,24,11,89,99,24,11,89,99,24,11,89,99,24,11]
           // 查
           // 查最后一个
           console.log(arr[arr.length-1])
   ```

2. 添加数据：使用push（） 方法将新元素添加到数组尾部

   ```js
           //增  push()
           // 添加到末尾
           var arr10 = [1,2,3,4,5,6,7,8,9,0]
           arr.push('hello')
           console.log(arr10)
   ```

3. 删除数据：可以使用 delete（） 运算符删除指定的元素

   ```js
           // 删除  delete 要删除的元素
           var arr1 = [1,2,3,4,5]
           delete arr1[4]
           console.log(arr1)
   ```

4. 删除末尾元素(更新数据) : pop()方法,该方法会返回删除的元素。

   ```js
           // 删除末尾元素  arr.pop()
           var arr2 = [1,2,3,4,5]
           arr2.pop()
           console.log(arr2
   ```

5. 删除顶端的元素 : shift()方法

   ```js
           // 删除开头的元素  shift()
           var arr3 = [1,2,3,4,5]
           arr3.shift()
           console.log(arr3)
   ```

6. 在数组顶端添加元素 : unshift()方法,返回值为新数组的长度

   ```js
           var arr3 = [1,2,3,4,5]
           arr3.unshift('nihao')
           console.log(arr3)
   ```

7. 字符转换：toString()方法将数组表示为字符串

   ```js
           var arr = [34,89,99,24,11,89,99,24,11,89,99,24,11,89,99,24,11,89,99,24,11]
           var str1 = arr.join('')
           console.log(str1)
   ```

8. 数组逆序reverse()：颠倒数组元素的顺序;返回值为逆序后的新数组

   ```js
   let arr9 = [1, 2, 3, 4, 5];
   let reversedArr = arr9.reverse();
   console.log("逆序后的数组：", reversedArr);
   ```

10. 数组排序 sort：

    ```js
    语法 数组名.sort(sortfunction)
    sortfunction若省略，默认为从按照ASII字符顺序进行升序排列
    sortfunction必须返回：正值、零、负值三者之一。正直表示第一个值大于第二个值，负值反
    之，零则相等。
    var arr1 = [72,33,12,44,24];
    arr1.sort(function(a,b){return a-b;});
    alert(arr1);
    var arr1 = [72,33,12,44,24];
    arr1.sort(function(a,b){return b-a;});
    alert(arr1);
    ```

11. 扩充数组 concat:将多个数组的元素合并为一个新的数组。

    ```js
    let arr1 = [1, 2, 3];
    let arr2 = [4, 5, 6];
    let arr3 = [7, 8, 9];
    
    let combinedArray = arr1.concat(arr2, arr3);
    console.log("合并后的新数组：", combinedArray);
    ```

12. splice方法：删除、替换、插入元素,会更改原数组

    第一参数为起始位置索引

    第二参数为切取元素个数

    第三个参数为插入元素，可选项

    ```js
    // 删除元素示例
    let arr4 = [1, 2, 3, 4, 5];
    // 从索引 2 开始删除 2 个元素
    let removedElements1 = arr4.splice(2, 2);
    console.log("删除元素后的数组：", arr4);
    console.log("删除的元素：", removedElements1);
    // 替换元素示例
    let arr5 = [1, 2, 3, 4, 5];
    // 从索引 1 开始删除 2 个元素，并插入 6 和 7
    let removedElements2 = arr5.splice(1, 2, 6, 7);
    console.log("替换元素后的数组：", arr5);
    console.log("被替换掉的元素：", removedElements2);
    // 插入元素示例
    let arr6 = [1, 2, 3];
    // 从索引 1 开始删除 0 个元素，并插入 4 和 5
    let removedElements3 = arr6.splice(1, 0, 4, 5);
    console.log("插入元素后的数组：", arr6);
    console.log("被删除的元素（这里没有删除，所以为空数组）：", removedElements3);
    ```

13. 切取数组的一段元素 slice：

    切取部分作为新数组返回，不会对原数组改变。

    第一参数为起始位置索引(包含)

    第二参数为结束位置索引，注意区分splice(不包含)

    若省略第二个参数则直接切取到结尾

    ```js
    let arr7 = [1, 2, 3, 4, 5];
    // 从索引 1 开始，到索引 3 结束（不包含索引 3 的元素）进行切片
    let slicedArray = arr7.slice(1, 3);
    console.log("切取的数组片段：", slicedArray);
    console.log("原数组不受影响：", arr7);
    ```

    

### Date 对象

Date是JavaScript的内置对象，系统在Date对象中封装了与日期和时间相关的属性和方法。

 Date使用UTC1970年1月1日0时开始经过的毫秒数来存储时间。



### Date构造函数

```js
var date= new Date();
无参数的情况下返回值为当前时间。
不同浏览器显示的时间格式会有细微差异
var date = new Date(milliseconds);
参数为毫秒值
var date = new Date(dateString);
参数为日期字符串
var date = new Date(year, month, day, hours, minutes, seconds,
milliseconds);
必选值:year, month, day；
```





### Date对象方法

**getDate()** **从** **Date** **对象返回一个月中的某一天** **(1 ~ 31)**。

**getDay()** **从** **Date** **对象返回一周中的某一天** **(0 ~ 6)**。

**getFullYear()** **从** **Date** **对象以四位数字返回年份。**

**getHours()** **返回** **Date** **对象的小时** **(0 ~ 23)****。**

getMilliseconds() 返回 Date 对象的毫秒(0 ~ 999)。

**getMinutes()** **返回** **Date** **对象的分钟** **(0 ~ 59)****。**

**getMonth()** **从** **Date** **对象返回月份** **(0 ~ 11)****。**

**getSeconds()** **返回** **Date** **对象的秒数** **(0 ~ 59)****。**

**getTime()** **返回** **1970** **年** **1** **月** **1** **日至今的毫秒数。**

setDate() 设置 Date 对象中月的某一天 (1 ~ 31)。

setFullYear() 设置 Date 对象中的年份（四位数字）。

setHours() 设置 Date 对象中的小时 (0 ~ 23)。

setMilliseconds() 设置 Date 对象中的毫秒 (0 ~ 999)。

setMinutes() 设置 Date 对象中的分钟 (0 ~ 59)。

setMonth() 设置 Date 对象中月份 (0 ~ 11)。

setSeconds() 设置 Date 对象中的秒钟 (0 ~ 59)。

setTime() setTime() 方法以毫秒设置 Date 对象。

```js
// 创建一个 Date 对象
let currentDate = new Date();
// 获取日期信息
console.log("当前日期是一个月中的第几天: ", currentDate.getDate());
console.log("当前日期是一周中的第几天: ", currentDate.getDay());
console.log("当前日期所在的年份: ", currentDate.getFullYear());
console.log("当前时间的小时数: ", currentDate.getHours());
console.log("当前时间的毫秒数: ", currentDate.getMilliseconds());
console.log("当前时间的分钟数: ", currentDate.getMinutes());
console.log("当前日期所在的月份（注意：0 表示一月）: ", currentDate.getMonth());
console.log("当前时间的秒数: ", currentDate.getSeconds());
console.log("从 1970 年 1 月 1 日至今的毫秒数: ", currentDate.getTime());
// 设置日期信息
// 设置日期为该月的第 15 天
currentDate.setDate(15);
// 设置年份为 2026
currentDate.setFullYear(2026);
// 设置小时数为 14
currentDate.setHours(14);
// 设置毫秒数为 500
currentDate.setMilliseconds(500);
// 设置分钟数为 30
currentDate.setMinutes(30);
// 设置月份为 5（注意：这里 5 表示六月）
currentDate.setMonth(5);
// 设置秒数为 20
currentDate.setSeconds(20);
// 设置从 1970 年 1 月 1 日起的毫秒数
let newTime = Date.UTC(2026, 5, 15, 14, 30, 20, 500);
currentDate.setTime(newTime);
// 输出设置后的日期信息
console.log("\n设置后的日期信息:");
console.log("日期是一个月中的第几天: ", currentDate.getDate());
console.log("日期是一周中的第几天: ", currentDate.getDay());
console.log("日期所在的年份: ", currentDate.getFullYear());
console.log("时间的小时数: ", currentDate.getHours());
console.log("时间的毫秒数: ", currentDate.getMilliseconds());
console.log("时间的分钟数: ", currentDate.getMinutes());
console.log("日期所在的月份（注意：0 表示一月）: ", currentDate.getMonth());
console.log("时间的秒数: ", currentDate.getSeconds());
console.log("从 1970 年 1 月 1 日至今的毫秒数: ", currentDate.getTime());
```



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <script>
        // var date = new Date();
        // console.log(date)

        // var date1 = new Date('2013 16:28:18')
        // console.log(date1)
        
        // // 2025年3月20日
        // var date = new Date(' 2025年3月20日')
        // console.log(date)

        function addZero(num){
    return num < 10 ? '0'+ num : num
  }

  function formatDate(dates){
      let date = new Date(dates) // 创建日期对象
      // 年
      let year = date.getFullYear()
      // 月份
      let month = addZero(date.getMonth() + 1)
      // 日 
      let day = addZero(date.getDate())
      // 小时
      let h = addZero(date.getHours())

      // 分钟
      let m = addZero(date.getMinutes())

      // 秒
      let s = addZero(date.getSeconds())

      let w = date.getDay()

      let ws = ['星期日','星期一','星期二','星期三','星期四','星期五','星期六']

      return `${year}年${month}月${day}日  ${h}时${m}分${s}秒  ${ws[w]}`
  }

  console.log(formatDate('2023-12-26 09:57:11'))



    </script>
</head>
<body>
    
</body>
</html>
```









## js DOM编程（文档对象模型）（动态）

用来操作页面上的元素  ：

1.给一个页面动态操作

2.点击一下会产生什么样的效果





**DOM是这样规定的：**

整个文档是一个文档节点；

每个HTML标签是一个元素节点；

包含在HTML元素中的文本时文本节点；

每一个HTML属性是一个属性节点；

注释属于注释节点。





### js获取HTML标签元素

#### 特殊：

**1.  querySelector**

通过型获取页面元素，获取的是**一个**（重要！！）

//在页面只获取一个

```js
        const divbox = document.querySelector('.box')  //在class上获取  就一个
        console.log(divbox)

        const li = document.querySelector('li')  //在li上获取  就一个
        console.log(li)
```



**2..querySelectorAll**

在页面中获取想要获取的**所有**内容

```js
        const lis = document.querySelectorAll('li')   //在li上获取  全部的！！
        console.log(lis)
```





#### 一般

| 元素                     | 说明                                                         |
| ------------------------ | ------------------------------------------------------------ |
| getElementById()         | 返回对拥有指定**id**的第一个对象的引用，返回值Element。具有**唯一性** ：不能同时给两个或两个以上的元素节点返回该元素，如果不存在，则返回null |
| getElementsByClassName() | 返回文档中所有指定类名的元素集合，作为 NodeList 对象参数为String,需要获取的元素类名,多个类名使用空格分隔(尽量不用) |
| getElementsByName(）     | 返回带有**指定名称**的对象集合，返回值NodeList/HTMLCollection。在同一个网页上，该属性并**不要求唯一性**，相同的name可以出现在多个标签上 |
| getElementsByTagName()   | 返回带有**指定标签名**的对象集合，返回值NodeList/HTMLCollection。将返回一个元素节点的对象，这个对象保存着所有相同元素名的节点列表 |
| getElementsByTagNameNS() |                                                              |

**getElementsByName(）****

```js
document.getElementsByName('goods') //获取属性name的值为goods的所有元素
document.getElementsByName('goods')[0]//获取属性name的值为goods的第一个元素
document.getElementsByName('goods')[1]//获取属性name的值为goods的第二个元素
```



**getElementsByTagName**()

```js
document.getElementsByTagName('*'); //获取所有元素
document.getElementsByTagName('li'); //获取所有li 元素
document.getElementsByTagName('li')[0]; //获取第一个li元素
document.getElementsByTagName('li').length; //获取所有li元素的数目
```



**:该方法不仅可以通过document对象调用，还可以通过元素节点Element来访问****



```js
        // getElementById()  
        const divBox = document.getElementById('box')
        console.log(divBox)
        // getElementsByName()   可以获取相同名称(name)元素，返回一个元素节点的列表
        const goods = document.getElementsByName('good') //获取的是一个集合
        console.log(goods)
        // getElementsByTagName()  通配符获取所有元素
        const allNode = document.getElementsByTagName('*')
        console.log(allNode)
        // getElementsByClassName()   根据class获取元素，获取到的结果是一个集合
        const boxNode = document.getElementsByClassName('box')
        console.log(boxNode)
        // 
```





### 深度解析document.write（）:

这是用文档写HTML和JS的代码，会在页面中显示出来；

温馨提示：文档加载之后使用docunment.write()会覆盖原文档.

除了直接输出文字外，它还支持带有HTML标签的输出内容。

比如直接输出一个标题

比如在输出内容中加入br换行标签

比如直接输出列表...... ； 

注意事项:

绝对不要在文档加载完成之后使用 document.write()。这会覆盖该文档。









### **JavaScript**操作标签元素的内容

**element.innerHTML**     设置或返回元素的内容。

注:可以设置内容的时候加上标签，设置的标签会被浏览器解析

**element.innerText**    设置或返回元素的文本内容

 **element.tagName**    返回元素的标签名。



#### innerText 和 innerHTML 的区别：

innerText 只能获取到文本内容，标签不会被获取 ，设置的内容会被浏览器认为是纯文本； 

innerHTML可以获取到所有的内容，包含标签，设置的内容会被浏览器认为是HTML内容，如果存在标签会被解析









### js操作标签属性

#### 1. HTML基本属性操作

**element.属性名**          设置或返回元素的指定属性。

 **element.className**        设置或返回元素的 class 属性。

注:class属性的操作必须使用className

注:Element对象使用 . 可以调用对象的各个属性





#### 2.  HTML方法操作属性

**element.getAttribute（）     返回元素节点的指定属性值**

​      getAttribute()方法将获取元素中某个属性的值，它和直接使用.属性获取属性值的方法有一定区别。

```js
document.getElementById('box').getAttribute('id');//获取元素的id 值
document.getElementById('box').id; //获取元素的id 值
document.getElementById('box').getAttribute('mydiv');//获取元素的自定义属性值
document.getElementById('box').mydiv //获取元素的自定义属性值，非IE 不支持
document.getElementById('box').getAttribute('class');//获取元素的class 值
```

**element.setArrtribute（）          把指定属性设置或更改为指定值**

​         setAttribute()方法将设置元素中某个属性和值。它需要接受两个参数：属性**名**和**值**。如果属性本身已存在，那么就会被覆盖。

```js
document.getElementById('box').setAttribute('align','center');//设置属性和值
document.getElementById('box').setAttribute('bbb','ccc');//设置自定义的属性和值
```

**element.setArrtribute ()          从元素中移除指定属性**

​            element.setArrtribute ()    可以移除HTML属性

```js
document.getElementById('box').removeAttribute('style');//移除属性
```

 

注:使用属性只能来获取和设置的是元素对象原始属性;使用方法可以用来设置元素对象自定义的属性;







### js  Document 对象属性一览

document可以通过一下属性可以查询指定属性值或给指定属性赋值

**语法**

document.属性名      获取属性值

document.属性名 = 值      给指定属性设置值

**常用**

**document.title //****设置或读取文档标题等价于HTML**的 <title> **标签**

document.bgColor //设置或获取页面背景色

document.fgColor //设置或获取前景色(文本颜色)

document.linkColor //设置或获取未点击过的链接颜色

document.alinkColor //设置或获取激活链接(焦点在此链接上)的颜色

document.vlinkColor //设置或获取已点击过的链接颜色

**document.cookie //设置和读出cookie**

document.URL //返回当前文档的 URL

**document.images //获取页面上的<img>标签**

images集合(页面中的图象)：可以使用指定的元素访问其各个属性



 注:HTMLCollection 是一个集合，表示 HTML 元素的集合，它提供了可以遍历列表的方法和属性。

 HTML DOM 中的 HTMLCollection 是“活”的；如果基本的文档改变时，那些改变通过所有HTMLCollection 对象会立即显示出来。

 HTMLCollection 对象是只读的，不能给它添加新元素，即使采用 JavaScript 数组语法也是如此。

 HTMLCollection 对象和 NodeList 对象很相似

```js
document.images.length //对应页面上<img>标签的个数
document.images[0] //第1个<img>标签
document.images.item(2) //第3个<img>标签
```









### js的层次节点

节点最常见的类型有**元素节点**，**注释节点**，和**文本节点**

节点的层次结构可以划分为：父节点与子节点、兄弟节点这两种，**当我们获取其中一个元素节点的时候，就可以使用层次节点来获取它相关的层次节点**

```js
<div id="div1">
	<p>我是div中的p段落</p>  <!--空白节点-->
	<!--我是页面中的注释-->
	<div>我是div1中的子div</div>  <!--空白节点-->
	我是div的纯文本内容
	<h2>我是div中的h2标题标签</h2>  <!--空白节点-->
</div>
```

一共有7个节点

childNodes 用于获取当前元素节点的所有子节点。因为浏览器会把节点之间的空白符当作文本结点处理。





### 获取层次节点

firstChild   获取当前元素节点的第一个子节点







## BOM编程

针对window对象，它能够进行数据的本地存储



### window对象

window对象时BOM对象的顶级对象 所有的对象都是由window对象延伸出来的

**Window** **对象表示一个浏览器窗口或一个框架**。在客户端 JavaScript 中Window 对象是全局对象，所有的表达式都在当前的环境中计算。也就是说，要引用当前窗口根本不需要特殊的语法，可以把那个窗口的属性作为全局变量来使用。例如，可以只写document，而不必写 window.document。

 同样，可以把当前窗口对象的方法当作函数来使用，如只写 alert()，而不必写 Window.alert()。

**示例：**

 document.write("www.oxlok.top");

 window.document.write("www.oxlok.top");

 也就是说调用window对象的属性或方法可以省略window。





### 三种弹出框（******）

**1.alert:显示带有一段消息和一个确认按钮的警告框**

```js
<script>
	alert("带一条消息和确定按钮的弹出框");
</script>
```



**2.confirm（）：显示带有一段消息以及确认按钮和取消按钮的对话框，返回值为布尔型；如果确定则返回true 点击取消返回false**

```js
    <script>
        confirm("带有一段消息以及确认按钮和取消按钮的对话框")
    </script>
```



**3.prompt(): 显示可以提示用户输入的对话框，第一个参数是提示，第二个参数是默认值，取消返回null，需要注意的是，返回的输入值是一个string类型的数据**

```js
<script>
	prompt("请输入您的姓名:"，”例如:张三”);
</script>
```





### 窗体控制：

##### open（）:  打开一个窗体

语法:window.open(URL,name,[specs]),该方法返回打开窗口的引用

参数介绍:

​		URL	 可选。打开指定的页面的URL。如果没有指定URL，打开与新的空白窗口

​		name		 可选。指定窗口的名称

可选。指定target属性或窗口的名称。支持以下值：

_blank - URL	加载到一个新的窗口。这是默认

_parent - URL	加载到父框架

_self - URL	替换当前页面

_top - URL	替换任何可加载的框架集

name - 窗口名称

​		specs 一个逗号分隔的项目列表。支持以下值：

​						height=pixels 窗口的高度。最小.值为100

​						left=pixels 该窗口距离屏幕左侧的位置

​						top=pixels 该窗口距离屏幕顶部的位置

​						width=pixels 窗口的宽度.最小.值为100

```js
    <script>
        //open 打开一个窗体
        window.open("https://draw.olxok.top","_blank","width=520,height=420,left=100,top=30")
    </script>

```

![image-20250327201743386](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250327201743386.png)





##### close（）:  关闭浏览器窗口

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <button>关闭</button>
    <button onclick="history.back()">返回</button>
    <!--  go(1) 是返回上一级  -->
    <button onclick="history.go(1)">返回1</button>

    
    
    <script>
        //.onclick：这是一个事件处理器属性，它指定了当按钮被点击时要执行的函数。
        document.querySelector('button').onclick=function(){
            window.close() //关闭窗口
        }
        console.log(history.length)
    </script>
</body>
</html>
```







### 窗口滚动

**1.scrollBy(xnum,ynum)**：按照指定的像素值来滚动内容

​			xnum 把文档向右滚动的像素数。

​			ynum 把文档向下滚动的像素数。

```js
document.querySelector('button').onclick = scrollWindow
<script type="text/javascript">
		function scrollWindow() {
		window.scrollBy(30,30)
	}
</script>
```



**2**、**scrollTo(xpos,ypos)**：把内容滚动到指定的坐标。

​			xpos 要在窗口文档显示区左上角显示的文档的 x 坐标。

​			ypos 要在窗口文档显示区左上角显示的文档的 y 坐标。

```js
<script type="text/javascript">
		function scrollWindow() {
		window.scrollTo(0,0)
	}
</script>
```







### 窗体打印

**print():   打印当前窗口的内容**

调用 print() 方法所引发的行为就像用户单击浏览器的打印按钮。通常，这会产生一个对话框，让用户可以取消或定制打印请求。





**案例：滚动   回到顶部    打印 的按钮案例**

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        div {
            height: 2000px;
            width: 3000px;
        }

        button {
            position: fixed;
        }

        .top {
            left: 200px;
        }

        .print {
            left: 250px;
        }
    </style>
</head>

<body>
    <button>滚动</button>
    <button class="top">回到顶部</button>
    <button class="print">打印</button>
    <div></div>

    <script>
        const btn = document.querySelectorAll('button')[0]
        const btn1 = document.querySelectorAll('button')[1]
        //尝试为第一个按钮元素设置点击事件处理器
        btn.onclick = scrollWindow
        function scrollWindow(){
            window.scrollBy(0,30)
        }

        //尝试为第二个按钮元素设置点击事件处理器
        btn1.onclick = scrollWindow1
        function scrollWindow1(){
            window.scrollTo(0,0)
        }

        //打印
        document.querySelector('.print').onclick = function(){
            window.print()
        }
    </script>
</body>

</html>
```









### 定时器

处理时间和间隔的函数：

**setTimeout() 函数**   

**clearTimeout()函数**

**setInterval()**

**clearInterval()**



#### 延时定时器

setTimeout()：定义延时定时器,在指定的时间后调用函数

 ```html
 <!DOCTYPE html>
 <html lang="en">
 <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>Document</title>
 </head>
 <body>
     <script>
         setTimeout(function(){
             document.write("隔3秒后触发")
         },3000)
 
         setTimeout(fun1,5000)  //在5秒后触发
 
         function fun1(){
             document.write("函数名的方式5秒后触发")
         }
     </script>
 </body>
 </html>
 ```



#### 间隔定时器

setInterval():   定义间隔型定时器，在间隔指定的事件后重复调用函数

**语法：**

​		setInterval(fun1,time)　　

fun：函数体或函数名，time指定的时间，单位为毫秒。会返回一个值id。

​		

​		clearInterval(id)：清除间隔型定时器

参数id是setInterval()函数返回的值，根据这个值可以停止返回值为idsetInterval()的执行。

```js
var h = setInterval(function () {
	document.write("3秒输出一次<br/>");
}, 3000);
```

注意，JavaScript是单线程的，因此，这个定时函数实际上是通过插入执行队列的方式来实现。







#### 动态时间效果

由于涉及到时间的显示问题，所以要用到日期对象Date，还有时间在不停的走，因此需要不断的调用函数，所以要用到Windows的定时器setInterval()方法

```js
<script>
	function disptime(){
	var today = new Date(); //获得当前时间
	var hh = today.getHours(); //获得小时、分钟、秒
	var mm = today.getMinutes();
	var ss = today.getSeconds();
		document.getElementById("myclock").innerHTML=hh+":"+mm+":"+ss;
}
window.setInterval(disptime,1000);
</script>
```



案例：倒计时

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <button>重新提交</button>


    <!-- 
        1.按钮可以点击，点击后锁定
        2.锁定的时候，设计倒计时，到0之前都是锁定状态
        3.按钮上文字变成'重新提交(xs)'
        4.倒计时结束后，又变回原样
        5.重新点击发送按钮，效果和第一步一样
     -->
    <script>
        const btn = document.querySelector('button')
        const countTime = 10     //设计倒计时的时间

        btn.onclick = function(){
            //设计倒计时
            let time = countTime
            //设置按钮为禁止点击锁定状态
            this.disabled = true
            //设置定时器，1秒执行一次
            var timer = setInterval(() =>{
                time--
                //设置按钮为点击状态
                time.texyContent = `重新提交(${time}s)`
                //判断time倒计时是否等于0，如果等于0，代表倒计时结束
                if(time == 0){
                    //设置按钮为可点击状态
                    this.disabled = false
                    //设置按钮文字为'重新提交'
                    this.textContent = `重新提交`
                    //清除定时器
                    clearTimeout(timer)
                }else{
                    //如果time不等于0，代表倒计时还没有结束
                    this.textContent = `重新提交(${time})`
                }
            },1000)
        }
    </script>
</body>
</html>
```





注意：定时器中有一个时异步任务和同步任务  一般是要等同步任务全部完成后在做异步任务









### window对象常用属性（******）

​		innerWidth  返回窗口的文档显示区的宽度

​		innerHeight    返回窗口的文档显示区的高度

​		name   设置或返回窗口的名称

​		outerheight   返回窗口的外部高度

​		outerwight    返回窗口的外部宽度

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>
        console.log('宽',window.innerWidth)
        console.log('高',window.innerHeight)
        window.name = '好好好'
        console.log(window.name)
        console.log(window.outerHeight)
        console.log(window.outerWidth)
    </script>
</body>
</html>
```







### History对象

History 对象包含用户（在浏览器窗口中）访问过的 URL。

History 对象是 window 对象的一部分，可通过 window.history 属性对其进行访问。



#### History对象属性

| 属性   | 说明                           |
| ------ | ------------------------------ |
| length | 返回当前窗口历史列表中的网址数 |



#### History对象方法

| 方法      | 说明                              |
| --------- | --------------------------------- |
| back()    | 加载history列表中的前一个URL      |
| forward() | 加载history列表中的下一个URL      |
| go(num)   | 加载 history 列表中的某个具体页面 |

History对象：back() 方法

​	 back() 方法可加载历史列表中的前一个 URL（如果存在）。

​	调用该方法的效果等价于点击后退按钮或调用 **history.go(-1)**。

History对象：forward() 方法

​	 forward() 方法可加载历史列表中的下一个 URL。

​	调用该方法的效果等价于点击前进按钮或调用 **history.go(1)**。

History对象：go() 方法

 	go() 方法可加载历史列表中的某个具体的页面。

​	该参数可以是数字，使用的是要访问的 URL 在 History 的 URL 列表中的相对位置。（**-1上一个页面，1前进一个页面**)。或一个字符串，字符串必须是局部或完整的URL，该函数会去匹配字符串的第一个URL。

​	history.go(number|URL)



像是跳转和后退页面

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <a href="./window属性.html">跳转</a>
    <button onclick="history.go(-1)">后退</button>

    <script>
        setTimeout(() =>{
            //访问当前的url的地址数量
            console.log(history.length)
            window.location.href = 'window属性.html'
        },2000)
    </script>
</body>
</html>
```









### location对象

Location 对象包含有关当前 URL 的信息。

Location 对象是 window 对象的一部分，可通过 window.location 属性对其进行访问。



#### location对象属性

| 属性     | 说明                          |
| -------- | ----------------------------- |
| hash     | 返回一个URL的锚部分（锚点）   |
| host     | 返回一个URL的主机名和端口     |
| hostname | 返回URL的主机名               |
| href     | 返回完整的URL                 |
| pathname | 返回的URL路径名               |
| port     | 返回一个URL服务器使用的端口号 |
| protocol | 返回一个URL的协议             |
| search   | 返回一个URL的查询部分？之后   |

#### location对象方法

| 方法      | 说明                                           |
| --------- | ---------------------------------------------- |
| assign()  | 载入一个新的文档 location.assign(URL)          |
| reload()  | 重新载入当前文档location.reload();             |
| replace() | 用新的文档替换当前文档location.replace(newURL) |

​		**window.location.assign(url)** ： 加载 URL 指定的新的 HTML 文档。就相当于一个链接，跳转到指定的url，当前页面会转为新页面内容，可以点击后退返回上一个页面。

​		**window.location.replace(url)** ： 通过加载 URL 指定的文档来替换当前文档，这个方法是替换当前窗口页面，前后两个页面共用一个窗口，所以是没有后退返回上一页的

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <button onclick="func()">按钮</button>

    <script>
        console.log(location)

        // location.href = 'https://www.olxok.top'
        // location.assign('https://www.olxok.top')      //打开新网页
        function func(){
            location.reload()  //刷新当前网页
        }

        console.log(navigator.userAgent)
    </script>
</body>
</html>
```









### Screen 对象

screen 对象包含有关客观端显示屏幕的信息

| 属性        | 说明                                     |
| ----------- | ---------------------------------------- |
| availHeight | 返回屏幕的高度（不包括Windows任务栏）    |
| availWidth  | 返回屏幕的宽度（不包括Windows任务栏）    |
| colorDepth  | 返回目标设备或缓冲器上的调色板的比特深度 |
| height      | 返回屏幕的总高度                         |
| pixelDepth  | 返回屏幕的颜色分辨率（每像素的位数）     |
| width       | 返回屏幕的总宽度                         |







### **Navigator** 对象

| 属性          | 说明                                                         |
| ------------- | ------------------------------------------------------------ |
| appCodeName   | 返回浏览器的代码名appCodeName 属性是一个只读字符串，声明了浏览器的代码名。在所有以 Netscape 代码为基础的浏览器中，它的值是 "Mozilla"。为了兼容起见，在 Microsoft 的浏览器中，它的值也是 "Mozilla"。 |
| appName       | 返回浏览器的名称                                             |
| appVersion    | 返回浏览器的平台和版本信息                                   |
| cookieEnabled | 返回指明浏览器中是否启用 cookie 的布尔值                     |
| platform      | 返回运行浏览器的操作系统平台                                 |
| userAgent     | 返回由客户机发送服务器的user-agent 头部的值                  |

**说明：**

 1.navigator.appCodeName：IE/Firefox/Chrome 系列浏览器中，它的值都是"Mozilla"。

 2.navigator.appName：IE/Firefox/Chrome 系列浏览器中 均为 Netscape。











fetch api

promise

es6 这是书
