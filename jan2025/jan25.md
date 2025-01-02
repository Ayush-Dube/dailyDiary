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