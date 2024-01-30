
**the difference between  a file system and a dbms**
- **dbms can be used to manage a database but we cant do it with a file system**
- **filesystem is a way to arrange files in a storage system (nands and discs)**
- **dbms provides data redundancy**
- **multiple users can access dbms**
- **data independence cant be implemented in a file system**

### 2 tier architecture

aka client server relationship
###### ADV:
- the main advantage is that it is very low maintenance 
###### DISADV:
- since client is directly connected to the server so it creates a security risk
- scalability is a huge issue if everyone accesses thru a single server as too many ppl on a single server creates a lag or slowdowns
### 3 tier architecture
it has an application layer in front of the server which then invokes
the database server by generation the query 


#### steps of making a DB
- DBMS (mysql in this case https://dev.mysql.com/downloads/file/?id=523570)
- create a database #creation 
    ```mysql
(CREATE DATABASE acme;) , (to use a DB write USE acme;)
```
- create a table ```
```mysql
CREATE TABLE users
   (first_name VARCHAR(100),
   last_name VARCHAR(100),
   email VARCHAR(50))```
- enter data
  ```mysql
  INSERT INTO users (first_name, last_name,) values ('Brad', 'Traversy', now());
```

- select names
  ```mysql
  SELECT * FROM users;
  SELECT first_name, last_name FROM users;
```

# *schema:-*
---
#### 3 schema architecture
- view level *(external schema)*
- logical level *(conceptual schema)*
- physical layer *(physical schema)*



# *data modeling*
___
##### relational model
- data + relations + semantics (meaning of the data) + constraints (parameters under which the data must be entered like no alphabates in the place of phone numbers)
- ###### types of relational model 
    1. conceptual model
	2. representational model
	 3. physical model 

# super key
---
Super key is an attribute set that can uniquely identify a tuple. A super key is a superset of a candidate key.

In the above EMPLOYEE table, for(EMPLOEE_ID, EMPLOYEE_NAME), the name of two employees can be the same, but their EMPLYEE_ID can't be the same. Hence, this combination can also be a key.

The super key would be EMPLOYEE-ID (EMPLOYEE_ID, EMPLOYEE-NAME), etc.




