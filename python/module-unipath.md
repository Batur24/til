
# Module Unipath 

Unipath模块

## 安装
pip install unipath

## 使用
```
from unipath import Path

file_path = Path(__file__)
current_dir = Path.(__file__).ancestor(1)
upper_dir = Path.(__file__).ancestor(2)

```

