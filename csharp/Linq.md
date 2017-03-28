
# Linq

## Select

Select method is similar with `map` in `python` or other languages.

```c#
[TestMethod]
public void TestSelect()
{
    List<int> squares = Enumerable.Range(1, 4).Select(x => x * x).ToList();
    List<int> expect = new List<int>() { 1, 4, 9, 16 };
    CollectionAssert.AreEqual(expect, squares);
}
```