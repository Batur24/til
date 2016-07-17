
# django orm join 查询

代码示例

```python
comments = CouponRewardInstanceLog.objects.filter(couponRewardInstance=red).extra(select={                        
                 'img':
                       'select wx_img from customer_storedvaluecard where \
                       weixin_couponrewardinstancelog.weixin_id=customer_storedvaluecard.finger_print',
                 'uname':
                       'select uname from customer_storedvaluecard where \
                       weixin_couponrewardinstancelog.weixin_id=customer_storedvaluecard.finger_print',
         })
```
