
# Python Pip

今天在新的虚拟环境里使用django，用pip下载，6M的包一直下不下来。这种速度真是无法忍受。我去找了下pip国内的镜像，速度飞快，感觉太爽了！

```
    pip install -i http://pypi.douban.com/simple/ --trusted-host=pypi.douban.com django==1.8.4
```
