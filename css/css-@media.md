
# CSS media

根据不同设备自适应页面，可根据media来调整设置。例如以下:

```css

img{
    max-width: 100%;
    display: inline-block;
}

@media(min-width: 420px){
    img{
        max-width: 48%;
    }
}

@media(min-width: 760px){
    img{
        max-width: 24%;
    }
}

```
