# **Flow of Control**

## *1.4.1 While Statement*

A **while** statement repeatedly executes a section of code, called **statement**, so long as a given condition is true. 

```Cpp
    while (condition)
        statement
```

## **Exercises Section 1.4.1**

**Exercise 1.9:** Write a program that uses a while to sum the numbers from
50 to 100.
```Cpp
#include <iostream>

int main()
{
    int v1 = 50, sum = 0;

    while (v1 < 101)
    {
        std::cout << v1 << std::endl; // Optional line too see the value of v1 for each iteration.
        sum += v1;
        ++v1;
    }
    std::cout << "The summation of the numbers from 50 to 100 is: " << sum << std::endl;

    return 0;
}
````

**Exercise 1.10:** In addition to the ++ operator that adds 1 to its operand,
there is a decrement operator (--) that subtracts 1. Use the decrement
operator to write a while that prints the numbers from ten down to zero.
```Cpp
#include <iostream>

int main ()
{
    int v1 = 10;

    while (v1 >= 0)
    {
        std::cout << v1 << std::endl;
        --v1;
    }

    return 0;
}
````

**Exercise 1.11:** Write a program that prompts the user for two integers.
Print each number in the range specified by those two integers.
```Cpp
#include <iostream>

int main()
{
    int upper = 0, lower = 0;

    std::cout << "Enter the upper value of the interval: " << std::endl;
    std::cin >> upper; 
    std::cout << "Enter the lower value of the interval: " << std::endl;
    std::cin >> lower;
    std::cout << "The numbers inside the interval are: " << std::endl;

    while (lower <= upper)
    {
        std::cout << lower << std::endl;
        ++lower;
    }

    return 0;
}
````