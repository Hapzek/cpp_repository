# **Exercises Section 1.2**

**Exercise 1.3:** Write a program to print Hello, World on the standard
output.

```Cpp
#include <iostream>

int main()
{
    std::cout << "Hello, World" << std::endl;
    return 0;
}
```

**Exercise 1.4:** Our program used the addition operator, +, to add two
numbers. Write a program that uses the multiplication operator, *, to print
the product instead.

```Cpp
#include <iostream>5

int main ()
{
    int var1 = 0, var2 = 0, var3 = 0;

    std::cout << "This program calculates the product of two integer numbers" << std::endl;
    std::cout << "Enter the first number:" << std::endl;
    std::cin >> var1;
    std::cout << "First number: " << var1 << std::endl;
    std::cout << "Enter the second number:" << std::endl;
    std::cin >> var2;  
    std::cout << "Second number: " << var2 << std::endl;

    var3 = var1 * var2;

    std::cout << var1 << " * " << var2 << " = " << var3 << std:: endl;

    return 0;
}
```
**Exercise 1.5:** We wrote the output in one large statement. Rewrite the
program to use a separate statement to print each operand.
```Cpp
#include <iostream>

int main ()
{
    int v1 = 0, v2 = 0;

    std::cout << "Enter two numbers: " << std::endl ;
    std::cin >> v1;
    std::cin >> v2;

    std::cout << "The sum of ";
    std::cout << v1;
    std::cout << " and ";
    std::cout << v2;
    std::cout << " is ";
    std::cout << v1 + v2 << std::endl;

    return 0;
}
```
**Exercise 1.6:** Explain whether the following program fragment is legal.
```Cpp
 // A: The program is ilegal. 

#include <iostream>

int main()
{
    int v1 = 1, v2 = 2;
    std::cout << "The sum of " << v1 << " and " << v2 << " is " << v1 + v2 << std::endl;
    return 0;
}
```