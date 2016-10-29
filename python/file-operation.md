

# 写入文件

```python
import codecs
import io

with codecs.open("test.l", mode='w', encoding='utf-8') as f:
    f.write(u"你好")


with io.open("test.l", mode='w', encoding='utf-8') as f:
    f.write(u"你好")
```
