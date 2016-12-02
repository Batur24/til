
# Python xlwt

## http返回excel
```python
def export_excel(request):
    response = HttpResponse(content_type='application/ms-excel')
    book = xlwt.Workbook(encoding="utf-8")
    response["Content-Disposition"] = 'attachment; filename=%s.xls' %"my-excel"
    sh = book.add_sheet("sheet1")
    sh.write(0,0,"hello world")
    book.save(response)
    return response
```
