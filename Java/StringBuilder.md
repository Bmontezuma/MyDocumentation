# ***stringBuilder***

The ***`StringBuilder`*** class in Java represents a String-like character sequence that is mutable, whereas objects of the ***`String`*** class are immutable. This provides an alternative to the ***`String`*** class when it’s a requirement to change a character sequence once it is defined.

It is similar to another class, ***`StringBuffer`***, but it is faster in most circumstances. The difference between ***`StringBuilder`*** and ***`StringBuffer`*** is that ***`StringBuilder`*** is not thread-safe. ***`StringBuilder`*** offers no guarantee of synchronization and should not be used across multiple threads.

## ***Syntax***

```java
StringBuilder s1 = new StringBuilder();
StringBuilder s2 = new StringBuilder(capacity);
StringBuilder s3 = new StringBuilder(sequence);
```
A ***`StringBuilder`*** can be created in the following ways:

- Calling the constructor with no arguments creates a ***`StringBuilder`*** with no contents and a capacity of 16 characters.
- Calling the constructor with the int argument, capacity, creates a StringBuilder with no contents and a capacity of capacity characters.
- Calling the constructor with a sequence argument that is either a String or a CharSequence creates a StringBuilder with contents and capacity equal to the specified String or CharSequence.

## ***Example***

The following example creates a StringBuilder with a specified String and then changes it by appending another String:
```java
import java.util.*;

public class Example {
  public static void main(String[] args) {
    StringBuilder str = new StringBuilder("Hello");
    System.out.println(str.toString());
    str.append(" World!");
    System.out.println(str.toString());
  }
}
```
This produces the following output:
```java
Hello
Hello World!
```
Below is a list of methods used by the ***`StringBuilder`*** class:

***`.append()`***: Appends the string representation of its argument.

***`.capacity()`***: Returns the current space available for characters in the StringBuilder.

***`.delete()`***: Removes a substring from the contents of a StringBuilder and returns the modified object.

***`.deleteCharAt()`***: Removes the character at the specified index from the contents of a StringBuilder and returns the modified object.

***`.indexOf()`***: Returns the index of the first occurrence of a substring in the StringBuilder or -1 if none are found.

***`.insert()`***: Places a sequence of characters into a StringBuilder and returns a reference to the object.

***`.lastIndexOf()`***: Returns the index of the last (rightmost) occurrence of a substring in the StringBuilder or -1 if no substring is found.

***`.length()`***: Returns the number of characters currently in the StringBuilder.

***`.replace()`***: Switches a substring in a StringBuilder with a specified String and returns the modified object.

***`.reverse()`***: Returns a modified StringBuilder object with its character sequence rearranged in the opposite order.

***`.substring()`***: Returns a String object representing a substring of the character sequence currently in a given StringBuilder.

***`.toString()`***: Returns a String representation of the character sequence currently in a given StringBuilder.

