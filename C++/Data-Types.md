# ***Data Types***
![Image](https://i.pinimg.com/736x/45/ff/9d/45ff9d60d3e023b9e1b8bf118f8621c9.jpg)
## ***Overview***
***`C++`*** supports various ***`data types`*** to represent different kinds of values in memory. These ***`data types`*** have specific memory sizes and are used for storing different types of information.

## ***Data Types and Memory Size***

| Data Type   | Memory Size |
|-------------|-------------|
| `bool`      | 1 byte      |
| `char`      | 1 byte      |
| `int`       | 4 bytes     |
| `float`     | 4 bytes     |
| `double`    | 8 bytes     |
| `std::string` | 24 bytes  |

## ***Integers***
***`int`*** is used for storing ***`integer (whole) numbers`***. It typically occupies ***`4 bytes`*** of memory space and ranges from ***`-2^31`*** to ***`2^31`***.

```cpp
int year = 1991;
int age = 28;
```
## ***Doubles***
The ***`double`*** type is for storing ***`floating-point (decimal) numbers`***, requiring ***`8 bytes`*** of memory space.

```cpp
double price = 8.99;
double pi = 3.14159;
```

# ***Booleans***
***`bool`*** stores ***`boolean values`*** of ***`true`*** or ***`false`*** and typically requires ***`1 byte`*** of memory space.

```cpp
bool organ_donor = true;
bool late_to_work = false;
```

## ***Characters***
***`char`*** stores individual characters within single quotes. It usually occupies ***`1 byte`*** of memory space and ranges from ***`-128`*** to ***`127`***.

```cpp
char grade = 'A';
char punctuation = '?';
```

## ***Strings***
***`Strings`*** are sequences of characters wrapped in double quotes. The ***`std::string`*** type is used for storing text strings.

```cpp
std::string message = "good nite";
std::string user = "@sonnynomnom";
```

## ***Data Type Modifiers***
***`Data type modifiers`*** in C++ allow modifying the length or behavior of built-in data types. Common modifiers include ***`signed`***, ***`unsigned`***, ***`short`***, and ***`long`***.

## ***Constants***
***`Constants`*** are variables whose values ***cannot be changed*** during program execution. They are declared using the ***`const`*** keyword.

```cpp
const double quarter = 0.25;
```

## ***Type Conversion***
***`Type conversion`*** allows converting one data type to another. It can be done ***implicitly*** by the compiler or ***explicitly*** by the programmer using casting.

### ***Implicit Conversion***
```cpp
int weight3 = weight1; // Compiler performs implicit conversion
```

### ***Explicit Conversion***
```cpp
int weight2 = (int) weight1;
```

## ***Safe Casting***
C++ offers a safer casting method called ***`static_cast`***, performed at compile time.

```cpp
int weight2 = static_cast<int>(weight1);
```

## ***Error in Casting***
Not all types can be converted. Attempting to convert ***incompatible types*** will result in a ***compilation error***.

```cpp
std::string s = static_cast<std::string>(weight2); // Compilation error
no known conversion for argument 1 from ‘int’ to ‘std::__cxx11::basic_string<char>&&’
```

## ***Fundamental Data Types***
In C++, ***`fundamental data types`*** serve as the basic building blocks for defining variables and manipulating data. These types represent the most primitive data entities that the language can operate on.

### ***Integers***
***`Integers`*** are used to represent ***whole numbers***. They can be either ***signed*** (*able to represent both positive and negative numbers*) or ***unsigned*** (*representing only non-negative values*). Commonly used integer types include ***`int`***, ***`short`***, ***`long`***, and ***`long long`***.

```cpp
#include <iostream>

int main() {
    // Declaring and initializing integer variables
    int a = 10;           // Regular integer
    short b = 20;         // Short integer
    long c = 1234567890;  // Long integer
    long long d = 9876543210; // Long long integer

    // Displaying the values
    std::cout << "a: " << a << std::endl;
    std::cout << "b: " << b << std::endl;
    std::cout << "c: " << c << std::endl;
    std::cout << "d: " << d << std::endl;

    return 0;
}
````

### ***Character***
The ***`char`*** type is used to store individual characters. It can hold a single character from the ASCII or extended ASCII character set.

```cpp
#include <iostream>

int main() {
    // Declaring and initializing char variables
    char grade = 'A';       // Single character
    char punctuation = '?'; // Single character
    
    // Displaying the values
    std::cout << "Grade: " << grade << std::endl;
    std::cout << "Punctuation: " << punctuation << std::endl;

    return 0;
}
```

### ***Boolean***
***`Boolean`*** data type (***`bool`***) represents truth values, which can be either ***`true`*** or ***`false`***. It is used for logical operations and control flow.
```cpp
#include <iostream>

int main() {
    // Declaring and initializing boolean variables
    bool isRaining = true;
    bool isSunny = false;
    
    // Displaying the values
    std::cout << "Is it raining? " << (isRaining ? "Yes" : "No") << std::endl;
    std::cout << "Is it sunny? " << (isSunny ? "Yes" : "No") << std::endl;

    return 0;
}
```

### ***Floating Point***
***`Floating-point`*** data types (***`float`***) are used to represent numbers with fractional parts. They can store real numbers with single precision.
```cpp
#include <iostream>

int main() {
    // Declaring and initializing floating-point variables
    float pi_float = 3.14159f;  // Single precision floating-point number
    double pi_double = 3.14159; // Double precision floating-point number
    
    // Displaying the values
    std::cout << "Pi (float): " << pi_float << std::endl;
    std::cout << "Pi (double): " << pi_double << std::endl;

    return 0;
}
```

### ***Double Floating Point***
The ***`double`*** type is similar to ***`float`*** but provides higher precision, allowing for greater range and accuracy in representing real numbers.
```cpp
#include <iostream>

int main() {
    // Declaring and initializing double variables
    double temperature = 98.6; // Temperature in Fahrenheit
    double pi = 3.14159265358979; // Value of pi
    
    // Displaying the values
    std::cout << "Temperature: " << temperature << " F" << std::endl;
    std::cout << "Pi: " << pi << std::endl;

    return 0;
}
```

### ***Void***
The ***`void`*** type represents the absence of type. It is commonly used to indicate that a function does not return any value or to specify an empty parameter list.

```cpp
#include <iostream>

// Function with void return type (no return value)
void greet() {
    std::cout << "Hello, World!" << std::endl;
}

int main() {
    // Calling the greet function
    greet(); // This function doesn't return any value
    
    return 0;
}
```

### ***Wide Character***
***`Wide character`*** (***`wchar_t`***) is used for representing wide characters, capable of storing characters from a wider range of character sets, including Unicode.

These ***fundamental data types*** form the foundation of C++ programming and are essential for understanding how data is represented and manipulated in the language.

```cpp
#include <iostream>

int main() {
    // Declaring and initializing a wide character variable
    wchar_t wideChar = L'Ω'; // Unicode character Omega
    
    // Displaying the value
    std::wcout << "Wide Character: " << wideChar << std::endl;

    return 0;
}
```

## ***Derived Data Types***

In C++, ***derived data types*** are created from ***fundamental data types***. They are essential for organizing and manipulating data in more complex ways.

### ***Function***
A ***`function`*** type represents the signature of a function, including its return type and parameter types. Function types are used to declare function pointers, pass functions as arguments, and return functions from other functions.

```cpp
#include <iostream>

// Function declaration
int add(int a, int b);

int main() {
    // Calling the function and storing the result in a variable
    int result = add(3, 5);

    // Displaying the result
    std::cout << "The sum is: " << result << std::endl;

    return 0;
}

// Function definition
int add(int a, int b) {
    return a + b;
}
```

### ***Array***
***`Arrays`*** are collections of elements of the same data type, stored in contiguous memory locations. They provide a convenient way to store multiple values of the same type under a single identifier.

```cpp
#include <iostream>

int main() {
    // Declaring and initializing an array of integers
    int numbers[5] = {1, 2, 3, 4, 5};

    // Accessing and printing elements of the array
    std::cout << "Array elements: ";
    for (int i = 0; i < 5; ++i) {
        std::cout << numbers[i] << " ";
    }
    std::cout << std::endl;

    return 0;
}
```

### ***Pointer***
***`Pointers`*** are variables that store memory addresses of other variables. They allow for dynamic memory allocation, accessing memory locations directly, and creating data structures like linked lists and trees.

```cpp
#include <iostream>

int main() {
    // Declare a variable
    int num = 10;

    // Declare a pointer variable and assign the address of 'num' to it
    int *ptr = &num;

    // Display the value of 'num' and the value stored at the memory location pointed to by 'ptr'
    std::cout << "Value of num: " << num << std::endl;
    std::cout << "Value stored at the memory location pointed to by ptr: " << *ptr << std::endl;

    // Modify the value of 'num' through the pointer
    *ptr = 20;

    // Display the updated value of 'num'
    std::cout << "Updated value of num: " << num << std::endl;

    return 0;
}
```

### ***Reference***
***`References`*** provide an alternative way to access variables by providing an alias or alternative name for an existing object. They are often used as function parameters to avoid copying large objects and to enable function overloading.

```cpp
#include <iostream>

int main() {
    // Declare a variable
    int num = 10;

    // Declare a reference variable and initialize it with 'num'
    int &ref = num;

    // Display the value of 'num' and 'ref'
    std::cout << "Value of num: " << num << std::endl;
    std::cout << "Value of ref: " << ref << std::endl;

    // Update the value of 'ref', which will also update the value of 'num'
    ref = 20;

    // Display the updated value of 'num'
    std::cout << "Updated value of num: " << num << std::endl;

    return 0
```

## ***User-defined Types***

In C++, ***`user-defined types`*** allow programmers to create their own data types tailored to specific needs. These types provide flexibility and abstraction, enabling the creation of complex data structures and encapsulation of data and functionality.

### ***Class***
A ***`class`*** is a blueprint for creating objects that encapsulate data for the state (*attributes*) and operations (*methods*) that manipulate that data. Classes support features such as ***inheritance***, ***polymorphism***, and ***encapsulation***, making them a cornerstone of object-oriented programming.

```cpp
#include <iostream>

// Define a class named 'Person'
class Person {
private:
    std::string name;
    int age;

public:
    // Constructor
    Person(std::string n, int a) : name(n), age(a) {}

    // Member function to display information
    void display() {
        std::cout << "Name: " << name << ", Age: " << age << std::endl;
    }
};

int main() {
    // Create an object of class 'Person'
    Person person1("Alice", 30);

    // Call the member function to display information
    person1.display();

    return 0;
}
```

### ***Structure***
Similar to classes, ***`structures`*** are ***user-defined data types*** that allow for the grouping of variables of different types under a single identifier. However, structures do not support member functions and are primarily used for lightweight data aggregation.

```cpp
#include <iostream>

// Define a structure named 'Person'
struct Person {
    std::string name;
    int age;
};

int main() {
    // Create an object of structure 'Person'
    Person person1;

    // Initialize the members of the structure
    person1.name = "Alice";
    person1.age = 30;

    // Display information using structure members
    std::cout << "Name: " << person1.name << ", Age: " << person1.age << std::endl;

    return 0;
}
```

### ***Union***
A ***`union`*** is a special data type that allows storing different data types in the same memory location. Unlike structures, where each member has its own memory space, unions share memory among their members. This can be useful for memory optimization or when different types need to be stored in the same location.

```cpp
#include <iostream>

// Define a union named 'Number'
union Number {
    int intValue;
    double doubleValue;
};

int main() {
    // Create an object of union 'Number'
    Number num;

    // Assign values to the members of the union
    num.intValue = 10; // Assign an integer value
    // Accessing the integer value
    std::cout << "Integer value: " << num.intValue << std::endl;

    // Assign a double value
    num.doubleValue = 3.14; 
    // Accessing the double value
    std::cout << "Double value: " << num.doubleValue << std::endl;

    // Accessing the integer value again after assigning a double value
    std::cout << "Integer value after assigning double value: " << num.intValue << std::endl;

    return 0;
}
```

### ***Enum***
***`Enumerations`*** (***`enums`***) allow defining a set of named integer constants, providing a way to create symbolic names for integral values. Enums improve code readability and maintainability by replacing "magic numbers" with meaningful identifiers.

```cpp
#include <iostream>

// Define an enumeration named 'Day' with constants representing days of the week
enum class Day {
    Monday,
    Tuesday,
    Wednesday,
    Thursday,
    Friday,
    Saturday,
    Sunday
};

int main() {
    // Declare a variable of enum type 'Day'
    Day today = Day::Wednesday;

    // Switch statement to check the day of the week
    switch (today) {
        case Day::Monday:
            std::cout << "Today is Monday." << std::endl;
            break;
        case Day::Tuesday:
            std::cout << "Today is Tuesday." << std::endl;
            break;
        case Day::Wednesday:
            std::cout << "Today is Wednesday." << std::endl;
            break;
        case Day::Thursday:
            std::cout << "Today is Thursday." << std::endl;
            break;
        case Day::Friday:
            std::cout << "Today is Friday." << std::endl;
            break;
        case Day::Saturday:
            std::cout << "Today is Saturday." << std::endl;
            break;
        case Day::Sunday:
            std::cout << "Today is Sunday." << std::endl;
            break;
    }

    return 0;
}
```

### ***Typedef***
The ***`typedef`*** keyword is used to create aliases or alternative names for existing data types, improving code readability and simplifying complex type declarations. Typedefs are commonly used to define custom names for built-in or user-defined types.

```cpp
#include <iostream>

// Define a typedef for a function pointer type
typedef void (*FunctionPointer)(int);

// Define a typedef for an integer array
typedef int IntArray[5];

int main() {
    // Using the typedefs
    FunctionPointer ptr = [](int x) { std::cout << "Value: " << x << std::endl; };
    IntArray arr = {1, 2, 3, 4, 5};

    // Call the function using the function pointer
    ptr(10);

    // Display the elements of the integer array
    std::cout << "Array elements: ";
    for (int i = 0; i < 5; ++i) {
        std::cout << arr[i] << " ";
    }
    std::cout << std::endl;

    return 0;
}
```
