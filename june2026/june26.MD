## ⚡june8 

- started coding 3 years ago...
- `type nul > newfile.txt`  command in cmd terminal

## june11
-   `alt + z` word wrap
- viewBox is like a telescope

        - 4 parameters
        - minX minY width height
        -   pan         zoom
        - if zoom parameters are greater than svg height and width --> ZOOMS IN (bigger)
        - if zoom parameter are smaller than svg height n width --> ZOOMS OUT (smaller)

- always use viewBox along with svg heigth and width parameters.



## june13

**Ideal tag position**


```html
<!DOCTYPE html>
<html>
<head> <!-- INSIDE HEAD-->
  <style>/* CSS here */</style>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <!-- HTML content -->
  <script src="script.js"></script>
</body>
</html>

```




## ⚡june 17
```html
<svg width="200" height="400" viewBox="0 0 200 400">

    <!-- Pole (Behind) -->
    <path
        d="
            M 93 300
            L 107 300
            L 103 165
            L 97 165
            Z"
        fill="#777"
        stroke="black"/>

    <!-- Windmill -->
    <g transform="translate(100 165)">

        <g>

            <animateTransform
                attributeName="transform"
                type="rotate"
                from="0 0 0"
                to="360 0 0"
                dur="4s"
                repeatCount="indefinite"/>

            <!-- Center -->
            <circle
                r="8"
                fill="#777"
                stroke="black"/>

            <!-- Blade 1 -->
            <path
                d="
                    M -7 -20
                    C -7 -10 7 -10 7 -20
                    L 2 -80
                    L -2 -80
                    Z"
                fill="#bbb"
                stroke="black"/>

            <!-- Blade 2 -->
            <path
                transform="rotate(120)"
                d="
                    M -7 -20
                    C -7 -10 7 -10 7 -20
                    L 2 -80
                    L -2 -80
                    Z"
                fill="#bbb"
                stroke="black"/>

            <!-- Blade 3 -->
            <path
                transform="rotate(-120)"
                d="
                    M -7 -20
                    C -7 -10 7 -10 7 -20
                    L 2 -80
                    L -2 -80
                    Z"
                fill="#bbb"
                stroke="black"/>

        </g>

    </g>

</svg>
```
