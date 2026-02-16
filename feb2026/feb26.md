## ⚡feb1
**Statring backend with Flask**

## feb2

![alt text](image.png)

![alt text](image-1.png)



## ⚡feb11

HTTP - hyper text transfer protocol 

first TCP is established then the communication is done with HTTP

http - 80
https - 443


## ⚡feb12

jinja
server template engine {{}}
`Browser → Flask → Jinja → Final HTML → Browser`

## ⚡feb 14

git remote remove origin
git remote add origin https://github.com/yourusername/new-repo.git


![alt text](image-2.png)

```powershell
(.venv) 
admin@AsusADG-Lapt MINGW64 /d/backEND_ALL/using_Python/project_101a (main)
$ deactivate

admin@AsusADG-Lapt MINGW64 /d/backEND_ALL/using_Python/project_101a (main)
$ cd .. 

admin@AsusADG-Lapt MINGW64 /d/backEND_ALL/using_Python (main)
$ cd project_102/

admin@AsusADG-Lapt MINGW64 /d/backEND_ALL/using_Python/project_102 (main)
$ ls

admin@AsusADG-Lapt MINGW64 /d/backEND_ALL/using_Python/project_102 (main)
$ ll -a
total 0
drwxr-xr-x 1 admin 197121 0 Feb 14 16:22 ./
drwxr-xr-x 1 admin 197121 0 Feb 14 16:22 ../

admin@AsusADG-Lapt MINGW64 /d/backEND_ALL/using_Python/project_102 (main)
$ python -m venv venv

admin@AsusADG-Lapt MINGW64 /d/backEND_ALL/using_Python/project_102 (main)
$ source venv/Scripts/activate
(venv)
admin@AsusADG-Lapt MINGW64 /d/backEND_ALL/using_Python/project_102 (main)
$ pip list
Package    Version
---------- -------
pip        22.3.1
setuptools 65.5.0

[notice] A new release of pip available: 22.3.1 -> 26.0.1
[notice] To update, run: python.exe -m pip install --upgrade pip
(venv)
admin@AsusADG-Lapt MINGW64 /d/backEND_ALL/using_Python/project_102 (main)
$
```


PowerShell me check karo:

```cmd
attrib .git
attrib .prakaENV
```

### 🔧 Agar manually hidden banana ho
```cmd
attrib +h .prakaENV
```

```
Git reads .gitignore top to bottom
Last matching rule wins
Negation (!) re-includes
But parent must not be ignored
```





## ⚡feb16
```python
def test():
    print("A")
    return 5
    print("B")

print(test())
```
return 5 immediately exits the function, returning 5 to the caller.


```

================ PYTHON FUNCTION & DECORATOR CORE CRUX ================

1) VARIABLES = REFERENCES
--------------------------------------------------
a1 = "gold"
b1 = 123

Variables do NOT store values.
They store references to objects in memory.

a1 ---> "gold"
b1 ---> 123


2) FUNCTION IS ALSO AN OBJECT
--------------------------------------------------
def someFun():
    return "silver"

someFun ---> function object

Function is NOT special syntax.
It is an object stored in memory.


3) FUNCTION OBJECT vs FUNCTION CALL
--------------------------------------------------
someFun      -> function object
someFun()    -> executes function

print(someFun)     -> <function someFun at 0x...>
print(someFun())   -> silver

() means EXECUTE.


4) ASSIGNING FUNCTION TO ANOTHER VARIABLE
--------------------------------------------------
x = someFun

someFun ----|
            |----> function object
x       ----|

No new function created.
Only new reference created.

x() works because x points to same function.


5) DECORATOR CORE IDEA
--------------------------------------------------
Decorator:
1) Takes a function
2) Creates wrapper function
3) Returns wrapper
4) Replaces original reference


6) BASIC DECORATOR STRUCTURE
--------------------------------------------------
def operator(func):

    def wrapper(a,b):
        res = func(a,b)
        return f"Result is {res}"

    return wrapper


7) WHAT THIS LINE REALLY DOES
--------------------------------------------------
newAdd = operator(add)

STEP 1: operator(add) runs
        func ---> original add
        wrapper created
        return wrapper

STEP 2: assignment
        newAdd ---> wrapper
        add    ---> original add


8) WRAPPER STORES ORIGINAL FUNCTION (CLOSURE)
--------------------------------------------------
wrapper remembers:
    func ---> original add

This remembering is called CLOSURE.

Closure = function remembering outer variables
even after outer function ends.


9) TWO PHASES (VERY IMPORTANT)
--------------------------------------------------

PHASE 1: WRAPPING
newAdd = operator(add)
(No numbers passed here)

PHASE 2: EXECUTION
newAdd(2,5)

Flow:
newAdd(2,5)
    ↓
wrapper(2,5)
    ↓
func(2,5)
    ↓
add(2,5)
    ↓
5
    ↓
"Result is 5"


10) CRITICAL DIFFERENCE
--------------------------------------------------
return wrapper     -> returns function object
return wrapper()   -> executes wrapper immediately

Decorator MUST return function object.


11) REAL DECORATOR SYNTAX
--------------------------------------------------
@operator
def add(a,b):
    return a+b

Python internally does:
add = operator(add)


12) FINAL CORE LOCK
--------------------------------------------------
- Functions are objects.
- Variables store references.
- Decorator returns a new function object.
- Original reference gets replaced.
- Wrapper remembers original via closure.
- Execution happens only when called.

Decorator = reference replacement + closure.


================ END OF CORE FOUNDATION =================
```