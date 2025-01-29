### **Database Schema:**
Assume you have the following tables:

#### `employees`
| emp_id | name     | department  | salary | hire_date  |
|--------|---------|------------|--------|------------|
| 1      | Alice   | HR         | 50000  | 2020-05-01 |
| 2      | Bob     | IT         | 60000  | 2019-06-10 |
| 3      | Charlie | IT         | 70000  | 2018-07-15 |
| 4      | David   | HR         | 52000  | 2021-03-12 |
| 5      | Eve     | Finance    | 75000  | 2017-08-20 |

#### `sales`
| sale_id | emp_id | amount | sale_date  |
|---------|--------|--------|------------|
| 1       | 1      | 5000   | 2024-01-01 |
| 2       | 2      | 12000  | 2024-01-02 |
| 3       | 3      | 8000   | 2024-01-03 |
| 4       | 4      | 4000   | 2024-01-04 |
| 5       | 5      | 15000  | 2024-01-05 |

---

### **SQL Problems:**

#### **1. Basic `SELECT` Query**
Retrieve the names and salaries of all employees.

```sql
SELECT name, salary FROM employees;
```

#### **2. `WHERE` Clause**
Find all employees from the IT department earning more than 60,000.

```sql
SELECT * from employees where department = "IT" AND salary > 60000;
```

#### **3. `HAVING` Clause**
Find departments where the total salary exceeds 100,000.

```sql
select department, sum(salary) AS Total_Salary from employees group by department HAVING Total_Salary > 100000;
```

#### **4. `DISTINCT` Clause**
List all unique departments in the company.

```sql
SELECT DISTINCT department from employees;
```

#### **5. `ALIAS` Usage**
Show employee names and their annual salary as `Annual_Salary`.

```sql
SELECT name, salary AS Annual_Salary from employees;
```

#### **6. `GROUP BY` Clause**
Find the total salary per department.

```sql
 SELECT department, sum(salary) AS SALARY from employees group by department;
```

#### **7. `ORDER BY` Clause**
Get all employees sorted by salary in descending order.

```sql
SELECT * from employees order by salary DESC;
```

#### **8. `LIMIT` Clause**
Retrieve the top 3 highest-paid employees.

```sql
 select * from employees order by salary DESC Limit 3;
```

#### **9. Caching & Query Optimization (`SQL_CACHE`, `SQL_NO_CACHE`)**
Retrieve sales data, using query caching.

```sql
SELECT SQL_CACHE * FROM sales;
```

To disable caching:
```sql
SELECT SQL_NO_CACHE * FROM sales;
```

#### **10. SQL Variables and Buffering**
Find the employee with the highest salary using a variable.

```sql
select @max_salary := MAX(salary) from employees;
SELECT name, salary from employees where salary=@max_salary
```
