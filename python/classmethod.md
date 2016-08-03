
# python classmethod

classmethod装饰器可以在不实例化类的情况下执行函数，例如:
```python
class TestClassMethod:
    @classmethod
    def print_text(self):
        print "ok, cool"

TestClassMethod.print_text() # ok, cool

class TestNoClassMethod:
    def print_text(self):
        print "ok, cool"

TestNoClassMethod.print_text() # 报错
TestNoClassMethod().print_text() # ok, cool
```
