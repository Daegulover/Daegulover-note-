# MySQL 数据库

sql 是不区分大小写的

### 注释：

 	- --1.DDL操作之数据库操作
 	-  # 也行



----------------------

## 对数据库的修改

### show databases;

查看所有数据库



### 创建数据库

create database 文件名 ;

create database if not EXTSTS 文件名 ；          （不存在的文件）



### 选择使用哪一个数据库

use mudb1 ;



### 删数据库

drop database mydb1 ； （不管有没有都要删）

drop database if exists mydb1 ；   (这个数据库存在就删，不存在就不删)



### 修改数据库编码

alter database 文件名 character set 修改后的文件名





-- 1. **查询所有数据库**
show DATABASE ;

-- 2. **创建数据库**
create database if not exists `mysql 03` ;

-- 3. **选择使用哪一个数据库**
use `mysql 01`;

-- 4. **删除数据库**
drop database `mysql 01`;
drop database if exists `mysql 01`;

-- 5.**修改数据库的编码**
alter database `mysql 03` character set user01 ;









## 在数据库中创建表

### 增 删 查 改

 1.查询

​		select * from 文件名

  2.删除

​		insert into 文件名 (表头)  values(添加的东西)

   3.修改

​		update 文件名 set 修改的东西 = '修改的值'  where 地址 = '地址'

​	4.删除

​		delete from 文件名 where 地址 = '地址'

5. 添加

    alter table 表名 add 字段名 类型（长度）[comment注释] [约束] ；

   ![image-20250407175741021](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250407175741021.png)

     ![image-20250407174957894](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250407174957894.png)

![image-20250402171825480](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250402171825480.png)







### DDL表操作

#### 查询

1. 查询当前数据库所有表

   show table ;

2. 查询表结构

   desc 表名 ;

3. 查询指定表的建表语句

   show create table 表名 ;



#### 创建

CREATE TABLE 表名(
	字段 1 类型 [注释] ,
	字段 2 类型 [注释] ,
	字段 3 类型 [注释] ,
	字段 4 类型 [注释] ,
	...
	字段 n 类型 [注释] 
)[表注释] ;

![image-20250409143512456](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250409143512456.png)





### 数据类型

MySQL中的数据类型有很多，主要分为三类：数值类型、字符串类型、日期时间类型

##### 数值类型

![image-20250407164345074](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250407164345074.png)



##### 字符串类型

![image-20250407164835810](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250407164835810.png)



##### 日期类型

![image-20250407164956164](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250407164956164.png)





**案例：根据需求创建表**

​		一下是信息表的需求：

![image-20250407165130162](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250407165130162.png)



//先要选择一个数据库，才能执行下一个任务

USE `Songyue 1` ;      

CREATE TABLE emp (
    id INT COMMENT '编号', 
    worknumber VARCHAR(10) COMMENT '工号',
    name VARCHAR(10) COMMENT '姓名',
    sex CHAR(1) COMMENT '性别',
    age TINYINT UNSIGNED COMMENT '年龄',
    idcard CHAR(18) COMMENT '身份证号',
    entrydate DATE COMMENT '入职时间'
) COMMENT = '员工表';



注意：注意中英文符号 





## 查询

### 条件查询

![image-20250409144052452](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250409144052452.png)

```mysql
-- 条件查询
SELECT id,name,sex
FROM `candy 01-01`
WHERE `candy 01-01`.id  IN
(
SELECT id FROM `candy 01-01` WHERE age >20
)
```

在` candy 01-01 `中查询年龄大于20的

* 根据这个表，查询没有成绩的学生

![image-20250409151245602](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250409151245602.png)

```mysql
-- 查询没有成绩的学生
select * from `candy 01-02` where score is null 
```

![image-20250409151407962](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250409151407962.png)





### 分组查询

```mysql
SELECT id
FROM `candy 01-01`
WHERE age >20
GROUP BY id
HAVING COUNT(sex)>=3
```





### 简单查询

但是这个是带有排序的

```mysql
SELECT *
FROM `candy 01-01`
ORDER BY age asc
```







## mysql 的字符串类

```mysql
-- 1.concat(): 连接字符串
SELECT concat(sname,'(',ssex,')')  学生信息from `candy 01-01`

-- 2.UPPER(): / LOWER():  转换为大写或小写
SELECT UPPER(age) upper_name from sex
SELECT LOWER(age) upper_name from sex

-- 3.SUBSTRING（）：截取子字符串
select id , SUBSTRING(id,1,5) as short_name from sex
-- 用户的基本信息中截取有用的信息，例如：身份证号后6位

-- 4.REPLACE(): 替换字符串中的部分内容
SELECT replace (name,'ff','zr') as replace_name from `candy 01-01`

-- 5.LENGTH(): 返回字符串的长度
select name,LENGTH(name) as 长度 from `candy 01-01`
```

![image-20250409150604295](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250409150604295.png)

* 根据这个表格来的









## 数学类函数

#### -- ABS(): 返回绝对值

```mysql
SELECT ABS(-10) as abs_value   -- 一般用在数学计算上，例如：求两个日期相差多少天
```



#### -- ROUND（）： 四舍五入

```mysql
SELECT round(23.66) as round_value  -- 在精度不高的计算中
```



#### -- MOD(): 求余数

```mysql
SELECT mod(19,3) as mod_value
```



#### -- CELL() / FLOOR(): 向上取整/向下取整

```mysql
SELECT cell(4.34) as 向上取整
SELECT floor(8.34) as 向下取整
```



#### -- POWER(): 幂运算

```mysql
select power(23,2) as v1
SELECT power(3,2) as v2
```









## 聚合函数类

#### -- SUM(): 求和

```mysql
SELECT sum(age) as total_age from `candy 01-02`
```



#### -- AVG(): 平均值

```mysql
SELECT avg(score) as avg_score from `candy 01-02`
```



#### -- MAX() / MIN() :求最大值 /最小值

```mysql
SELECT max(score),min(score) from `candy 01-02`
```









## 日期和时间类函数

#### -- 1.NOW(): 当前的日期和时间

```mysql
SELECT now() as
```



#### -- 2.YEAR() / MONTH() / DAY() :提取年月日

```mysql
SELECT id,year(id)as 年, month(id) as 月 ,day (id) as 日 from `candy 01-03 time`
```



#### -- 3.DATEDIFF(): 计算两个日期之间的天数差

```mysql
SELECT abs (DATEDIFF(now(),'2025-05-16')) as 相差的天数     -- 一般是生日祝福的短信，邮件
```



#### -- 4.DATA_FORMAT(): 格式化日期

```mysql
select event_time,date_format(event_time,'%Y年-%m月-%d日 %H时:%i分:%s秒') as format_value from event_log
```



#### -- 5.TIMESTAMPDIFF():计算两个时间的差值(单位可指定)

```mysql
SELECT TIMESTAMPDIFF(MINUTE,'2025-04-14 17:15:06','2025-05-16 23:01:09') as dfv1
```







## 控制流函数类

#### -- 1. if(): 简单的条件判断，相当于编程语言中的if...else

```mysql
SELECT name,score,if(age>18,'成年','未成年') as result from `candy 01-02`
```



#### -- 2. case: 多条件分支判断

```mysql
select name,score,
case 
	when score>=90 then '优秀'
	when score>=80 then '良好'
	when score>=60 then '及格'
	else'不及格'
	
end as result from `candy 01-02`
```



#### -- 3.nullif(): 比较两个表达式，热锅相同返回NULL

参考语法：select nullif(10,10) as result

##### -- 3.3-- 3.3添加测试的语句

```mysql
-- 创建表
CREATE TABLE sales_data (
    sale_id INT PRIMARY KEY AUTO_INCREMENT,
    product_id VARCHAR(10),
    product_name VARCHAR(50),
    sale_date DATE,
    sale_amount DECIMAL(10, 2),
    discount DECIMAL(5, 2)
);
-- 添加数据
INSERT INTO sales_data (product_id, product_name, sale_date, sale_amount, discount) VALUES
('P001', '智能手表', '2023-10-01', 299.99, 0),
('P002', '无线耳机', '2023-10-02', 149.99, 10),
('P003', '平板电脑', '2023-10-03', 499.99, 25),
('P004', '蓝牙音箱', '2023-10-04', 79.99, 0),
('P005', '智能手机', '2023-10-05', 699.99, 50);


SELECT 
    product_id,
    product_name,
    sale_date,
    sale_amount,
    NULLIF(discount, 0) AS 折扣金额
FROM 
    sales_data;
```



#### -- **4.COALESCE()**：返回第一个非 NULL 的值。

```mysql
--4.1参考语法：SELECT COALESCE(NULL, 2, 3) AS result;
--4.2例如：假设我们想查询每个学生的姓名、选修课程名称以及成绩。如果某个学生没有选任何课程，
	则我们希望显示“未选课”作为课程名称，并将成绩显示为 0
SELECT 
    s.sname AS student_name,
    COALESCE(c.cname, '未选课') AS course_name,
    COALESCE(sc.score, 0) AS score
FROM 
    student s
LEFT JOIN 
    sc ON s.sno = sc.sno
LEFT JOIN 
    course c ON sc.cno = c.cno;
```





#### -- 5.IFNULL()：如果第一个参数为NULL，则返回第二个参数。

```mysql
-- 例如：s004这个学生虽然选择了c002这门课但是没去考试，那么成绩查询出来则默认为0
select IFNULL(score,0) from `candy 01-02`
```





## mysql 练习

1.查询所有学生的姓名和年龄

```mysql
select name as 姓名, concat (age,'岁')
from `candy 01-01`
```

![image-20250410110035091](C:\Users\32473\AppData\Roaming\Typora\typora-user-images\image-20250410110035091.png)



2.查询每门课程的选课人数和最高分

```mysql
select max(age) from `candy 01-02`
```



3.查询每位学生的平均成绩，并按平均成绩从高到低排序

```mysql
select id,avg(score) from `candy 01-02` group by id
```



4.查询每个学生是否通过了所有课程（即所有课程的成绩都 >=60）

```mysql
select id,
	case
		when min(score)>=60 then'通过'
		else'未通过'
	end
from `candy 01-02`
group by id
```



5.查询所有事件的时间，并以“YYYY-MM-DD HH:mm:ss”格式显示

```mysql
SELECT event_name , DATE_FORMAT(event_time, '%Y-%m-%d %H:%i:%s') AS formatted_time
FROM event_log;
```

