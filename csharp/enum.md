
# Enum

Seems like Enum can be very useful, why didn't I notice this type before?

```c#
enum Days { Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday };
[TestMethod]
public void EnumTest()
{
    Days today = Days.Monday;
    int dayNum = (int)today;
    Assert.AreEqual("Monday", today.ToString(), "shoud be Monday");
    Assert.AreEqual(1, dayNum, "shoud be 1");
}
```
[参考](https://msdn.microsoft.com/zh-cn/library/cc138362.aspx)