
# Linq

## Select

`Select` method is similar with `map` in `python` or other languages.

```c#
[TestMethod]
public void TestSelect()
{
    List<int> squares = Enumerable.Range(1, 4).Select(x => x * x).ToList();
    List<int> expect = new List<int>() { 1, 4, 9, 16 };
    CollectionAssert.AreEqual(expect, squares);
}
```

## Where

`Where` method is similar with `filter` in `python` or other languages.

```c#
[TestMethod]
    public void TestWhere()
    {
        int[] array = { 1, 50, 44 };
        var result = array.Where(x => x > 45);
        CollectionAssert.Contains(result.ToList(), 50, "test where");
    }
```

## Aggregate

`Aggregate` method is similar with `reduce` in `python` or other languages.

```c#
[TestMethod]
public void AggregateTest()
{
    int[] array = { 1, 50, 50 };
    int result = array.Aggregate((a, b) => a + b );
Assert.AreEqual(101, result, "test Aggregate");
}
```

## Sum

`Sum` method is for adding all numbers in `Linq`

```c#
[TestMethod]
    public void TestSum()
    {
        List<int> nums = new List<int> { 1, 2, 3 };
        int sumList = nums.Sum(n => n);
        Assert.AreEqual(6, sumList, "sum the list");
    }
```