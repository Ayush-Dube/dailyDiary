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

<details>
<summary>✨objects in Javascript before oops</summary>
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
<summary>Next</summary>
</details>