### ⚡ sep1

<details>

Reference type (left side)  
`Shape xx = ... ;`  
→ yahan Shape sirf ek reference type hai. Matlab compiler dekhega ki tum iss variable se Shape class/Interface ke andar declare kiye gaye methods hi call kar sakte ho.  

Object type (right side)   

new Circle(cx101, 5);  
 
- yahan constructor call ho raha hai Circle ka. Iska Shape se direct lena-dena nahi hota, kyunki constructor subclass mein hi defined hota hai.   

Tumhari line ko tod ke samjhte hain:   
`Shape xx = new Circle(cx101, 5);`  

Step 1: new Circle(cx101, 5)  
- Ye call karega Circle class ka constructor (agar tumne banaya hai).  
Example:  
```java

class Circle extends Shape {
    String name;
    int radius;

    Circle(String name, int radius) {
        this.name = name;
        this.radius = radius;
    }
}

```

Matlab compiler pehle check karega ki Circle class me aisa constructor exist karta hai ya nahi.  

Step 2: Shape xx = (that Circle object)  
- Ab wo Circle ka object ban gaya hai, lekin tum uska reference ek Shape type variable me store kar rahe ho.
Ye upcasting hai → subclass object ko superclass reference me daalna. Ye hamesha legal hai (agar inheritance relation hai).

Tumhara doubt:  

👉 "Shape class mei tou Circle constructor hoga nahi jo ye line handle kr sake??"  

Bilkul sahi pakda! ✅  

- Shape me Circle ka constructor hona zaroori nahi hai.  

- Circle ka constructor sirf Circle ke andar hi hota hai, wahi call hota hai.

Shape xx ka matlab sirf ye hai ki:  

- Tum xx se sirf wo methods call kar sakte ho jo Shape me declare hain.  

- Tum Circle-specific methods (jo Shape me nahi hain) directly xx se call nahi kar paoge.

Example full code:
```java
class Shape {
    void draw() {
        System.out.println("Drawing shape...");
    }
}

class Circle extends Shape {
    String name;
    int radius;

    Circle(String name, int radius) {
        this.name = name;
        this.radius = radius;
    }

    void draw() {
        System.out.println("Drawing circle " + name + " with radius " + radius);
    }

    void circleOnlyMethod() {
        System.out.println("This is only in Circle");
    }
}

public class Demo {
    public static void main(String[] args) {
        Shape s = new Circle("cx101", 5);

        s.draw();              // ✅ Allowed (declared in Shape, overridden in Circle)
        // s.circleOnlyMethod(); // ❌ Not allowed (Shape doesn't know this method)
    }
}


Output:

Drawing circle cx101 with radius 5

```

👉 So short answer:  

>new Circle(cx101, 5) → Circle ka constructor chal raha hai.  

>hape xx → reference type restrict karta hai ki tum Shape ke declared methods hi call kar pao.

>Constructor hamesha subclass me hi hota hai, superclass me nahi.
</details>