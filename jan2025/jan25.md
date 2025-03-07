### ⚡jan1 
- Happy New 2025
-   <details>
      <summary>mysql ouput to a file</summary>     

        🔹In the command echo "SHOW TABLES;" | mysql -u root -p mysql > ~/project/  system_tables.txt, the execution order is as follows:  
        
        - echo "SHOW TABLES;" runs first, generating the string SHOW TABLES; to be sent through the pipe.
        
        - The pipe (|) takes the output from echo and sends it as input to the MySQL client.
        
        - The MySQL command (mysql -u root -p mysql) runs concurrently with echo, waiting for input while prompting for a password due to the -p option.
        
        - Output redirection (> ~/project/system_tables.txt) occurs after the MySQL command executes, saving the results of SHOW TABLES; to the specified file.
        
        This sequence illustrates how piped commands execute in parallel, with the first command producing output that feeds into the second command.

        🔹2nd Approach
            👉 mysql -u root -p -e "SHOW TABLES;" mysql > ~/project/system_tables.txt   

            - Replace root with your MySQL root username (if different).
            - Enter the password when prompted.
            - The -e flag allows you to execute SQL statements directly from the command line.   

            - The mysql -u root -p -e "SHOW TABLES;" part executes the SQL command SHOW TABLES;.
            - By adding mysql after the SQL command, we specify the database (in this case, the mysql system database) where the SHOW TABLES; command should be executed.

            - If you don’t specify the database, MySQL won’t know where to execute the SHOW TABLES; command, and you'll get an error like: NO database selected

            🔹If the database is named test_DB, you simply replace mysql with test_DB   

                mysql -u root -p -e "SHOW TABLES;" test_DB > ~/project/system_tables.txt  

            🔹If you want to copy the contents of the maintable from the database test_DB to a file table.txt  
            👇  
            mysql -u root -p -e "SELECT * FROM maintable;" test_DB > ~/project/table.txt

            Explanation:
            mysql -u root -p: Connects to MySQL as the root user.
            -e "SELECT * FROM maintable;": Executes the SQL query to select all rows and columns from the table maintable.
            test_DB: Specifies the database where maintable resides.
            >~/project/table.txt: Redirects the output of the query to the file table.txt in the 
             ~/project directory.

             ~ represents the home directory for that user , its value is different for different users.

             Notes:
                🔻If the table has many rows or complex data, the output in table.txt might include column headers and data in a tab-separated format.

                🔻For custom formatting, you might need to tweak the SQL query or use additional tools like awk or sed.




        
  
    </details>

- `Ctrl + L` to clear mysql terminal/command line 
- import in Pyhton
    - import sideMDL  
      - sideMDL.method1()  
      - sideMDL.method2() 
    - from sideMDL import method1,metho2
    - from sideMDL import *
    - after import sideMDL, if unsure about existing methods do `dir(sideMDL)`
    - from sideMDL import method1 as m1, method2 as m2  

        m1()   
        m2()
    
- `if __name__ == '__main__'`   write this in the moduleFile, code after this line will not run   
   in the hero file (i.e main file).

- Virtual Environment in python 
    - seperate independent environment having different versions os softwares.  
      `python -m venv anyName`  
      for activating the env   
      windows 
      `anyName\Scripts\activate.bat` -cmd 
      `anyName\Scripts\Activate.ps1` -powershell, but give Execution policy  
      linux  
      `source anyName/bin/activate`
    - `echo %PATH%`
    -  `pip freeze > requirements.txt`
    - give this txt file to fellow developer and they can install it   
      `pip install -r requirements.txt`
    - mysql is a software like python. not a package
    - mainly for managing pip packages .
    - inside a new env if u do `pip list ` it should be empty.
    - for powershell and vscode terminal remember to give Execution Policy.
    - `Set-ExecutionPolicy RemoteSigned -Scope Process` this allows to operator for current session, if u close the window it will reset to default.
    - in some cases the virtual module itself might be outdated ,mainly in linux  
      in that case do `sudo apt update` then install the `python virtualenv ` itself   
      then do , the venv cmd for creating virtual enviornment. 


### ⚡jan2
 
 - databasE names are case-sensitive;for end of query use`;`  
 - `mysqladmin` is used for performing administrative operations   
    - creating/droping databases
    - server status  
    - shutting down mysql servers  
    - managing user accounts
 - `mysqladmin -u root -p create myDB_name`
 -  
 - select
    - `SELECT VERSION();`
    - `SELECT DATABASE();`
    - `SELECT USER();`
 - SHOW 
    
- cpu ram ussage
  
      # print("cpu ram")
      import time 
      import psutil

      def display_usage(cpu_usage,mem_usage,bars=50):
          cpu_percent = (cpu_usage/100)
          cpu_bar = '*'* int(cpu_percent * bars) + "-" *(bars -int(cpu_percent * bars))
          mem_percent = (mem_usage / 100)
          mem_bar = '*'* int(mem_percent * bars) + "-" *(bars -int(mem_percent * bars))

          print(f"\rCPU Usage: |{cpu_bar}|{cpu_usage}%  ",end='')
          print(f"MemoryRAM: |{mem_bar}| {mem_usage}% ", end="\r")


      while True:
          display_usage(psutil.cpu_percent(),psutil.virtual_memory().percent,60)    
          time.sleep(0.5) 

- next


### ⚡jan5

- my-sql-connector is like a ssh agent (maybe not) that helps u to connect to a db server that has a  
  ip address and password.

#### Windows enviornment variable 

- suppose u have just now installed python a, node and c++ on your computer and now you want to run   
  run various .py, .js ,.cpp   

      ✨
      EDIT SYSTEM Environment VARIABLE 
      


### ⚡jan6


- sql   
    - create table  

            CREATE TABLE products (
                id INT AUTO_INCREMENT PRIMARY KEY,
                name VARCHAR(100) NOT NULL,
                price DECIMAL(10,2) NOT NULL,
                description TEXT,
                weight FLOAT,
                in_stock BOOLEAN,
                created_at DATETIME DEFAULT CURRENT_TIMESTAMP,
                last_updated TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
                  );  

- `DESCRIBE products;`


### ⚡jan9

- using `gitignore` file to exclude folders that u do not require to upload to github.  
- 

### ⚡jan10

- mysql 
    - `--` for comments
    - limit with offset is used , when dealing with `pagination` on a web page .

### ⚡ jan 11

    SELECT title, price, publication_year
    FROM books
    WHERE genre = 'Technical'
    AND publication_year >= 2022
    ORDER BY price DESC;


### ⚡jan 12

- difference bwteen schema , database, table  


### ⚡jan13

<details>
    <summary> paackages </summary>

      In this lab, you have explored two fundamental concepts in Python programming: functions and modules. You have learned how to define and use functions, understand function scope, create and use modules, import specific functions from modules, and organize related modules into packages.

    You started by creating simple functions and gradually moved to more complex concepts like function scope and global variables. You then learned how to create modules to organize related functions and variables into separate files, making your code more maintainable and reusable.

    You explored different ways of importing functions from modules, including importing specific functions and using aliases. This knowledge allows you to write more concise and readable code while avoiding naming conflicts between different modules.

    Finally, you learned how to create a package, which is a way to organize related modules into a directory hierarchy. This is particularly useful for larger projects where you need to manage multiple related modules.

    These concepts of functions and modules are crucial for writing well-organized, efficient, and reusable Python code. As you continue your Python journey, you'll find these skills essential for building more complex programs and collaborating on larger projects. Remember to practice these concepts regularly and explore the vast ecosystem of Python modules and packages available to enhance your programming capabilities
</details>



### ⚡jan14

<details>
<summary>module</summary>

    # Space Math Module

      def calculate_fuel(distance):
          return distance*500

      def time_to_destination(distance, speed):
          return distance/speed

      def gravity_force(mass1, mass2, distance):
          G = 6.67430e-11
          return (G *mass1 *mass2)/(distance**2)

</details>

<details>
<summary>use import</summary>

        # Space Mission Planner

        from space_math import calculate_fuel,time_to_destination,gravity_force 

        # Mission parameters
        distance = 225000000  # km
        speed = 20000  # km/h
        planet_mass = 6.39e23  # kg
        spacecraft_mass = 15000  # kg

        # TODO: Use the imported functions to calculate mission details
        fuel_needed = calculate_fuel(distance)
        travel_time = time_to_destination(distance, speed)
        grav_force = gravity_force(planet_mass, spacecraft_mass, distance)
        # TODO: Print the mission details (fuel needed, time to destination, gravitational force)
        print("Space Mission Details:")
        print("----------------------")
        print(f"Fuel needed: {fuel_needed:.2f} liters")
        print(f"Time to destination: {travel_time:.2f} hours")
        print(f"Gravitational force at destination: {grav_force:.2f} N")

</details>

### ⚡jan15

  - Lists in Python are created using square brackets [], with items separated by commas  
  - You can add items to a list using the append() method or insert items at a specific position  
   using the insert()  
  - To remove items, you can use the remove() method or the del statement:

  tuple()

  - Tuples are created using parentheses ().
  - However, unlike lists, tuples are immutable.   
    This means you cannot change their contents after creation:
    
        >>> person = ("Alice", 25, "Engineer")
        >>> name, age, occupation = person  # Tuple unpacking   
 
 - Without the comma, Python will interpret it as a regular value in parentheses.
   
        >>> single_item_tuple = (42,)
        >>> print(type(single_item_tuple))
        <class 'tuple'>


### ⚡jan16

<details>
<summary>crud code</summary>

        missions = []
        mission_details = {}

        def add_mission(missions, mission_details, name, details):
            missions.append(name)
            mission_details[name] = details
            print("Mission added successfully!")

        def update_mission(mission_details, name, key, value):
            if name in mission_details:
                mission_details[name][key] = value
                print(f"Updated {key} for mission {name}")
            else:
                print(f"Mission {name} not found")

        def display_missions(missions, mission_details):
            print("\nAll Missions:")
            for i, mission in enumerate(missions, 1):
                print(f"{i}. {mission}")
                for key, value in mission_details[mission].items():
                    print(f"   {key}: {value}")
                print()

        def list_astronauts(mission_details):
            all_astronauts = set()
            for mission in mission_details.values():
                crew = mission.get('Crew', '').split(', ')
                all_astronauts.update(crew)
            return all_astronauts

        # Main menu loop (provided in the initial script)
        while True:
            print("\nSpace Mission Management System")
            print("1. Add Mission")
            print("2. Update Mission")
            print("3. Display Missions")
            print("4. List Astronauts")
            print("5. Exit")

            choice = input("\nEnter your choice: ")

            if choice == '1':
                name = input("Enter mission name: ")
                destination = input("Enter destination: ")
                launch_date = input("Enter launch date: ")
                crew = input("Enter crew members (comma-separated): ")
                details = {
                    "Destination": destination,
                    "Launch Date": launch_date,
                    "Crew": crew
                }
                add_mission(missions, mission_details, name, details)

            elif choice == '2':
                name = input("Enter mission name to update: ")
                key = input("Enter detail to update (Destination/Launch Date/Crew): ")
                value = input(f"Enter new value for {key}: ")
                update_mission(mission_details, name, key, value)

            elif choice == '3':
                display_missions(missions, mission_details)

            elif choice == '4':
                astronauts = list_astronauts(mission_details)
                print("\nAll Astronauts:")
                for astronaut in astronauts:
                    print(f"- {astronaut}")

            elif choice == '5':
                print("Exiting Space Mission Management System. Goodbye!")
                break

            else:
                print("Invalid choice. Please try again.")
</details>


### ⚡jan20

<details>
<summary>repeated Count</summary>

    from typing import List

    def count_clone_soldier(matrix: List[List[str]]):
        # Create an empty dictionary to store the count of each soldier ID
        clone_count = {}

        # Iterate over each row in the matrix
        for row in matrix:
            # Iterate over each soldier ID in the current row
            for soldier_id in row:
                # Check if the soldier ID is already present in the clone_count dictionary
                if soldier_id in clone_count:
                    # If the soldier ID is already present, increment its count by 1
                    clone_count[soldier_id] += 1
                else:
                    # If the soldier ID is not present, initialize its count to 1
                    clone_count[soldier_id] = 1

        # Iterate over the clone_count dictionary to decrement the count of each soldier ID by 1
        for soldier_id in clone_count:
            clone_count[soldier_id] -= 1

        # Remove any soldier IDs from the clone_count dictionary whose count is 0 after decrementing
        clone_count = {k: v for k, v in clone_count.items() if v != 0}

        # Return the clone_count dictionary containing the count of each soldier ID
        return clone_count



</details>

### ⚡jan24  
-  `+=`  its not =+, if u use = then + its tring to assign that value.
- using `set()` to a variable  

      - usr_set_variable = set() 
        usr_set_variable.add('apple') 
        usr_set_variable.add('apple') 
        usr_set_variable.add('apple') 
        usr_set_variable.add('banana') 
        usr_set_variable.add('banana')

        print(usr_set_variable)

        only apple and banana will print 

### ⚡jan25

- json in python 
    - only double quates
    - parsed
    - json.load vs json.loads

- 


### ⚡jan28


# Beginner vs. Industry-Level Code: Key Differences 🚀

---

## 1. **Data Storage** 💾
### **Beginner**
- Uses **JSON files** (e.g., `store.json`).
- Simple for small projects but **not scalable**.
- No support for relationships (e.g., users → posts).

### **Industry**
- Uses **databases** (PostgreSQL, MongoDB, etc.).
- Handles large datasets, transactions, and relationships.
- Supports indexing and optimized queries.

---

## 2. **Backend Framework** 🛠️
### **Beginner**
- Plain Python/JavaScript with manual file handling.
- No structure for routing or authentication.

### **Industry**
- Uses frameworks like **Django** (Python), **Express** (Node.js), or **Spring Boot** (Java).
- Built-in tools for routing, auth, and ORM (e.g., Django ORM).

---

## 3. **API Design** 🌐
### **Beginner**
- No APIs; logic in a single file.
- Direct file reads/writes.

### **Industry**
- Uses **RESTful APIs** or **GraphQL**.
- Example endpoints:  
  - `GET /api/users` → Fetch users.  
  - `POST /api/posts` → Create a post.

---

## 4. **Authentication & Authorization** 🔒
### **Beginner**
- No login system or security checks.

### **Industry**
- **JWT tokens** or **OAuth** for user authentication.
- Role-based access (e.g., admins can delete posts).

---

## 5. **Error Handling** ❌
### **Beginner**
- Basic error messages (e.g., `print("Error!")`).

### **Industry**
- Returns **HTTP status codes** (e.g., `404 Not Found`, `500 Server Error`).
- Logs errors for debugging.

---

## 6. **Input Validation** ✔️
### **Beginner**
- No checks for invalid/malicious data.

### **Industry**
- Validates inputs (e.g., email format, password strength).
- Sanitizes inputs to block **SQL injection** and **XSS attacks**.

---

## 7. **Scalability** 📈
### **Beginner**
- Crashes under heavy traffic.

### **Industry**
- Uses **load balancing**, **caching** (Redis), and **cloud services** (AWS, Azure).
- Horizontally scales across servers.

---

## 8. **Security** 🛡️
### **Beginner**
- Passwords stored in plain text (🚨 **unsafe!**).

### **Industry**
- Encrypts passwords with **bcrypt** or **Argon2**.
- Uses **HTTPS** for secure communication.

---

## 9. **Testing** 🧪
### **Beginner**
- No tests.

### **Industry**
- **Unit tests** (functions), **integration tests** (APIs), **E2E tests** (user flows).
- Tools: pytest (Python), Jest (JavaScript).

---

## 10. **Code Structure** 📂
### **Beginner**
- Single file with all logic ("spaghetti code").

### **Industry**
- **Modular architecture** (MVC, Clean Architecture):  
  - **Models**: Define database schemas.  
  - **Views**: Handle API responses.  
  - **Controllers**: Business logic.  
  - **Services**: Reusable components.  

---

## **Example: Social Media App** 🌍
### Database Tables
```sql
Users (id, name, email, password_hash)
Posts (id, content, user_id)
Comments (id, content, post_id, user_id)
Likes (id, post_id, user_id)
Followers (follower_id, following_id)