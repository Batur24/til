
# Python 内置函数

利用零散的时间，把python内置的函数一个一个过一遍。

## abs()

```
Return the absolute value of a number. 
The argument may be an integer or a floating point number. 
If the argument is a complex number, its magnitude is returned.
```

返回一个数字的绝对值。  
参数可以是整型，也可以是浮点数。   
如果参数是复数，返回｀该复数与其共轭复数的正平方根｀ 额...

```
a = complex(3,4) # a = (3+4j)
abs(a) # 5.0
```

## all()

```
Return True if all elements of the iterable are true 
(or if the iterable is empty). 
Equivalent to:

def all(iterable):
    for element in iterable:
        if not element:
            return False
    return True
```
如果可迭代的每一个元素都是True，返回True
```
a = [1,2,3]
all(a) # True
a = [1,2,0]
all(a) # False
```
