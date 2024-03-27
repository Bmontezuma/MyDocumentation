# ***ArrayList***

*The ArrayList class uses dynamic arrays that are resizable, unlike traditional fixed arrays.* However, each element must still be of the same type. *Elements can be added or removed at any time, making the ArrayList more flexible.*

*Some other important points about the ArrayList class include:*

- *It has the ability to contain duplicate elements.*
- *It maintains insertion order.*
- *It is non-synchronized and, therefore, not safe for multiple threading.*
- *It allows random access since arrays work on an index basis.*
- *The space/time complexity is a bit slower than a LinkedList due to the nature of adding/removing elements.*

## ***Syntax***

*This class is imported with the java.util package.*

```
import java.util.ArrayList;
```
*The syntax for defining an instance of ArrayList is similar to defining a traditional array. A key difference is that angle brackets <> are used instead of square brackets:*
```
ArrayList<DataType> arrayListInstance = new ArrayList<DataType>();
```
### ***Example***

*In the example below, a new ArrayList instance arr is defined. There are print statements throughout to show elements being added to and removed from arr before it is ultimately cleared:*
```
// Import from the java.util package
import java.util.ArrayList;

public class Example {
  public static void main(String []args) {
    ArrayList<String> arr = new ArrayList<>();

    System.out.println(arr);  // Currently empty

    arr.add("hello");
    arr.add("India");

    System.out.println(arr);

    arr.remove("hello");

    System.out.println(arr.size());  // Prints size of ArrayList

    arr.clear();

    System.out.println(arr); // Empty again
  }
}
```
*The output would be:*
```
[]
[hello, India]
1
[]
```
# ***ArrayList Methods***

- ***`add()`***: *Adds an element to an ArrayList.*

- ***`addAll()`***: *Adds a collection to an ArrayList.*
- ***`contains()`***: *Checks if an element is present in the ArrayList or not.*
- ***`get()`***: *Retrieves the element present in a specified position in an ArrayList*.

- ***`indexOf()`***: *Returns the index of the first occurrence of a given element, or -1 if not found.*
- ***`isEmpty()`***: *Checks if an ArrayList is empty.*
- ***`remove()`***: *Removes a specified element from an ArrayList.*
- ***`removeIf()`***: *Removes all the elements of an ArrayList that satisfy a given predicate.*
- ***`retainAll()`***: *Retains only the elements that are contained in the specified collection*.
- ***`set()`***: *Replaces the element present in a specified position in an ArrayList*.
- ***`size()`***: *Returns the number of elements in the ArrayList.*
- ***`sort()`***: *Used to sort arrays of primitive types and objects*.
- ***`spliterator()`***: *Returns a Spliterator over the elements in ArrayList*.
- ***`subList()`***: *Returns a view of a portion of the list based on the specified start and end indices*.
- ***`toArray()`***: *Converts an ArrayList into an array*.
- ***`trimToSize()`***: *Adjusts the capacity of the ArrayList to be the same as its size*.


