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
  
 
