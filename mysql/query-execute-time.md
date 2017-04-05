
# Query Execute Time

To check a sql statement execute time, we can use `profiling`

```sql
set profiling = 1;
select * from user;
show profiling;
show profiling for query 1;
```

[Reference](http://stackoverflow.com/questions/11274892/measuring-actual-mysql-query-time)