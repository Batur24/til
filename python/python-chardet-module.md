
# python 检测编码

```
    pip install chardet
    from chardet import detect
    detect("hello") #{'confidence': 1.0, 'encoding': 'ascii'}
    detect("你好") #{'confidence': 0.7525, 'encoding': 'utf-8'}
```
utf8还是assic都是字符串对象，是二进制编码方式;可以用detect来检测;
unicode是unicode对象
```
len(dir("s")) #71
len(dir(u"s")) #73
[i for i in dir(u"s") if i not in dir("s")] #['isdecimal', 'isnumeric']
```
