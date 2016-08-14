
# Django related name

有ForeignKey的model里, django会自动生成一个FOO_set的属性, 可以用related_name替换这个属性名(用了related_name, Foo_set还是可以用)。例如:

```python
form django.db import models

class Game(models.Model):
    user = ForeignKey(User, related_name="players)
    level = models.IntegerField()

lol = Game.objects.get(id=1)
lol.players.all() #返回所有User结果
lol.user_set.all() #返回所有User结果

# 原生sql语句为:
select ... # check it later

```
如果一个model里有两个ForeignKey, 都是指向同一个table, 那会产生两个FOO_set, 所以这时必须声明related_name
> 这个时候用FOO_set会是哪个呢? 还可以用吗?


[Django document](https://docs.djangoproject.com/en/dev/ref/models/fields/#django.db.models.ForeignKey.related_name)  
[What is `related_name` used for in Django?](http://stackoverflow.com/questions/2642613/what-is-related-name-used-for-in-django)
