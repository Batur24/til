
# String Unicode

string => unicode
```python
s = "hello world"
u = unicode(s, "utf-8")

# or
u = s.decode("utf-8")

print u, type(u)
```

unicode => string
```
u = u"hello world"
s = u.encode("utf-8")
print s, type(s)

```
