
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

## OrderedDict
> 有顺序的字典
```python
from collections import OrderedDict
a = {"banana": 43, "apple": 3, "orange": 23}
b = OrderedDict(sorted(a.items(), key=lambda t: t[0])) # 按照key排序
c = OrderedDict(sorted(a.items(), key=lambda t: t[1])) # 按照value排序
```
