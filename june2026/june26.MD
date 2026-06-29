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

## june21

<details><summary>SVG</summary>

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        #tt{
            transition: transform 1s ease;
        }
        #tt:hover{
            transform:  translateX(500px); 
        }
    </style>
</head>

<body>
    <svg height="500" width="500" viewBox="0 0 500 500" style="border: 2px solid black;background-color:#5ab5ff">

        <circle cx="250" cy="250" r="210" fill="#e06534" />
        <circle cx="250" cy="250" r="150" fill="white" />
        <circle cx="250" cy="250" r="80" fill="#2c6837" />

    </svg>
    <hr>
    <svg height="200" width="200" style="border: 2px solid black;">
        <rect x="0" y="0" width="100" height="100" fill="blue" />
        <rect x="100" y="0" width="100" height="100" fill="green" />
        <rect x="0" y="100" width="100" height="100" fill="red" />
        <rect x="100" y="100" width="100" height="100" fill="yellow" />

    </svg>
    <hr>
    <!-- VIEWBOX -->
    <svg height="200" width="200" viewBox="80 80 100 100">

        <rect x="0" y="0" width="100" height="100" fill="blue" />
        <rect x="100" y="0" width="100" height="100" fill="green" />
        <rect x="0" y="100" width="100" height="100" fill="red" />
        <rect x="100" y="100" width="100" height="100" fill="#ffff00" />

    </svg>

    <hr>

    <svg id="tt" height="400" width="400" viewBox="0 0 400 400" style="border: 3px GREY solid;">   
        <polygon stroke="orange" fill="gold"  stroke-width="5"
            points=
            "
            0,200
            160,160
            200,0
            240,160
            400,200
            240,240
            200,400
            160,240
            "/>

            <polyline stroke="blue" stroke-width="4" points="50,50 60,30 60,100" fill="none"/>    

    </svg>
    <!-- I did this myself -->

    <br>
    <br>
    <svg height="500" width="800" style="border: 2px blue solid;background-color:azure">

        <ellipse/>
    </svg>



</body>

</html>
```
</details>


## june25


<details>


```
╔════════════════════════════════════════════════════════════════════╗
║        💡 JavaScript Boolean + ! (NOT) + Bulb Toggle Summary      ║
╚════════════════════════════════════════════════════════════════════╝

1️⃣ Boolean
   ├─ true  ✅
   └─ false ❌

2️⃣ if Statement
   ├─ if(expression)
   ├─ expression → evaluates to true/false
   ├─ true  → block runs ▶️
   └─ false → block skipped ⏭️

3️⃣ NOT Operator (!)
   ├─ !true  → false
   ├─ !false → true
   └─ Meaning: "Give me the opposite value." 🔄

4️⃣ Equivalent Conditions
   ├─ if(a)        ≡ if(a === true)
   └─ if(!a)       ≡ if(a === false)

5️⃣ Bulb State 💡
   Initial:
      on = false   (Bulb OFF)

   First Click:
      on == false ✅
      → Turn bulb ON
      → on = true

   Second Click:
      on == true
      → Turn bulb OFF
      → on = false

6️⃣ Shortcut (Toggle)
   Instead of:

      if(on === false)
          on = true;
      else
          on = false;

   Use:

      on = !on;

   Because:
      false → true
      true  → false

7️⃣ Golden Rules ⭐
   🟢 if(a)
      = "If a is true."

   🔴 if(!a)
      = "If a is false."

   🔄 a = !a
      = "Flip (toggle) the value of a."

────────────────────────────────────────────────────────────────────

🧠 Mental Reading Trick

if(a)
👉 "Is a true?"

if(!a)
👉 "Is a false?"

a = !a
👉 "Make a the opposite of what it is."

────────────────────────────────────────────────────────────────────

🎯 Remember:
`!` DOES NOT mean "true".
`!` means "NOT" (the opposite value).

```



</details>


## ⚡june26

- The `**` operator computes the exponential (power) of a number


## ⚡june29
- a python function can hold variables with it.

```python
def greet():
      print("Hi")



greet.language = "English"

print(greet.language)
#English
```

Totally works
