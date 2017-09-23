
# CSS Animation

I found the CSS animation was much easier than I previous thought. I used to prefer using javascript to write animation, but after watching some youtube videos, no doubt the css solutions are much more elegant. See the code below.

```html
    <h1>test</h1>
    <div class="square">
        hello
    </div>


    <style>
        .square {
            width: 200px;
            height: 200px;
            text-align: center;
            line-height: 200px;
            background: red;
            cursor: pointer;
            transition: background 1s, transform 0.3s 1s;
        }

        .square:hover{
            background: blue;
            transform: rotate(360deg)
        }
    </style>
```

when mouse hover, the square would turn blue for 1 second, and transform will rotate as well.