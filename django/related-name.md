
# Django related name

有ForeignKey的model里, django会自动生成一个FOO_set的属性, 可以用related_name替换这个属性名(用了related_name, Foo_set还是可以用)。例如:

```python
form django.db import models

class Game(models.Model):
    player = ForeignKey(User, related_name="players")
    judger = ForeignKey(User, related_name="judgers")
    level = models.IntegerField()

g1 = Game.objects.create(player=u1, judger=u20, level=9)
g2 = Game.objects.create(player=u2, judger=u20, level=9)
g3 Game.objects.create(player=u3, judger=u20, level=9)


g1.judger.judgers.all() #返回上面三个Game对象,所有judger为u20的Game对象
Game.objects.filter(judger=lol.judger) #效果跟上面相同

```
related_name="+", 不向后关联

[Django document](https://docs.djangoproject.com/en/dev/ref/models/fields/#django.db.models.ForeignKey.related_name)  
[What is `related_name` used for in Django?](http://stackoverflow.com/questions/2642613/what-is-related-name-used-for-in-django)
