# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**

![image](https://github.com/user-attachments/assets/695a7f01-aed4-4858-a301-d961b73cde77)


```sql
select date(AppointmentDateTime) as AppointmentDate, count(*) as  TotalAppointments
from Appointments
group by AppointmentDate;
```

**Output:**

![image](https://github.com/user-attachments/assets/b14f88a1-c1a9-42d0-bae4-d882657f1e57)

**Question 2**

![image](https://github.com/user-attachments/assets/2e75ee22-7f6f-45ac-b98d-3faf73b4bb6e)


```sql
select name,email,length(email) as  min_email_length
from customer
order by length(email)
limit 1;
```

**Output:**

![image](https://github.com/user-attachments/assets/1d545d0b-2f70-4403-a615-588e5b261299)

**Question 3**

![image](https://github.com/user-attachments/assets/4eca07ed-0e28-4b09-a3f1-a3d15346c968)


```sql
select avg(length(email)) as avg_email_length
from customer
order by length(email)
limit 1;
```

**Output:**

![image](https://github.com/user-attachments/assets/5560d51e-31f3-4500-bd99-321dd1b9db92)

**Question 4**

![image](https://github.com/user-attachments/assets/4b5ae2fc-930c-4be4-836b-9e441908948a)


```sql
select sum(purch_amt) as TOTAL
from orders
```

**Output:**

![image](https://github.com/user-attachments/assets/34263e68-a303-4561-9604-fa121c78a36e)

**Question 5**

![image](https://github.com/user-attachments/assets/97c38b68-e8eb-4fa0-99bf-65c6aa7751b7)


```sql
select jdate,MIN(workhour)
from employee1
group by jdate
having MIN(workhour) <10 ;
```

**Output:**

![image](https://github.com/user-attachments/assets/ac3ea2f4-d55d-4f17-b67f-0b789dd289fb)

**Question 6**
![image](https://github.com/user-attachments/assets/198f73fc-92bf-44dd-9270-a2d7653bff65)



```sql
select max(purch_amt) as MAXIMUM
from orders
order by purch_amt;
```

**Output:**

![image](https://github.com/user-attachments/assets/d4a77ba2-8c60-4188-b40c-d58340e7b220)


**Question 7**

![image](https://github.com/user-attachments/assets/0ee1bc64-51ff-4336-ac94-2782fd23dea1)



```sql
select address,AVG(salary)
from customer1
group by address
having avg(salary) > 5000
```

**Output:**

![image](https://github.com/user-attachments/assets/8f3edd30-e9e8-4425-9de1-cff048369ae8)

**Question 8**

![image](https://github.com/user-attachments/assets/fcb8ceab-b54a-433c-abb4-c6989c2be2cb)



```sql
select category_id,count(product_name)
from products
group by category_id
having min(category_id) <3
```

**Output:**
![image](https://github.com/user-attachments/assets/cbad0c42-f896-4394-9484-bb338100342a)


**Question 9**

![image](https://github.com/user-attachments/assets/38219b0f-8f55-48e7-90e2-11e7d73c6579)



```sql
select sum(inventory) as total
from fruits
where unit ='LB'
```

**Output:**

![image](https://github.com/user-attachments/assets/22b88888-6959-4199-b37b-f510ed1e9567)


**Question 10**

![image](https://github.com/user-attachments/assets/87ed7af8-d973-43c3-8a62-085fd3337951)



```sql
select count(distinct salesman_id) as COUNT
from orders
```

**Output:**

![image](https://github.com/user-attachments/assets/a84d3ab8-bb50-4ca5-8071-d218fb9f983e)



## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.

![image](https://github.com/user-attachments/assets/76f13057-b2ba-4b90-a996-696d78163b66)

