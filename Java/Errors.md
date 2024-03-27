# ***Errors***

In Java, situations where things might go wrong in the program are predominantly handled by the following subclasses of the java.lang.Throwable class: Error and Exception.

## ***Errors***
The Error class represents illegal operations that cause serious abnormalities in the program and are not recommended to catch. Some examples include the following:

- The ***`ClassFormatError`*** occurs when a class file cannot be read or interpreted.\
- The ***`IncompatibleClassChangeError`*** occurs when a base class is altered after a child class has already been initialized.\
- The ***`NoClassDefFoundError`*** occurs when the file with the class containing the main() method cannot be found.

# ***Exceptions***
The Exception class refers to abnormal and unexpected events that disrupt the flow of the program but can be reasonably handled by a catch-statement. Some examples include:

- The ***`ArrayIndexOutOfBoundsException`*** occurs when attempting to access an index that does not exist within a given array.\
- The ***`FileNotFoundException`*** occurs when a file with the specified path cannot be found.\
- The ***`NumberFormatException`*** occurs when an attempt is made to convert a string to a numeric type and the string contains non-numeric characters.\
- The ***`NullPointerException`*** occurs when attempting to use a null value in place of where an object is required.

### ***Example***
A ***`try...catch`*** block is a means for a programmer to encapsulate a block of code and “catch” a potentially-thrown Exception (but never an Error) before it halts the execution of the program.

In the example below, the code used in the try block will run until the Exception is thrown by the assignment to the c variable because division by zero, 0, is not possible. In the catch block, an ArithmeticException is thrown and yields a printed message along with details about where the Exception can be traced.
```java
class DivideByZero {
  public static void main(String[] args) {
    int a = 27, b = 0;
    try {
      System.out.println("I'm executed first!");
      int c = a / b; // This will throw an exception
      System.out.println("I'm never executed!");
    } catch (ArithmeticException e) {
      System.out.println("Exception Caught!");
      e.printStackTrace();
    }
      System.out.println("Done!");
  }
}
```
When a programmer needs to handle more than one type of error, there are two common ways to do so, as follows:
```java
// Handle different errors separately
try {

} catch (Exception1 e) {

} catch (Exception2 e) {

}

// Handle different errors in the same way
try {

} catch (Exception1 | Exception2 e) {

}
```

# ***Errors***
***`ArithmeticException`*** - 
Occurs when an arithmetic operation yields an error.

***`ArrayIndexOutOfBoundsException`*** - 
Occurs when attempting to access an index that does not exist within a given array.

***`ClassFormatError`*** - 
Occurs when a class file cannot be read or interpreted.

***`ConcurrentModificationException`*** - 
Occurs when an item is removed or added from iterable content during iteration.

***`FileNotFoundException`*** - 
Occurs when a file with the specified path cannot be found.

***`IncompatibleClassChangeError`*** - 
Occurs when a base class is altered after a child class has already been initialized.

***`InvalidClassException`*** - 
Occurs when the Serialization runtime detects a problem with a class.

***`NegativeArraySizeException`*** - 
Occurs when an application tries to create an array with negative size.

***`NoClassDefFoundError`***
Occurs when the file with the class containing the main method cannot be found.

***`NullPointerException`*** - 
Occurs when attempting to use a null value in place of where an object is required.

***`NumberFormatException`*** - 
 Occurs when an attempt is made to convert a string to a numeric type and the string contains non-numeric characters.

***`StringIndexOutOfBoundsException`*** -
Occurs when a String method tries to use an index that is either negative or greater than the size of the string.

***`TypeNotPresentException`*** - 
Occurs when an application tries to access a type using a string representing the name of the type, but no definition for the type with the specified name can be found.
