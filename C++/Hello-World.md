# ***Hello World***

### ***Compile Command***
Using ***GNU***, *the compilation command* is***`g++`*** followed by the ***file name***. Here, the name of the ***source file*** is ***hello.cpp***.
```cpp
g++ hello.cpp
```
### ***Execute Command***
The ***execution command*** is ***`./`*** followed by the ***file name***. Here, the name of the executable file is ***`a.out`***.
```cpp
./a.out
```
### ***Single-line Comments***
***Single-line comments*** are created using ***two consecutive forward slashes***. The compiler ignores any text after ***`//`*** on the same line.
```cpp
// This line will denote a comment in C++
```
### ***Multi-line Comments***
***Multi-line comments*** are created using ***`/*`*** to ***begin the comment***, and ***`*/`*** to ***end the comment***. The compiler ignores any text in between.
```cpp
/* 
This is all commented out.
None of it is going to run!
*/
```
### ***Program Structure***
The ***program*** runs ***line*** by ***line***, from ***top*** to ***bottom***:

The ***first line*** instructs the compiler to ***locate*** the file that contains a ***library*** called ***iostream***. This library contains code that allows for ***input*** and ***output***.
The ***main()*** function houses all the instructions for the program.
```cpp
#include <iostream>

int main() {

  std::cout << "1\n";
  std::cout << "2\n";
  std::cout << "3\n";

}
```
### ***Basic Output***
***std::cout*** is the “***character output stream***” and it is used to write to the ***standard output***. It is followed by the symbols ***`<<`*** and the ***value to be displayed***.
```cpp
std::cout << "Hello World!\n"; 
```
### ***New Line***
The ***escape sequence*** ***`\n`*** (*backward slash and the letter n*) generates a ***new line*** in a ***text string***.

std::cout << "Hello\n";
std::cout << "Hello again\n";
