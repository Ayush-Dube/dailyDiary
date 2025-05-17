### ⚡may1

#### Constructor in java
  - to initialize a new objects of a class ,automatically.
  - a specail method which ,    
     - has no return type,
     - is public most of the time (except singleton)     
     - starts with capital letter ,same name as the class
  - a construtor can be overloaded with paramaeters
  - if no constructor is defined , java provides with a default construtor.


### ⚡may9

- exception handling in java 

✅ 1. Every risky code needs its own try-catch:
In Java, exceptions are caught only inside try-catch blocks.
If any line (like nextInt()) is outside a try-catch, → exception will NOT be caught → program crashes.

👉 Solution:

Always wrap every risky operation (input, division, etc.) inside try-catch.

Or group related risky code in one try-catch block.

Example:

      try {
         int num = scn.nextInt();
      }
       catch(Exception e) {
         System.out.println("Handled input error: " + e);
      } 
       
✅ 2. Scanner.nextInt() leaves invalid input in the buffer → causes repeat errors:
When user enters invalid input (like a letter instead of a number) → nextInt() throws InputMismatchException → BUT does not remove that bad input from the buffer.

➡️ Next call to nextInt() → immediately fails again → leads to error repeating instantly without waiting for input.

👉 Symptom you saw: "prompt printed twice back to back."

👉 Solution:
After catching input error → always call scn.nextLine() inside catch to clear the buffer.

✅ This removes the invalid token, so next input works fine.   
 
         catch(Exception e) {
         System.out.println("error: " + e);
         scn.nextLine();  // clears invalid input
      }

✅ 3. Global / Universal Exception Handler (Thread.setDefaultUncaughtExceptionHandler):
In Java, you can set a global uncaught exception handler using:   

            Thread.setDefaultUncaughtExceptionHandler((t, e) -> {
         System.out.println("Global handler caught: " + e);
      });

BUT:

❌ This handler only catches exceptions not already caught → it runs AFTER thread dies → cannot recover or prevent program exit.

✅ It is useful for logging/reporting crashes, not for flow control.

👉 You CANNOT replace local try-catch with global handler if you want program to continue running.

✅ 4. Division by Zero & Random 0 handling:
Since you're dividing num / randNum and randNum is random 0-5, → sometimes randNum becomes 0 → triggers ArithmeticException (divide by zero)

✅ This needs to be inside try-catch too.

✅ 5. Input prompts & input errors must be independently handled:
Your program asks:

input number

input 1/0 to continue

Each of these inputs can fail separately → each needs its own try-catch!

Mistake: having select = scn.nextInt() outside try-catch → → leads to crash when invalid input (like a letter) is entered.

👉 Solution:

      try {
      int select = scn.nextInt();
      doKaro = (select == 1);
      scn.nextLine();  // clear newline
      }
         catch(Exception e) {
      System.out.println("Invalid select input: " + e);
      scn.nextLine(); // clear bad input
      doKaro = false; // default exit on bad input
      }   

✅ Now program doesn't crash if user types a letter instead of number.

✅ 6. Java Exception Handling works at block level, not method/class level:
❌ Java doesn’t automatically “catch everything in a method” unless you explicitly wrap that block inside a try-catch.

There’s no “global try-catch” for a method like in some other languages.

✅ Every risky line must be explicitly inside some try-catch block.

🏆 Final improved code structure (clean, handles all cases):  
 
      import java.util.Scanner;
      import java.util.Random;

   class Main {
   public static void main(String[] args) {
      Scanner scn = new Scanner(System.in);
      boolean doKaro;

      do {
         try {
         System.out.print("enter a number: ");
         int num = scn.nextInt();

         Random random = new Random();
         int randNum = random.nextInt(6);  // 0 to 5
         double res = num / randNum;       // might throw ArithmeticException

         System.out.println("Random number: " + randNum);
         System.out.println("Result: " + res);
         } catch (Exception e) {
         System.out.println("An error occurred: " + e);
         scn.nextLine(); // clear bad input
         }

         try {
         System.out.print("enter 1 to continue or 0 to exit... -> ");
         int select = scn.nextInt();
         scn.nextLine(); // clear newline
         doKaro = (select == 1);
         } catch (Exception e) {
         System.out.println("Input error: " + e);
         scn.nextLine(); // clear bad input
         doKaro = false; // exit on bad input
         }

      } while (doKaro);

      scn.close();
      }
      }


✅ This code:

Handles wrong input for number

Handles division by zero

Handles wrong input for continue/exit

Doesn’t print duplicate prompts

Doesn’t crash

Logs all exceptions

💥 Takeaways:
Java requires explicit local try-catch for each risky operation.

Scanner’s nextInt() → leaves invalid input in buffer → must call nextLine() inside catch.

Global exception handler useful for logging, but not for preventing crash/recovery.

Division by zero must be handled if divisor might be zero.

Every independent input needs separate error handling.

📌 Tips for future:
✅ Always flush invalid input with scn.nextLine()
✅ Always wrap every nextInt()/nextDouble() in try-catch
✅ Don’t rely on global handler for keeping program alive
✅ Avoid mixing different scanner input types unless you manage buffer carefully

### ⚡may16

#### sqlJoins
- inner 
- left 
- right
- self

      //syntax for joins
      SELECT table1.col1,table1.col2,table2.colx,table2.coly
      FROM table1 ____JOIN table2
      ON table1.col2 = table2.colx

      