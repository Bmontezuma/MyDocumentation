# ***User Input***

The Scanner class is used to get user input, and it is found in the ***`java.util`*** package.

## ***To use the Scanner class***:

- Import the Scanner class at the top of the file.
- Create a Scanner object.
- Use a method from the Scanner class.

## ***To import the Scanner class, add at the top of the file***:
```java
import java.util.Scanner;

In our example, we will use the .nextLine() method, which is used to read Strings:

import java.util.Scanner;                         // 1. Import the Scanner class

class Main {
  public static void main(String[] args) {
    Scanner myObj = new Scanner(System.in);       // 2. Create a Scanner object

    System.out.println("Enter your user name");

    String userName = myObj.nextLine();           // 3. Read the user input with .nextLine()

    System.out.println("The username is: " + userName);
  }
}
```
Here, the user can enter some text in the terminal, press enter, and that string will get stored in the variable userName.

## ***Input Types***
In the example above, we used the ***`.nextLine()`*** method, which is used to read Strings. To read other types, look at the table below:

## ***Method***
***`.nextBoolean()`***	Reads a boolean value from the user

***`.nextByte()`***	Reads a byte value from the user

***`.nextDouble()`***	Reads a double value from the user

***`.nextFloat()`***	Reads a float value from the user

***`.nextInt()`***	Reads a int value from the user

***`.nextLine()`***	Reads a String value from the user

***`.nextLong()`***	Reads a long value from the user

***`.nextShort()`***	Reads a short value from the user
