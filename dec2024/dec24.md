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

- `id` in python provide the address of the object.

- default parameters 
- visualisation of class execution in python
- `__` private 
- in cmd `. code`


### ⚡dec13
- <details>
    <summary>Topic1</summary>

      🔹wrtie ur thing here  
        
  </details>


- <details>
    <summary>Topic2</summary>

      🔹wrtie ur 2nd thing here  
        
  </details>
- <details>
    <summary>Jupyter</summary>

     ### **Jupyter Notebook vs. JupyterLab**    "non- block syntax"

    | **Feature** | **Jupyter Notebook**| **JupyterLab**|
    |--------------------|---------------------------------------|---------------------------------------|
    | **UI**| Simple, single-document.| Modern, multi-tab, customizable.|
    | **File Handling** | Basic.| Advanced with drag-and-drop.|
    | **Extensions** | Limited, manual setup.| Built-in manager, easier to use.|
    | **Performance**| Lightweight, beginner-friendly.| Heavier, ideal for multitasking.|
    | **Terminal**| Not supported.| Fully integrated (see below).|

    ### **How to Use Terminal in JupyterLab**
    1. Open **JupyterLab** (`jupyter lab`).
    2. In the file browser, click **“+”** or the launcher.
    3. Under **"Other"**, select **Terminal**.
    4. Run shell commands directly within the terminal tab.        
  </details>

### ⚡dec14

- explored decorator 
- `__name__ =__main__` 
- assert in python for validation

### 
- win+x uu 
- <details>
    <summary>input str/nostr</summary>

      def wrtdis(v):
        res = str(v)
        print(res)

      but if u give input withput " " , it will consider it as a unknow variable.  
      undefined variable.


      to tackle this ,  
      at the time of taking input change it there itself. 

      var1 = str(input())

      wrtdis(var1)          
        
  </details>


### ⚡dec19

- `echo ~` to echo the pwd in linux.
- |interactive|Problem's|Videoral|
  |---|---|---|
  |LabEx|HackerRank|tutedude|
  |ProgramizPro|HackerEarth|30daysCode|
  |Excersim||FreeCodeCamp|

### ⚡dec20
- facinf dilama strong complusion to buy labEx for interatice learning ,please forget labEx for a while promise once learnt backend ,we will have it
- start adding for labex fee


### ⚡dec22

- <details>
    <summary>Try,Except</summary>

      🔹universal error handler   
          
        try:  
          print(1/0)
        except Exception as e:
          print(f"an error occured:{e}")
        
  </details>

- <details>
    <summary>super().__init__()</summary>

      🔹wrtie ur thing here  
        
  </details>


### ⚡dec23  

- <details>
    <summary>✨oops Inheritance</summary>

      class A:
        def speak(self):
         print("from class A")

      class B(A):
        def speak(self):
          print("from class B")

      a1 = A()
      b1 = B()

      a1.speak()  # Calls the speak method from class A
      b1.speak()  # Calls the overridden speak method from class B   

    x, But i dont want the method of class A not class B when speak()  
     
      class A:
        def speak(self):
          print("from class A")

      class B(A):
        def speak(self):
          A.speak(self)  # Explicitly call A's speak method

      a1 = A()
      b1 = B()

      a1.speak()  # Output: from class A
      b1.speak()  # Output: from class A 

    method2:-use super()

      class A:
        def speak(self):
           print("from class A")

      class B(A):
         def speak(self):
           super().speak()  # Call the parent class's method

      a1 = A()
      b1 = B()

      a1.speak()  # Output: from class A
      b1.speak()  # Output: from class A   

   method3 -Do Not Define speak in B  

      class A:
        def speak(self):
          print("from class A")

      class B(A):
        pass  # Inherit everything from A without modification

      a1 = A()
      b1 = B()

      a1.speak()  # Output: from class A
      b1.speak()  # Output: from class A   

   method4-  Dynamically Assign speak from A to B

       class A:
        def speak(self):
          print("from class A")

        class B(A):
          pass

      B.speak = A.speak  # Dynamically assign A's speak method to B

      a1 = A()
      b1 = B()

      a1.speak()  # Output: from class A
      b1.speak()  # Output: from class A    

        
  </details>

### ⚡dec24

- python interpretor
    - `ctlr + D`;`ctrl +Z`;`quit()`;`exit()`
    - interpretor reads a python file 
    - interpretor on its own  can also be used for simple instructions.


- <details>
    <summary>👉MRO and using Super</summary>

      🔹observe the below code  
       
        
  </details>

### ⚡dec25
  

### ⚡dec30
- learning mysql in linux terminal
- service vs systemtl ?
- mysql was not starting in labEx,because there was a mysql already installed and it was contradicting the new version.
- to run a `.sh` file   
    - `bash fileName.sh `  make sure it has proper permission.
- make adocker image of mysql database on your own.
- `pip list ` in cmd.
- what is virtual everything 
- `if __name__ =__main__`

- way to practice sql 
  - labEx proper env along with ide and web porting.
  - play with dockerr terminal
  - Incus try it for 30 mins.  
- <details>
    <summary>make adictionary from 2 arrays</summary>

      🔹
    
</details>

### ⚡dec30  
- 🖥️ Using mysql and python on labEx machine ...did database things✨  
- <details>
  <summary>sql cmnds</summary>
          
      - INSERT INTO table_name (column1, column2, column3)  
        VALUES 
        (value1a, value2a, value3a),
        (value1b, value2b, value3b);   

      - SELECT * FROM sidetable ORDER BY id;
      - UPDATE sidetable
        SET id = 103
        WHERE id = 102 AND age = 29;
    
  
  </details>
- <details>
    <summary> checkout the code here...</summary>

      🔹wrtie ur thing here 

      👉MariaDB [test_DB]> show TABLES;
      +-------------------+
      | Tables_in_test_DB |
      +-------------------+
      | maintable         |
      | sidetable         |
      +-------------------+
      2 rows in set (0.000 sec)

      👉MariaDB [test_DB]> desc maintable;desc sidetable;
      +-------+-------------+------+-----+---------+-------+
      | Field | Type        | Null | Key | Default | Extra |
      +-------+-------------+------+-----+---------+-------+
      | id    | int(11)     | YES  |     | NULL    |       |
      | name  | varchar(50) | YES  |     | NULL    |       |
      | game  | varchar(50) | YES  |     | NULL    |       |
      +-------+-------------+------+-----+---------+-------+
      3 rows in set (0.001 sec)

      +--------+--------------+------+-----+---------+-------+
      | Field  | Type         | Null | Key | Default | Extra |
      +--------+--------------+------+-----+---------+-------+
      | id     | int(11)      | YES  |     | NULL    |       |
      | age    | int(11)      | YES  |     | NULL    |       |
      | role   | varchar(100) | YES  |     | NULL    |       |
      | salary | varchar(100) | YES  |     | NULL    |       |
      +--------+--------------+------+-----+---------+-------+
      4 rows in set (0.000 sec)



      👉MariaDB [test_DB]> SELECT * FROM maintable;SELECT * FROM sidetable;
      +------+-------+-------+
      | id   | name  | game  |
      +------+-------+-------+
      |  100 | aname | agame |
      |  101 | bname | bgame |
      |  102 | cname | cgame |
      |  103 | dname | dgame |
      +------+-------+-------+
      4 rows in set (0.000 sec)

      +------+------+------------+----------+
      | id   | age  | role       | salary   |
      +------+------+------------+----------+
      |  100 |   23 | full-stack | $99,000  |
      |  101 |   25 | front-end  | $79,000  |
      |  102 |   27 | back-end   | $109,000 |
      |  103 |   29 | dev-ops    | $99,999  |
      +------+------+------------+----------+
      4 rows in set (0.000 sec) 
        
  </details>


- learn alot...GOD SPEED🏹
