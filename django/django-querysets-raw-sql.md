
# 查看django querysets的原始sql语句
```python
    from django.db import connection, reset_queries
    connection.queryies # 查看raw sql, 花费时间
    reset_queries # 清除上面语句的结果
```
参考 https://docs.djangoproject.com/en/1.9/faq/models/#faq-see-raw-sql-queries
