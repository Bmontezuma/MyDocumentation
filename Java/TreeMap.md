# ***TreeMap***

A ***`TreeMap`*** is an implementation of the Map interface, where its items are stored as key-value pairs and it is sorted either by natural ordering of its keys or through a Comparator.

A ***`TreeMap`*** differs from a ***`HashMap`*** in terms of how their contents are stored. A ***`HashMap`*** stores its keys as hashes in a hash table whereas a ***`TreeMap`*** stores its keys in a binary tree structure, which is a type of tree data structure that has at most two children nodes per parent.

While the structure of a TreeMap is more orderly, it comes as a tradeoff with speed in comparison to a HashMap. In Big-O notation, most HashMap operations run in amortized ***`O(1)`*** time; they are generally more time-efficient. Most TreeMap operations run in ***`O(log(n))`*** time and the TreeMap is generally more space-efficient due to its dynamic allocation of memory per value added.

***Note***: Complexity is a crucial factor when determining what structure to implement. For faster operations over data, aim for a HashMap. For structured and sorted operations on data, it’s best to stick to a TreeMap.

## ***Syntax***
```java
import java.util.TreeMap;

TreeMap<KeyDataType, ValueDataType> myTreeMap = new TreeMap<KeyDataType, ValueDataType>();
```
Since the TreeMap class comes from the java.util package, it must be imported in order to be used. The TreeMap is initialized with two generic types inside angle brackets < ... >. The generic data types for KeyDataType and ValueDataType can either be different or the same.

## ***Accessing Items***

Keys are used for uniquely identifying a value in a TreeMap. This allows for efficient data storage and easy access. In the example below, the course names are the keys and the teachers assigned are the values that can be accessed by passing the corresponding key into the .get() method.
```java
import java.util.TreeMap;

public class Main {
  public static void main(String[] args) {
    TreeMap<String, String> courseTeacher = new TreeMap<String, String>();

    // Add keys and values (CourseNames, Teacher)
    courseTeacher.put("History", "Ben");
    courseTeacher.put("Mathematics", "Jeanette");
    courseTeacher.put("Physics", "Lily");

    System.out.println(courseTeacher.get("Physics"));
    System.out.println(courseTeacher.get("History"));
  }
}
```
The following will be printed in the output below:
```java
Lily
Ben
```
## ***Adding Items***

Items can be added to a ***`TreeMap`*** using the ***`.put()`*** method. It accepts two parameters, a ***`key`*** and a ***`value`***, and stores them as a pair ***`({ key=value })`***.
```java
import java.util.TreeMap;

public class Main {
  public static void main(String[] args) {
    TreeMap<String, String> courseTeacher = new TreeMap<String, String>();

    courseTeacher.put("History", "Ben");
    courseTeacher.put("Mathematics", "Jeanette");
    courseTeacher.put("Physics", "Lily");

    System.out.println(courseTeacher);
  }
}
```
This will output the following “course=teacher” assignments:
```java
{History=Ben, Mathematics=Jeanette, Physics=Lily}
```
## ***Removing Items***

Items can be removed from a TreeMap using the ***`.remove()`*** method. It accepts one parameter, the key, and removes the corresponding key-value pair from the HashMap.
```java
import java.util.TreeMap;

public class Main {
  public static void main(String[] args) {
    TreeMap<String, String> courseTeacher = new TreeMap<String, String>();

    courseTeacher.put("History", "Ben");
    courseTeacher.put("Mathematics", "Jeanette");
    courseTeacher.put("Physics", "Lily");

    courseTeacher.remove("Physics");

    System.out.println(courseTeacher);
  }
}
```
This will output the following:
```java
{History=Ben, Mathematics=Jeanette}
```
## ***Removing All Items***

The ***`.clear()`*** method can be used to remove all the items from the TreeMap.
```java
java

import java.util.TreeMap;

public class Main {
  public static void main(String[] args) {
    TreeMap<String, String> courseTeacher = new TreeMap<String, String>();

    courseTeacher.put("History", "Ben");
    courseTeacher.put("Mathematics", "Jeanette");
    courseTeacher.put("Physics", "Lily");

    courseTeacher.clear();

    System.out.println(courseTeacher);
  }
}
```
The emptied TreeMap will be displayed in the output below:
```java
{}
```
## ***Traversing a TreeMap***

A TreeMap can be traversed with the for-each loop. The ***`.keySet()`*** method can be used to obtain only the keys while the ***`.values()`*** method can be used to obtain only values.
```java
import java.util.TreeMap;

public class Main {
  public static void main(String[] args) {
    TreeMap<String, String> courseTeacher = new TreeMap<String, String>();

    courseTeacher.put("History", "Ben");
    courseTeacher.put("Mathematics", "Jeanette");
    courseTeacher.put("Physics", "Lily");

    System.out.println("Courses offered at our Institute:");

    for (String i : courseTeacher.keySet()) {
      System.out.println(i);
    }

    System.out.println("\nTeachers teaching at our Institute:");

    for (String i : courseTeacher.values()) {
      System.out.println(i);
    }
  }
}
```
The following output will look like this:
```java
Courses offered at our Institute:
Mathematics
History
Physics

Teachers teaching at our Institute:
Jeanette
Ben
Lily
```
