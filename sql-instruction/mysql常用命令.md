# �������ݿ�
create database ���ݿ���
# չʾ���ݿ�
show databases
# ʹ�����ݿ�
use ���ݿ��� charset set uf8 collate utf8_general_ci
# �鿴��ǰʹ�õ�����
select database()
# �ڵ�ǰ���ݿ��н���ı�׼���
create table user (
	id int(32) not null auto_increment,
	name varchar(32) not null,
	password varchar(50) not null,
	primary key(id)
) engine=innodb auto_increment=3 default charset=utf8
# ����в�������
INSERT INTO USER VALUES (3, '�����', '123456')




