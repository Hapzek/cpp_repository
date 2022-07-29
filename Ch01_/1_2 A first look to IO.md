# **1.2 A first look at Input/Output**

There is not any statements to do input or output. Instead, we neeed to use an standard library. The library we will be using in this book is **iostream**. There are two types named istream and ostream. 

```
A stream is a sequence of characters read from or written to an IO device. The term stream is intended to suggest that the characters are generated, or consumed, sequentially over time.
```

## Standart Input and Output Objects.

The library defines four IO objects. 

* **Input:** object of type *istream* named **cin** (pronounced see-in).
* **Output**
    * object of type ostream named **cout** (pronounced see-out),
    * object of type ostream named **cerr** (pronounced see-err),
    * object of type ostream named **clog** (pronounced see-log).
\

    **cerr**, referred to as the *standart error*, for warning and error messages.
    \
    **clog**, for general information about the execution of the program.


### **Example code**

```Cpp
#include <iostream> // Tells the compiler we want to use the iostream library.
int main()
{
    std::cout << "Enter two numbers: " << std::endl; // "<<" its an output operator.
    int v1 = 0, v2 = 0; // defining and initializaing variables
    std::cin >> v1 >> v2; //
    std::cout << "The sum of" << v1 << " and " << v2
              << " is " << v1 + v2 << std::endl;
    return 0; 
}
```
### Let's explain more in depth what the following lines does (1.2.1),

```Cpp
    std::cout << "Enter two numbers: " << std::endl; // "<<" its an output operator.
```
The operators "<<" and ">>" needs two operands:

            std::cout << the value to print 
            std::cin >> the destiny variable

For the more complex (1.2.1) code, we can think it like math operations and the separate each operations the following way,

```Cpp
    (std::cout << "Enter two numbers: ")
    << std::endl; // "<<" its an output operator.
```
```Cpp
The first operation we are doing is (std::cout << "Enter two numers: "), then we do << std::endl to the result of the last operation.
```

In other words, we are printing the string **"Enter two numbers: "**, then we are calling the manipulator **endl**.

Let's talk about **endl**, **std::**, and **::** ,

* **endl**: It's a special value called a **manipulator**. Writing **endl** has the effect of ending the current line and flushing the buffer associated with that device. Flushing the buffer ensures that all the output the program has generated so far is actually written to the output stream, rather than sitting in memory to be written.

* **std::**: This prefix indicates that the names **cout** and **endl** are defined inside the **namespace std**. Namespaces allow us to avoid inadvertent collisions between the names we define and uses of those same names inside a library.

* **::** , it's the **scope operator**, states that we want to use the **"object"** of his right side from the **namespace** at his left side.

## Reading from a stream, **std::cin.**

In this case, we are reading instead of writting. It's almost the same logic we used with **cout**.

```Cpp
    std:: cin >> v1 >> v2; // is the same as:

    (std:: cin >> v1)
    >> v2;                // and also the same as,

    std:: cin >> v1;
    std:: cin >> v2;
```
First we **"save"** whatever we are receiving in **v1**, and then we receive a second string to save in **v2.**