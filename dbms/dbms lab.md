**assignment lab day 1 : create the test table
insert data 
describe
show the entire test table 
find out all names of the test table***
#creation

| id | name | city | phone number | salary |
| ---- | ---- | ---- | ---- | ---- |
| e101 | Tamal saha | Kolkata | 83522151 | 32000.00 |
| e102 | Rohit Sen | Delhi |  | 35000.86 |
| e103 | Kunal sen | Durgapur | 93128641 | 42000.96 |
| e104 | Ruma pal | Kolkata | 94328641 | 35050.32 |
| e105 | Souvik raj | Bangalore |  | 41000.00 |
| e106 | Raj kumar | Delhi | 62934261 |  |
| e107 | probal sen | Durgapur | 92315621 |  |


```mysql

mysql> desc student;
+---------+-------------+------+-----+---------+-------+
| Field   | Type        | Null | Key | Default | Extra |
+---------+-------------+------+-----+---------+-------+
| roll_no | char(6)     | YES  |     | NULL    |       |
| regn_no | char(10)    | YES  |     | NULL    |       |
| name    | varchar(50) | YES  |     | NULL    |       |
| dob     | date        | YES  |     | NULL    |       |
| marks   | smallint(6) | YES  |     | NULL    |       |
+---------+-------------+------+-----+---------+-------+
5 rows in set (0.00 sec)

mysql> show tables;
+----------------+
| Tables_in_lab1 |
+----------------+
| student        |
| test           |
+----------------+
2 rows in set (0.00 sec)

mysql> desc hjgkjk;
ERROR 1146 (42S02): Table 'lab1.hjgkjk' doesn't exist
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| lab1               |
| lab2               |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| world              |
+--------------------+
8 rows in set (0.00 sec)

mysql> desc student;
+---------+-------------+------+-----+---------+-------+
| Field   | Type        | Null | Key | Default | Extra |
+---------+-------------+------+-----+---------+-------+
| roll_no | char(6)     | YES  |     | NULL    |       |
| regn_no | char(10)    | YES  |     | NULL    |       |
| name    | varchar(50) | YES  |     | NULL    |       |
| dob     | date        | YES  |     | NULL    |       |
| marks   | smallint(6) | YES  |     | NULL    |       |
+---------+-------------+------+-----+---------+-------+
5 rows in set (0.00 sec)

mysql> drop table student;
Query OK, 0 rows affected (0.05 sec)

mysql> desc student;
ERROR 1146 (42S02): Table 'lab1.student' doesn't exist
mysql> create table student(roll_no char(6) primary key,regn_no char(10) not null,name varchar(50),dob date,marks smallint);
Query OK, 0 rows affected (0.06 sec)

mysql> desc student;
+---------+-------------+------+-----+---------+-------+
| Field   | Type        | Null | Key | Default | Extra |
+---------+-------------+------+-----+---------+-------+
| roll_no | char(6)     | NO   | PRI | NULL    |       |
| regn_no | char(10)    | NO   |     | NULL    |       |
| name    | varchar(50) | YES  |     | NULL    |       |
| dob     | date        | YES  |     | NULL    |       |
| marks   | smallint(6) | YES  |     | NULL    |       |
+---------+-------------+------+-----+---------+-------+
5 rows in set (0.00 sec)

mysql> insert into student values ('123456',,'avik samanta',,100);
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near ''avik samanta',,100)' at line 1
mysql> insert into student values ('123456','2143253251','avik samanta',,100);
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '100)' at line 1
mysql> insert into student values ('123456','2143253251','avik samanta','',100);
ERROR 1292 (22007): Incorrect date value: '' for column 'dob' at row 1
mysql> insert into student values ('123456','2143253251','avik samanta',null,100);
Query OK, 1 row affected (0.04 sec)

mysql> insert into student values ('123456','2143253251','avik samanta','2002-12-15',100);
ERROR 1062 (23000): Duplicate entry '123456' for key 'PRIMARY'
mysql> insert into student values ('123457','2143253251','avik samanta','2002-12-15',100);
Query OK, 1 row affected (0.04 sec)

mysql> insert into student values ('123458','2143253251','avik samanta','21-05-2004',100);
ERROR 1292 (22007): Incorrect date value: '21-05-2004' for column 'dob' at row 1
mysql> select * from student;
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123456  | 2143253251 | avik samanta | NULL       |   100 |
| 123457  | 2143253251 | avik samanta | 2002-12-15 |   100 |
+---------+------------+--------------+------------+-------+
2 rows in set (0.00 sec)

mysql> select roll_no,regn_no,dob from student;
+---------+------------+------------+
| roll_no | regn_no    | dob        |
+---------+------------+------------+
| 123456  | 2143253251 | NULL       |
| 123457  | 2143253251 | 2002-12-15 |
+---------+------------+------------+
2 rows in set (0.00 sec)

mysql> insert into student (roll_no,regn_no,name) values ('123459','2143253251','avik samanta');
Query OK, 1 row affected (0.04 sec)

mysql> insert into student (name,roll_no,regn_no) values ('ariyan basu','123454','2143253251');
Query OK, 1 row affected (0.04 sec)

mysql> select * from student;
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123454  | 2143253251 | ariyan basu  | NULL       |  NULL |
| 123456  | 2143253251 | avik samanta | NULL       |   100 |
| 123457  | 2143253251 | avik samanta | 2002-12-15 |   100 |
| 123459  | 2143253251 | avik samanta | NULL       |  NULL |
+---------+------------+--------------+------------+-------+
4 rows in set (0.00 sec)

mysql> alter table student add column (class char(2));
Query OK, 0 rows affected (0.10 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> select * from student;
+---------+------------+--------------+------------+-------+-------+
| roll_no | regn_no    | name         | dob        | marks | class |
+---------+------------+--------------+------------+-------+-------+
| 123454  | 2143253251 | ariyan basu  | NULL       |  NULL | NULL  |
| 123456  | 2143253251 | avik samanta | NULL       |   100 | NULL  |
| 123457  | 2143253251 | avik samanta | 2002-12-15 |   100 | NULL  |
| 123459  | 2143253251 | avik samanta | NULL       |  NULL | NULL  |
+---------+------------+--------------+------------+-------+-------+
4 rows in set (0.00 sec)

mysql> alter table student drop column(class);
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '(class)' at line 1
mysql> alter table student drop column class;
Query OK, 0 rows affected (0.12 sec)
Records: 0  Duplicates: 0  Warnings: 0

mysql> alter table student modify name (char(20));
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '(char(20))' at line 1
mysql> alter table student modify coulm (name char(20));
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '(name char(20))' at line 1
mysql> alter table student modify column (name char(20));
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near '(name char(20))' at line 1
mysql> alter table student modify name char(20);
Query OK, 4 rows affected (0.10 sec)
Records: 4  Duplicates: 0  Warnings: 0

mysql> select * from student;
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123454  | 2143253251 | ariyan basu  | NULL       |  NULL |
| 123456  | 2143253251 | avik samanta | NULL       |   100 |
| 123457  | 2143253251 | avik samanta | 2002-12-15 |   100 |
| 123459  | 2143253251 | avik samanta | NULL       |  NULL |
+---------+------------+--------------+------------+-------+
4 rows in set (0.00 sec)

mysql> desc student;
+---------+-------------+------+-----+---------+-------+
| Field   | Type        | Null | Key | Default | Extra |
+---------+-------------+------+-----+---------+-------+
| roll_no | char(6)     | NO   | PRI | NULL    |       |
| regn_no | char(10)    | NO   |     | NULL    |       |
| name    | char(20)    | YES  |     | NULL    |       |
| dob     | date        | YES  |     | NULL    |       |
| marks   | smallint(6) | YES  |     | NULL    |       |
+---------+-------------+------+-----+---------+-------+
5 rows in set (0.00 sec)

mysql> alter table student modify name char(10);
ERROR 1265 (01000): Data truncated for column 'name' at row 1
mysql> select * from student;
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123454  | 2143253251 | ariyan basu  | NULL       |  NULL |
| 123456  | 2143253251 | avik samanta | NULL       |   100 |
| 123457  | 2143253251 | avik samanta | 2002-12-15 |   100 |
| 123459  | 2143253251 | avik samanta | NULL       |  NULL |
+---------+------------+--------------+------------+-------+
4 rows in set (0.00 sec)

mysql> update student set dob = '2003-12-25';
Query OK, 4 rows affected (0.05 sec)
Rows matched: 4  Changed: 4  Warnings: 0

mysql> select * from student;
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123454  | 2143253251 | ariyan basu  | 2003-12-25 |  NULL |
| 123456  | 2143253251 | avik samanta | 2003-12-25 |   100 |
| 123457  | 2143253251 | avik samanta | 2003-12-25 |   100 |
| 123459  | 2143253251 | avik samanta | 2003-12-25 |  NULL |
+---------+------------+--------------+------------+-------+
4 rows in set (0.00 sec)

mysql> update student set dob = '2010-07-23' where roll_no = '123456';
Query OK, 1 row affected (0.04 sec)
Rows matched: 1  Changed: 1  Warnings: 0

mysql> select * from student;
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123454  | 2143253251 | ariyan basu  | 2003-12-25 |  NULL |
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
| 123457  | 2143253251 | avik samanta | 2003-12-25 |   100 |
| 123459  | 2143253251 | avik samanta | 2003-12-25 |  NULL |
+---------+------------+--------------+------------+-------+
4 rows in set (0.00 sec)

mysql> update student set dob = '2015-01-01',marks = 80 where roll_no = '123454';;
Query OK, 1 row affected (0.04 sec)
Rows matched: 1  Changed: 1  Warnings: 0

ERROR:
No query specified

mysql> select * from student;
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123454  | 2143253251 | ariyan basu  | 2015-01-01 |    80 |
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
| 123457  | 2143253251 | avik samanta | 2003-12-25 |   100 |
| 123459  | 2143253251 | avik samanta | 2003-12-25 |  NULL |
+---------+------------+--------------+------------+-------+
4 rows in set (0.00 sec)

mysql> delete from student where roll_No = '123459';
Query OK, 1 row affected (0.04 sec)

mysql> select * from student;
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123454  | 2143253251 | ariyan basu  | 2015-01-01 |    80 |
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
| 123457  | 2143253251 | avik samanta | 2003-12-25 |   100 |
+---------+------------+--------------+------------+-------+
3 rows in set (0.00 sec)

mysql> truncate from student where roll_No = '123457';
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'from student where roll_No = '123457'' at line 1
mysql> commit;
Query OK, 0 rows affected (0.00 sec)

mysql> rollback;
Query OK, 0 rows affected (0.00 sec)

mysql> select * from student where dob >= "2010-01-01";
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123454  | 2143253251 | ariyan basu  | 2015-01-01 |    80 |
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
+---------+------------+--------------+------------+-------+
2 rows in set (0.00 sec)

mysql> select * from student where dob >= "2010-01-01" and dob <= "2014-12-31";
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
+---------+------------+--------------+------------+-------+
1 row in set (0.00 sec)

mysql> select * from student where dob between "2010-01-01" and "2014-12-31";
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
+---------+------------+--------------+------------+-------+
1 row in set (0.00 sec)

mysql> select * from student;
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123454  | 2143253251 | ariyan basu  | 2015-01-01 |    80 |
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
| 123457  | 2143253251 | avik samanta | 2003-12-25 |   100 |
+---------+------------+--------------+------------+-------+
3 rows in set (0.00 sec)

mysql> select * from student where name like "%basu";
+---------+------------+-------------+------------+-------+
| roll_no | regn_no    | name        | dob        | marks |
+---------+------------+-------------+------------+-------+
| 123454  | 2143253251 | ariyan basu | 2015-01-01 |    80 |
+---------+------------+-------------+------------+-------+
1 row in set (0.00 sec)

mysql> select * from student where name like "avik%";
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
| 123457  | 2143253251 | avik samanta | 2003-12-25 |   100 |
+---------+------------+--------------+------------+-------+
2 rows in set (0.00 sec)

mysql> select * from student where name like "%avik%";
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
| 123457  | 2143253251 | avik samanta | 2003-12-25 |   100 |
+---------+------------+--------------+------------+-------+
2 rows in set (0.00 sec)

mysql> select * from student;
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123454  | 2143253251 | ariyan basu  | 2015-01-01 |    80 |
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
| 123457  | 2143253251 | avik samanta | 2003-12-25 |   100 |
+---------+------------+--------------+------------+-------+
3 rows in set (0.00 sec)

mysql> select * from student where name like "a_ik%";
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
| 123457  | 2143253251 | avik samanta | 2003-12-25 |   100 |
+---------+------------+--------------+------------+-------+
2 rows in set (0.00 sec)

mysql> select * from student where name like "a_i%";
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123454  | 2143253251 | ariyan basu  | 2015-01-01 |    80 |
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
| 123457  | 2143253251 | avik samanta | 2003-12-25 |   100 |
+---------+------------+--------------+------------+-------+
3 rows in set (0.00 sec)

mysql> select * from student where marks = 100;
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
| 123457  | 2143253251 | avik samanta | 2003-12-25 |   100 |
+---------+------------+--------------+------------+-------+
2 rows in set (0.00 sec)

mysql> select * from student where marks = 100 and dob >= "2010-01-01";
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
+---------+------------+--------------+------------+-------+
1 row in set (0.00 sec)

mysql> select * from student where marks = 100 or dob >= "2010-01-01";
+---------+------------+--------------+------------+-------+
| roll_no | regn_no    | name         | dob        | marks |
+---------+------------+--------------+------------+-------+
| 123454  | 2143253251 | ariyan basu  | 2015-01-01 |    80 |
| 123456  | 2143253251 | avik samanta | 2010-07-23 |   100 |
| 123457  | 2143253251 | avik samanta | 2003-12-25 |   100 |
+---------+------------+--------------+------------+-------+
3 rows in set (0.00 sec)

