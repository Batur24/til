
# Collections

## defaultdict
```python
from collections import defaultdict

a_dict = {}
a_dict["hello"] # KeyError

b_dict = defaultdict(int)
a_dict["hello"] # 0

```

## namedtuple
> 带名字的tuple
```python
from collections import namedtuple

Point = namedtuple('Point', 'x y')

a = Point(11, 12)

a.x # 11
a.y # 12

```
