
# UnitTest

## Assert


## StringAssert


## CollectionAssert

To compare two list
```c#
    List<int> expect = new List(){1, 2};
    List<int> actual = new List(){3, 4};
    CollectionAssert.AreEqual(expect, actual);
```


