
# 装饰器

虽然说经常用装饰器，但是自己没有写过装饰器，今天突然想到这个，然后搜索了下，发现挺简单的。

```
def say_hello(func):   
    def new_func(name):
        print "hello "
        return func(name)
    return new_func
 
@say_hello
def tesing(name):
    print name

tesing("David") #hello David
```
