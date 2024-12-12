### ⚡dec1
- frontend project idea --> a card adder button(dom) which adds card to a grid layout.  
- flex-wrap:`wrap`  
- stiffneck
- grid  

      🔹g-t-c : repeat(5,300px) 
        but  
        g-t-c : repeat(auto-fit,300px)  
        also use justify-content and to center cards  
        
- how to prevent inspect tool in browser for a website.
- `...` for overflowing content in cards

### ⚡dec2
- i am struggling with grid a little bit , grid col i can handle(using minmax and auto-fit) but how to deal with rows, that i dont know 
- rows are not easy to predit , i guess i have to fix a definite size for them
- the solution is `grid-auto-rows: 350px` this makes new cards evrytime with 350px tall  
- what is `[class ^="box-"]` in css?
- `auto-fill vs auto-fit` u  

### ⚡dec3
- it is required that i should` make notes and videoNotes` in such a manner that i can refer and `revise` them `everyday`  
- interesting  

      <h1>
        <div>Text1</div>
        <div>Text2</div>
      </h1>

      🔹u should not have a block element inside  a h1 tag, instead use span tag.  

### ⚡ dec4
- `.item:nth-of-type(n)` to select the nth number of element of the class `.item`    

- started OOPS
    - abstraction 
    - inheritance
    - enscapsulation 
    - polymorphism    

### ⚡dec5
- commands in windows   `& && ||`

      🔹run commands regardless whether success or failure    
       - dir & cls & command3   
      🔹run the 2nd command only if the 1st is success
       - cd folder && dir   
      🔹run 2nd if 1st fails   
       - cd folder || echo %cd%

- 2 pyhton files sharing          
- free api
  - lorem picsome
  - json placeholder


#### Four hash Heading 
<details>
    <summary>👉objects in Javascript before oops</summary>
    - objects in js  
    
          ---  
          // console.log('hi hello')

          const person1 = {
              //properties- k:v
              name: "adam",
              lastName : "wonders",
              age :31,
              
              //methods r functions
              sayHi : ()=>console.log(`hello there i am '${name}'`),
              sayHi2 : ()=>console.log(`hello there i am  '${this.name}'`),
              sayHi3 : ()=>console.log(`${this}`),
              sayhi4(){return this}
          } 

          const person2 = {
              //properties- k:v
              name : "Bri",
              lastName : "Moon",
              gender : 'female',
              age :25,
              //methods r functions
              sayHi : function(){console.log(`hello there i am '${name}'`)},
              sayHi2 : function(){console.log(`hello i m '${this.name}'`)}  ,
              sayHi3(){console.log(`combined method also ${this}`)}
          } 

          person1.sayHi()
          person1.sayHi2()
          person1.sayHi3()
          console.log('               ')

          person2.sayHi()
          person2.sayHi2()
          person2.sayHi3()

          console.log('               ')

          console.log(person1.age)
          console.log(person2.lastName)
          console.log(person2.age)
          console.log(person1.name)
          console.log('               ')
          console.log(person1.sayhi4())
          // so key takeways
          // arrow function can cause problem for methods inside a Object, u have write function syntax properly
          // can combine k:v and fun1(){ur func code} 
          // avoid using ()=> syntax in objects
          //observe how I got the data of this keyword

</details>


<details>
<summary>👉Next</summary>
      
    ---  
    start from here
    copy this template
    ---
</details>


<details>
<summary>👉2 files of python</summary>
      
    ---  
    start from here
    copy this template
    ---
</details>

### ⚡dec6

- use of constructor in js and python
- setInterval takes a function 
- if u hav closed the terminal and see what task were running through ur terminal   
  `tasklist`   
  `tasklist /FI "IMAGENAME eq j*"`  
   taskill `pid`
- oops in python


### ⚡dec8
- return vs print in python or any language
- without Constructor

      ✨ in Javascript  

        const car1 = {
        make: "Toyota",
        model: "Corolla",
        year: 2023,
        start: function() {
          console.log(`${this.make} ${this.model} is starting...`);
        }
      };  

      console.log(car1.make); // Toyota
      car1.start(); // Toyota Corolla is starting...  

      👉This approach is fine for one or two objects but becomes   
      repetitive when you need multiple objects with similar properties.    

      ✨in python
       
       car2 = {
         "make": "Honda",
        "model": "Civic",
        "year": 2022,
        "start": lambda: print("Honda Civic is starting...")
        }

        car2["start"]()  # Honda Civic is starting...

      👉In Python, you cannot directly define a method (def) inside a dictionary like in    JavaScript objects.  
      However, you can define it using a callable lambda or  by assigning a function explicitly to a key in the dictionary.


      ✨  
        'def start_audi():
            print("Audi A4 is starting...")
      

            car7 = {
          "make": "Audi",
          "model": "A4",
          "year": 2017,
          "start": start_audi
            }

       car7["start"]()  # Audi A4 is starting...

- with Constructor  

      ✨in Javascript  

      class Car {
        constructor(make, model, year) {
          this.make = make;
          this.model = model;
           this.year = year;
         }

      start() {
        console.log(`${this.make} ${this.model} is starting...`);
          }
      }


      const car3 = new Car("Ford", "Focus", 2021);
      const car4 = new Car("Nissan", "Altima", 2020);
      const car5 = new Car("Chevrolet", "Malibu", 2019);

      car3.start(); // Ford FocusCorolla is starting...
      car4.start(); // Nissan Altima is starting...
      car5.start(); // Chevrolet Malibu is starting...  

      ✨in Python  
       
       class Car:
          def __init__(self, make, model, year):
            self.make = make
            self.model = model
            self.year = year

          def start(self):
            print(f"{self.make} {self.model} is starting...")  
             
      car6 = Car("BMW", "3 Series", 2018)

- in python Classes `__`hides the variable/function.
- `def __init__(self,para1,para2)` is auto function that runs immediatley as the class object is created.     
     
 

- Comparison
  |Constructor|No Constructor|
  |---|---|
  |Resuseable class simplifies object creation|Each Objecy is manually created.|
  |Consistency is maintained|Properties and methods are written repeatedly for each object.|
  |changes can be made in one place(in class) instead of evry object|Code--> difficult to maintain|


### ⚡dec9
- #### var let const in Js    

  <details>
    <summary>Click</summary>
    
        ✨   
        <script>  
          var name = 'adam';
          console.log(typeof(name), name)   // string adam

          name = 7
          console.log(typeof(name) , name)  // string 7 
          👉why still string , lets explore with let and const


          let name1 = 'bob';
          console.log(name1 , typeof(name1))  // bob  string          

          name1 = 9 
          // let name1 = 9   //redeclaration not allowed 
          //let name1 = 'bob2'  // reassignment is allowed
          console.log(name1,typeof(name1));  
  
          const name2 = 'Chinook' 
          console.log(name2,typeof(name2)); 
          
          // name2 = 11; // error  
          const name2 = 11 // error --> already been declared 
          console.log(name2, typeof(name2)) 
  
          //therfore typeScript is usefull       
        
        </script>  
  </details>      


- try except finally in python

- #### abstraction and enscapsulation go hand in hand  
  - 

- can we re assign values to a class object ,how to prevent it?  

### ⚡ dec11

- due to fever ,i lost my streak of commiting continously ,anyways

- glass morphism

    <details>
    <summary>GlassMorphism</summary>
             
      🔹background-color: transparent;  
         backdrop-filter: blur(10px)   // higher value higher blur

      🔹rgba change the 'a'     
         if you want to use some other color;
      🔹 also use -webkit format for other browsers   

    </details>


### ⚡dec12

- id in python

- default parameters 
- visualisation of class execution in python
- __private 
