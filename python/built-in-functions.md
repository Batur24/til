
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

```python
# Return True if all elements of the iterable are true 
# (or if the iterable is empty). 
# Equivalent to:

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

## any()
```python
# Return True if any element of the iterable is true. 
# If the iterable is empty, return False. Equivalent to:
def any(iterable):
    for element in iterable:
        if element:
            return True
    return False
```
可迭代的元素有一个不为空，返回True, 所有为空False
例子
```python
a = (1,2,0,"test")
print any(a) # True
b = (0,0,"")
print any(b) # False
```

## getattr(object, name[, default])
获取对象属性
```python
# Return the value of the named attribute of object. 
# name must be a string. 
# If the string is the name of one of the object’s attributes, 
# the result is the value of that attribute. 
# For example, getattr(x, 'foobar') is equivalent to x.foobar. 
# If the named attribute does not exist, 
# default is returned if provided, 
# otherwise AttributeError is raised.

class Play:
	def play(self):
		return "let's play"

p = Play()
action = getattr(p, "play)
action() # let's play

```
## hasattr(object, name)
对象是否有指定的属性
```python
# The arguments are an object and a string. 
# The result is True 
# if the string is the name of one of the object’s attributes, 
# False if not. 
# (This is implemented by calling getattr(object, name) 
# and seeing whether it raises an exception or not.)

class Play:
	def play(self):
		return "let's play"

hasattr(Play, "play") # True
```
## join()
```python
	# The method join() returns a string 
	# in which the string elements of sequence 
	# have been joined by str separator.
	a1 = ["a","b","c"]
	a2 = "abcde"
	b1 = ",".join(a1)
	b2 = ",".join(a2)
	print b1 # "a,b,c"
	print b2 # "a,b,c,d,e"
```
可迭代的字符元素用指定的字符连接起来


