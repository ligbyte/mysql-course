# README

_Read this in other languages:_
[_English_](README.en-US.md)

* MySQL常用数据类型(数值、字符串、日期时间、JSON类型、空间类型)

## 常用命令和语句


|  命令-语句            | 说明  |
|  -----               | ----- |
| mysql -u root -p    (mysql -h 127.0.0.1 -P 3306 -u root -p"123456" --ssl-mode=DISABLED  game) | 登录数据库                          |
| show databases;                                                                               | 显示数据库                          |
| create database game;                                                                         | 创建数据库                         |
| drop database game;                                                                           | 删除数据库                        |
| use game;                                                                                     | 选择数据库                         |
| create table player(id INT, name VARCHAR(20), level INT,exp INT, gold DECIMAL(10,2));         | 创建表                              |
| drop table player;                                                                            | 删除表                              |
| show tables;                                                                                  | 显示表:                              |
| desc player;                                                                                  | 查看表结构                          |
| alter table player modify column name varchar(200);                                           | 表: 修改表字段name长度                |
| alter table player rename column name to nick_name;                                           | 表: 重命名字段 (mysql 8.0.21) |
| alter table player change name nick_name varchar(100);                                        | 表: 重命名字段 (mysql 5.7.44)  |
| ALTER TABLE player ADD COLUMN last_login DATETIME;                                            | 表: 添加字段 |
| alter table player drop column last_login;                                                    | 表: 删除字段 |
| insert into player(id,nick_name,level,exp) values (1,"lime",190,10000);                       | 增          |
| 单元格                                                                                         | 删          |
| update player set level = 200 where name = "jun";                                             | 改          |
| select * from player;                                                                         | 查          |
| alter table player modify level int default 1;                                                | 表:修改默认值 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |
| 单元格                                                                                         | 单元格 |

## Course Links

* [YouTube](https://youtu.be/nZlH5in_660)
* [B站](https://www.bilibili.com/video/BV1AX4y147tA/)


## 数据的导入方法：

安装好MySQL之后，进入MySQL的命令行界面，创建一个名为game的数据库：
```sql
create database game;
```

然后退出MySQL的命令行界面，在终端中执行如下命令来导入数据：
```bash
mysql -u root -p game < game.sql
```

示例演示：
![Alt text](./img/mysql-import.png)

数据：
![Alt text](./img/database-snip.png)


## 数据的导入方法：

安装好MySQL之后，进入MySQL的命令行界面并按照下面的步骤来创建一个数据库：

1. 打开终端，输入如下命令来登录MySQL：
```bash
mysql -u your_username -p
```
将your_username替换为你的MySQL用户名，然后会提示你输入MySQL密码。

登录成功后，你应该会看到MySQL的提示符：
```css
mysql>
```

2. 输入如下命令来创建一个名为game的数据库：
```sql
CREATE DATABASE game;
```
3. 你可以通过如下命令来确认数据库是否创建成功：
```sql
SHOW DATABASES;
```
4. 退出MySQL的命令行界面：
```sql
exit;
```
5. 在终端中执行如下命令来导入数据：
```bash
mysql -u root -p game < game.sql
```

里面还有一些其他数据，可以用来练习：

* city_data：中国省市区三级联动数据，包括各区域的经纬度和身份证前六位。
* game.npc： 三国题材游戏武将数据。
* company：  MySQL官方提供的示例公司数据。
* sakila：   MySQL官方提供的示例电影租赁数据。
* shop：     一个简单的电商数据，包括商品、订单、用户等信息。
* world：    MySQL官方提供的示例世界国家和城市数据。

示例：
![Alt text](./img/sango.png)
