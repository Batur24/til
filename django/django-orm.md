
## Django ORM

```
    Use QuerySet.count()

    ...if you only want the count, rather than doing len(queryset)
```

```
    Use QuerySet.exists()

    ...if you only want to find out if at least one result exists, rather than if queryset.
```

参考 https://docs.djangoproject.com/en/1.9/topics/db/optimization/


> 返回包含字典数据的列表
```
    result = QuerySet.values() # return ValuesQuerySet object
    list_result = [entry for entry in result] # return list with dict inside
```
