
# System IO

## Path

`GetExtension` is a method to get the file extension. 

```c#
using System.IO;
[TestMethod]
public void FileExt()
{
    string ext = Path.GetExtension("C:/a.txt");
    Assert.AreEqual(".txt", ext, "get the file extension");
}
```
[Reference](https://msdn.microsoft.com/en-us/library/system.io.path.getextension(v=vs.110).aspx)