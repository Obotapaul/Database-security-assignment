# Database-security-assignment
# SQL Solutions Documentation

This document provides an explanation of the SQL queries written in the `answers.sql` file. Each query addresses a specific task related to database management and user privileges.

---
Question 1 🗑️
Task: Drop an index named `IdxPhone` from the `customers` table.

Solution:
```sql
ALTER TABLE customers
DROP INDEX IdxPhone;

CREATE USER 'bob'@'localhost'
IDENTIFIED BY 'S$cu3r3!';

Question 2 👤
Task: Write an SQL query to create a user named `bob` with the password `S$cu3r3!`, restricted to the `localhost` hostname.

Solution:
```sql
CREATE USER 'bob'@'localhost'
IDENTIFIED BY 'S$cu3r3!';
```
- The `CREATE USER` statement creates a new user named `bob` with access restricted to the `localhost` hostname.
- The `IDENTIFIED BY` clause sets the password for the user.

---
Question 3 🔑
Task: Write an SQL query to grant the `INSERT` privilege to the user `bob` on the `salesDB` database.

Solution:
```sql
GRANT INSERT
ON salesdb
TO 'bob@localhost';
```
- The `GRANT` statement is used to assign the `INSERT` privilege to the user `bob`.
- The `ON salesdb` clause specifies that the privilege is granted for the `salesDB` database.
- The `TO 'bob@localhost'` clause ensures the privilege is granted to the `bob` user restricted to `localhost`.

---
Question 4 🔐
Task: Write an SQL query to change the password for the user `bob` to `P$55!23`.

Solution:
```sql
ALTER 'bob@localhost' 
IDENTIFIED BY 'P$55!23';
```
- The `ALTER` statement is used to modify the user `bob`.
- The `IDENTIFIED BY` clause updates the password to `P$55!23`.
