# 第一次实验
### 18软工三班 王鹏凯

#### sql代码

![](./pict1.png)

```sql 
SELECT d.department_name,count(e.job_id)as "部门总人数",
avg(e.salary)as "平均工资"
from hr.departments d JOIN hr.employees e
on d.department_id = e.department_id
and d.department_name in ('IT','Sales')
GROUP BY d.department_name;

