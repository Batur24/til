
# django middleware

> 自定义中间件

## 位置
文件夹:yourproject/yourapp/middleware  
**初始化文件夹** middleware建__init__.py  
创建文件filter_ip_middleware.py

## 创建
允许特定ip访问
```
# filter_ip_middleware.py
class FilterIPMiddleware(object):
    # Check if client IP is allowed
    def process_request(self, request):
        allowed_ips = ['192.168.1.1', '123.123.123.123', etc...] # Authorized ip's
        ip = request.META.get('REMOTE_ADDR') # Get client IP
        if ip not in allowed_ips:
            raise Http403 # If user is not allowed raise Error

       # If IP is allowed we don't do anything
       return None
```
## 设置
在settings.py中设置
```
MIDDLEWARE_CLASSES = (
    'django.middleware.common.CommonMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
     # Above are django standard middlewares

     # Now we add here our custom middleware
     'yourapp.middleware.filter_ip_middleware.FilterIPMiddleware'
)
```

## 说明
方法process_request是必须的，如果返回异常，直接返回;如果正常，返回None，交给下一个中间件处理。

[参考1](http://stackoverflow.com/questions/18322262/how-to-setup-custom-middleware-in-django)
