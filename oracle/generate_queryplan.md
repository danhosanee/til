# Generate Query Plan 

> Generate query plan in Oracle for tuning

```sql
explain plan for
select  e.ename,r.rname
from    employees  e
join    roles       r on (r.id = e.role_id)
join    departments d on (d.id = e.dept_id)
where   e.staffno <= 10
and     d.dname in ('Department Name 1','Department Name 2');

SELECT *
FROM table(DBMS_XPLAN.DISPLAY (FORMAT=>'ALL +OUTLINE'));
```
