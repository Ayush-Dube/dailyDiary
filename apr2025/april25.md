### ⚡1april
- Constrcutor in java
- change the  setting of code runner ,so that, the output will run on ternimal ,enabling us to give input as well . Soppose it will ask us to provide 2 numbers , and then give output based on our input.

-   <details>
        <summary>    
            Explore more about Static and Non Static keyword 
        </summary>  

            ✨
            - 
    </details>

- in april I plan to 
    - to walk daily for one hour
    - learn blender
    - learn C
    - learn Java

### ⚡2apr

- Ctel + D to select one by one similar value in vs code.

- forgot to write return 0; but still running,bcoz inbuilt in newer versions of C.


### ⚡3apr
- Java
   -  Object-oriented hai → Har cheez class aur object ke around ghoomti hai.

   -  Static vs Non-Static → Agar alag-alag objects ke liye alag data chahiye, to static mat use kar.

   -  this tabhi kaam karega jab object bana hoga, static ke andar this nahi chalega.

   - Constructor use kar, setInfo() ki zaroorat nahi padti.


### ⚡4apr

- use time command before each python main.py ; time gcc ./a.out , to find the time taken for execution;

- for using return cariage use `\r,end =" "` , the end ="" is important .

### ⚡5apr
- how to finf time taken in windows terminal , by a code to get executed.(in the same way we do in linux with time python main.py)
- calling a class inside a class in java.
- what if no internet and u try to push the code to github.
- 2 terminals chating.



### ⚡8apr
- `Alt+0176` ° for degree symbol
- sequence of if-else statement matters , refer FizzBuzz Program.
- working with git and gitignore
    - observe that git init command in terminal creates a .git folder (hidden),which confirms git has intialised here
    - now make a .gitignore file and inside mention the path and file format ,use wildcards.
---      
- Keep your repos clean with .gitignore.
- Use git add -f to include ignored files only when necessary.
- For bigger projects, structure .gitignore by language and file type.
---

- Noticed extra files (`.class`, `.out`) being pushed — these are **compiled files**, not needed in the repo.
- touch a gitignore file and add the paths or file extensions to be ignored.

        Pattern	Effect
        *.class	-->Ignores .class files only in the current folder
        **/*.class -->Ignores .class files in all folders and subfolders
---
-  Only if u want ,Remove Already Tracked Compiled Files

        git rm --cached *.class
        git rm --cached *.out
        git commit -m "Removed compiled files and added .gitignore"
        git push
---
- If Ignored Files Are Needed Later

        git add -f MyProgram.class
        git commit -m "Added MyProgram.class for debugging"
        git push

    To remove it again:

        git rm --cached MyProgram.class
        git commit -m "Removed .class file"
        git push
---

### ⚡9apr

- `!= `not equal to
- ` gcc number_compare.c -o nb;./nb`
-  for loop in python to print even number using modulus , i++and continue statement;  
- nested `if`s ,if statement placed inside another if or else block.
- inPython some code  

        import time
        print('test')

        try:
            def loopme(int):
                for i in range(int):
                    if(i%2==0):
                        print(f'{i} is Even.')                    
                    else:
                        print(i)

            # loopme(20)
            loopme('m')
                
        except:
            print("Something went wrong")
---
- 
            