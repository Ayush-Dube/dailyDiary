## 💫pep-8 guidelines

Naming Conventions:

- snake_case: Use for functions and variables (e.g., my_function, user_name).
- PascalCase: Use for class names (e.g., MyClass).
- UPPERCASE_SNAKE_CASE: Use for constants (e.g., MAX_CONNECTIONS).

Spacing:

- Use a single space around most operators (=, +=, ==, <, >).
- Use a space after commas in lists, tuples, and function arguments.
- Avoid extra spaces immediately inside parentheses, brackets, or braces.


## id | memory address



```text
+================================================================+
|       🐍 PYTHON OBJECT ID, REFERENCES & MEMORY ADDRESS          |
+================================================================+

1. 🧠 UNDERSTANDING PYTHON OBJECTS
   |
   |-- 1.1 Variable
   |      A name/reference pointing to a Python object.
   |
   |-- 1.2 Object
   |      Actual data stored and managed in memory.
   |
   |-- 1.3 Memory Address
   |      Location of an object in memory.
   |
   |-- 1.4 Object ID
          Identity assigned to an object by Python.

2. 🔍 WHAT IS id()?
   |
   |-- 2.1 Built-in Python function:
   |      id(object)
   |
   |-- 2.2 Returns the identity of an object.
   |
   |-- 2.3 Guarantees:
   |      • Unique during an object's lifetime.
   |      • Remains constant during its lifetime.
   |      • Different live objects have different IDs.
   |
   |-- 2.4 IMPORTANT:
          In CPython, id() typically represents the object's
          memory address. Python does NOT guarantee this for
          every Python implementation.

3. 📦 REFERENCES & SHARED OBJECTS

   a = [10, 20]
   b = a

   MEMORY VISUALIZATION:

       a ---------+
                  |
                  v
             +----------+
             | [10, 20] |
             +----------+
                  ^
                  |
       b ---------+

   • Both variables reference the SAME object.
   • id(a) == id(b) → True
   • a is b         → True

4. 🔄 MUTABLE OBJECTS (LIST, DICTIONARY, SET)

   a = [10, 20]
   b = a

   b.append(30)

   print(a)  → [10, 20, 30]
   print(b)  → [10, 20, 30]

   WHY?
   • append() modifies the existing list.
   • Both variables reference that same list.
   • Therefore, both observe the modification.

5. 🆕 REASSIGNMENT VS MODIFICATION

   CASE A: MODIFICATION

   a = [10, 20]
   b = a
   b.append(30)

   Result:
   a → [10, 20, 30]
   b → [10, 20, 30]

   CASE B: REASSIGNMENT

   a = [10, 20]
   b = a
   b = [100, 200]

   Result:

   a ------------> [10, 20]

   b ------------> [100, 200]

   • A new list is created.
   • b now references the new list.
   • a remains unchanged.

6. ⚖️ == vs is vs id()

   OPERATOR     PURPOSE
   ------------------------------------------------
   ==           Compares values (equality).
   is           Checks object identity.
   id()         Returns object identity.

   EXAMPLE:

   a = [10, 20]
   b = a
   c = [10, 20]

   a == c  → True
   a is b  → True
   a is c  → False

   WHY?
   • a and b reference the same object.
   • c is a separately created object.
   • Their values are equal, but their identities differ.

7. 🛠️ PRACTICAL USES OF id()

   • Debugging unexpected changes in lists/dictionaries.
   • Checking whether objects are shared.
   • Understanding references passed to functions.
   • Learning shallow copy vs deep copy.

   NOTE:
   In normal Python programming, prefer 'is' for identity
   comparisons. You rarely need id() directly.

8. 🎯 FINAL MENTAL MODEL

   VARIABLE      → Name/reference
   OBJECT        → Actual data
   MEMORY ADDRESS→ Location in memory
   OBJECT ID     → Identity of an object
   is            → Checks whether references point to
                   the same object
   ==            → Checks whether values are equal

+================================================================+
| 🚀 NEXT TOPICS TO LEARN                                        |
|                                                                |
|  1. Mutable vs Immutable Objects                               |
|  2. Shallow Copy vs Deep Copy                                  |
|  3. Python Memory Management                                   |
|  4. Garbage Collection                                        |
+================================================================+
```