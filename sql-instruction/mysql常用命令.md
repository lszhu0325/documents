# 创建数据库
create database 数据库名
# 展示数据库
show databases
# 使用数据库
use 数据库名 charset set uf8 collate utf8_general_ci
# 查看当前使用的数据
select database()
# 在当前数据库中建表的标准语句
create table user (
	id int(32) not null auto_increment,
	name varchar(32) not null,
	password varchar(50) not null,
	primary key(id)
) engine=innodb auto_increment=3 default charset=utf8
# 向表中插入数据
INSERT INTO USER VALUES (3, '孙悟空', '123456')




