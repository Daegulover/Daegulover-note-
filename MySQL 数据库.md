# MySQL 数据库

sql 是不区分大小写的

### 注释：

 	- --1.DDL操作之数据库操作
 	-  # 也行





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







