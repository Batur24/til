
# F() Expressions

```python
from django.db.models import F
User.objects.filter(userid=F('mid')) # 筛选出userid和mid相同的
```


