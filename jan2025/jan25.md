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