# ***Iterator***

An iterator is an object that allows code to step through collections. Java has Iterator and ListIterator objects, both imported through the java.util package. The main difference between the two is that ListIterator allows for the bidirectional traversal of collections. The ListIterator can only be retrieved from collections that implement the List interface.

## ***Syntax***
```java
Iterator value = collection.iterator()

ListIterator listvalue = listcollection.listIterator()
```
Collections have an ***`.iterator()`*** method that returns an Iterator object. List collections also have a ***`.listIterator()`*** method that return a ListIterator object.

## ***Example***
The following example uses an Iterator to traverse an ArrayList:
```java
import java.util.*;

public class Example {
  public static void main(String args[]) {
    // Create a new ArrayList
    ArrayList l = new ArrayList();

    // Add some items to the ArrayList
    l.add(1);
    l.add(2);
    l.add(3);
    l.add(4);
    l.add(5);

    Iterator i = l.iterator();

    // Loop through ArrayList contents
    while(i.hasNext()) {
      Object item = i.next();
      System.out.print(item + ", ");
    }
  }
}
```
This example outputs the following:
```java
1, 2, 3, 4, 5,
```
Iterator and ListIterator objects have the following methods to traverse their collections:

# ***Iterator***
***`.add()`***
Adds an entry to the underlying collection of a ListIterator object.

***`.hasNext()`***
Returns true if an Iterator or a ListIterator object has more elements. Returns false otherwise.

***`.hasPrevious()`***
Returns true if a ListIterator object has prior elements. Returns false otherwise.

***`.next()`***
Returns the next element from an Iterator or a ListIterator object.

***`.nextIndex()`***
Returns the index of next element from a ListIterator object.

***`.previous()`***
Returns the previous element from a ListIterator object.

***`.previousIndex()`***
Returns the index of the previous element from a ListIterator object.

***`.remove()`***
Removes an entry from the underlying collection of an Iterator or ListIterator object.

***`.set()`***
Replaces the current entry in the underlying collection of a ListIterator object.
