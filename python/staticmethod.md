
# python staticmethod

staticmethod装饰器既可以在不实例化执行函数，也可以实例化后执行，例如:
```python
class TestStaticMethod:
    @staticmethod
    def print_text():
        print "okay"

TestStaticMethod.print_text() # okay
TestStaticMethod().print_text() # okay
```
加上staticmethod装饰器，不再用参数self
