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
```

#### **2. `WHERE` Clause**
Find all employees from the IT department earning more than 60,000.

```sql
```

#### **3. `HAVING` Clause**
Find departments where the total salary exceeds 100,000.

```sql
```

#### **4. `DISTINCT` Clause**
List all unique departments in the company.

```sql
```

#### **5. `ALIAS` Usage**
Show employee names and their annual salary as `Annual_Salary`.

```sql
```

#### **6. `GROUP BY` Clause**
Find the total salary per department.

```sql
```

#### **7. `ORDER BY` Clause**
Get all employees sorted by salary in descending order.

```sql
```

#### **8. `LIMIT` Clause**
Retrieve the top 3 highest-paid employees.

```sql
```

#### **9. Caching & Query Optimization (`SQL_CACHE`, `SQL_NO_CACHE`)**
Retrieve sales data, using query caching.

```sql
```

To disable caching:
```sql
```

#### **10. SQL Variables and Buffering**
Find the employee with the highest salary using a variable.

```sql
```
