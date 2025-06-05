# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```

**Question 1**

![image](https://github.com/user-attachments/assets/04818378-2dc9-467d-b614-2b63c9d77feb)



```sql
INSERT INTO Customers(CustomerID  ,Name, Address, Email)
SELECT CustomerID ,Name ,Address, Email FROM Old_customers;
```

**Output:**

![image](https://github.com/user-attachments/assets/26a3e5cf-fcff-496d-b32c-02d3158238ff)


**Question 2**

![image](https://github.com/user-attachments/assets/23eb6657-a5ba-4144-a0d0-7c3cc89457c8)


```sql
UPDATE products
SET product_name = 'Grapefruit'
WHERE product_id =4;
```

**Output:**

![image](https://github.com/user-attachments/assets/473aa9d8-5ec3-449f-8dbb-7ade5898f043)

**Question 3**

![image](https://github.com/user-attachments/assets/1c342715-8111-4015-b9c6-8e15a43bbba3)


```sql
DELETE FROM surgeries
WHERE  surgery_id =3;
```

**Output:**

![image](https://github.com/user-attachments/assets/e5f9ae34-2171-4670-a28f-f73cf7d7e2fe)

**Question 4**

![image](https://github.com/user-attachments/assets/d7a1226e-45a4-4636-824d-fec9e7140f7b)


```sql
SELECT customer_id, cust_name, city, grade, salesman_id
FROM  customer
WHERE  grade >100;
```

**Output:**

![image](https://github.com/user-attachments/assets/96fd5275-4a92-4c69-9388-7af795b53147)

**Question 5**

![image](https://github.com/user-attachments/assets/d8f79995-752c-4e1b-a92e-6557b54fb687)


```sql
SELECT ename,hiredate,DATE(hiredate ,'+100 Days') AS DateAfter100Days
FROM emp;
```

**Output:**

![image](https://github.com/user-attachments/assets/428fb821-40c4-4cd4-8734-85239ffb183a)

**Question 6**

![image](https://github.com/user-attachments/assets/65985934-6989-416a-b18d-a26c423a101e)


```sql
SELECT id,ROUND(decimal,3) AS  rounded_value
FROM Calculations;
```

**Output:**

![image](https://github.com/user-attachments/assets/dcec3256-8c1f-4496-a356-70756b822ad5)

**Question 7**

![image](https://github.com/user-attachments/assets/0e8354b2-cb3e-4e10-b7ce-ff50a4f80610)


```sql
DELETE FROM Customer
WHERE LENGTH(CUST_NAME) =6;
```

**Output:**
![image](https://github.com/user-attachments/assets/f380fb09-c29e-4619-b906-56c290a4ff4f)


**Question 8**

![image](https://github.com/user-attachments/assets/b2748d5f-71c2-44bc-90ae-cb372f889ea0)


```sql
UPDATE Employees 
SET salary = 8000
WHERE employee_id =105 AND salary < 5000;
```

**Output:**

![image](https://github.com/user-attachments/assets/eb5e4fa9-43a2-4a7d-b464-20bf09d12b18)


**Question 9**

![image](https://github.com/user-attachments/assets/01e04d07-8b7f-43ba-b971-571584953176)



```sql
SELECT id, value1, 
        CASE 
           WHEN  value1 >50 THEN 'High'
           ELSE 'Low'
        END AS  value_category
FROM Calculations;

```

**Output:**
![image](https://github.com/user-attachments/assets/4eb27299-6f8c-4ca6-a580-e445046e2cde)


**Question 10**
![image](https://github.com/user-attachments/assets/eda03365-733c-4036-b7d5-29808868d5a4)



```sql
SELECT 
    product_id, 
    original_price, 
    discount_percentage,
    original_price *discount_percentage AS discount_amount
FROM 
    products
WHERE  
    original_price * discount_percentage >50;
```

**Output:**
![image](https://github.com/user-attachments/assets/8da24314-14bd-4d94-8487-b65d193c7f1e)


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.

![image](https://github.com/user-attachments/assets/557dbc8d-28d6-4388-8055-b18f80f8527f)

