# Cpp

Code editor : [Visual Studio Code](https://code.visualstudio.com/download)

Here is the [support page for c++ compiler](https://en.cppreference.com/w/cpp/compiler_support) 

Compilers :
 1. [GCC + Clang](https://winlibs.com/)
 2. [MSVC](https://visualstudio.microsoft.com/downloads/)
 
**Learnings:**

* In C++, a statement is a unit of code, in simple its a line of code. It terminated with a semicolon.
* An expression is something that can return any value, which can be a part of statement or an entire statement. Eg: x = 42; (both expression and statement). An expression can also contains operators and parantheses.
* **Identifiers:**
  * Identifiers provide readable names.
  * In C++ identifiers made of Latin ISO aplhabetes lower(a-z) and upper(A-Z), 10 western alpha numericals (0-9) and an ASCII underscore (_).
  * An Identifier may not begin with numeral.
  * One cannot use reserved (keywords, alternative tokens) as identifiers.
  * Case sentitive (Az, aZ)
  * Current standards allow identifiers to be of any length, although only first 63 characters are checked for uniqueness.
  * And only the first 31 characters are guaranteed for external identifiers, so in pratice keep the identifiers under 31 characters long.
  * Initial underscore for the identifiers are reserved for system identifiers, so avoid it.
* **Variables:**
   * int i {} --> variable datatype **integer**, name as **i**, {} intializes with an **initial value as 0**.
   * int i {12} --> intializes with an **initial value as 12** (A better way to intialize).
   * int i = 12 --> intializes with an **initial value as 12** (An old way from C).
   * const int i {12} --> **const int** is the variable type now and **const** tells the compiler, once the variable is defined the value cannot be changed once defined.
   * auto i = 47 --> **auto** allows the compiler to decide the type of the variable. there should be some value needed to identify the datatype.
* **Pointers:**
   * int *ip; --> This is the pointer definition.
   * A pointer is a variable that holds address of another variable.
   * From above, the pointer is named as ip and its type is pointer to int. Memory is allocated to pointer but not int.
   * ip = &x; --> Assigns address of x to a pointer ip. **&** is called reference operator.
   * y = *ip; --> * is the dereference operator. We access the value pointed by the pointer.
 * **Reference:**
    * int &y = x; --> This is reference declaration.
    * The value of the reference is always the value of the referred variable.
    * No syntax for changing the refernce, once its declared the value cannot be changed to a different variable, it always refers to the same variable. Eg : in pointers, from above *ip is pointing to x, we can change it to ip = &y, now *ip is pointing to y.
    * So if you use y = z; then the x value is changed to z, since its being referenced.
    * Reference is not an object or a pointer, its a trick of a syntax which is dangerous to use and also debug.
    * Its advisable to use a **const** for the reference, so that the value cannot be changed further.
  
 * **Conditionals:**
    * A conditional statement allows you to run one block of code or another based on a condition.
    * if (condition) {
          statement-block;
      }
      This is an example of conditional statement in C++, if the condition is true, then the statement is executed.
      If the condition is false, the flow continues without executing the statement-block.
    * An **if** statement may also have **else**, in which if the **if** condition is false, then the **else** condition based statement-block is executed.
    * Turnary conditional operator :
       * auto s = x > y ? "yes" : "no";
       * What it does here is it evalutes the condition, and the ? seperates the condition from the results.
       * if the condition is true, it returns the value and if the condition is false, it returns the second value.
     
 * **Loops :**
    * **While**
       * The basic while loop looks like a simple if statement. In this case the statement-block will execute repeatedly until the condition is false.
       * while (condition) {
             statement-block;
         }
      * To break the loop in between, you can use **break** keyword at a specific condition inside the loop.
      * To skip one loop execution, you can use **continue** keyword at a specific condition inside the loop, and continue execution for the rest.
   * **do-whille**
      * The only difference is, in the beginning you have do and the end of the loop, you have while
      * do {
             statement-block;
         } while (condition);
      * But the major difference is, in while the condition is checked first then statements are exeucted, so the chances are that if the condition is false, the statements are never executed (zero times)
      * Where as in do-while, the statements are executed atleast once, thereafter condition is checked.
      * While loop is entry controlled loop, do-while is exit controlled loop.
    * **For**
       * There are two types, one inherited from C and other is from C++.
       * for (int i {0}; i < 5; ++i) { // for (Initializer, condition, increment)
            statement-block;
         }
       * Another type is range based for loop, which has been added since C++ 11.
       * for (int i : {0,1,2,3,4,5,}) { // for (range declaration : range expression)
            cout << i << ' ';
         }
       * range declaration is a variable whose type is the same of the element of the sequence represented by range expression. Often uses the auto specifier for automatic type.

