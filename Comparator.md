#  ***Comparator***

*The ***`Comparator`*** interface is used to order objects of an arbitrary class. It is distinct from the ***`Comparable`*** interface, which is implemented by the class itself to define its natural ordering. The ***`Comparator`*** interface is typically implemented in a separate class.*

### ***Syntax***

```java
class MyComparator implements Comparator<MyClass> {
  @Override 
  public int compare(MyClass a, MyClass b) {
    // Compare logic
    ...
    return result;
  }
}
```
### ***Return Value Meaning***

| ***Return Value*** | ***Meaning***                                 |
|--------------|-----------------------------------------|
| >= 1         | first object instance > second object instance |
| 0            | first object instance = second object instance |
| <= -1        | first object instance < second object instance |

### ***Usage Example***
*Suppose we have an Employee class*:

```java
// Employee.java
public class Employee {
  String firstName;
  String lastName;

  // Constructor sets firstName and lastName
  public Employee(String first, String last) {
    this.firstName = first;
    this.lastName = last;
  }

  // User-friendly output when printed.
  public String toString() {
    return "( " + lastName + ", " + firstName + " )";
  }
}
```
*We can define an EmployeeSort class implementing the Comparator interface*:
```java
// EmployeeSort.java
import java.util.*;

public class EmployeeSort implements Comparator<Employee> {

  // Implement the Comparator interface
  @Override 
  public int compare(Employee valueA, Employee valueB) {
    if (valueA.lastName.compareTo(valueB.lastName) != 0) {
      // If lastNames are different, compare lastName
      return valueA.lastName.compareTo(valueB.lastName);
    } else {
      // If lastNames are the same, compare firstName
      return valueA.firstName.compareTo(valueB.firstName);
    }
  }
}
```

*Finally, we can use the Comparator interface in sorting*:
```java
// SortExample.java
import java.util.*;

public class SortExample {
  public static void main(String[] args) {
    // Set up array with a few Employee classes
    Employee a[] = new Employee[5];
    a[0] = new Employee("Kirk","Douglas");
    a[1] = new Employee("Mel","Brooks");
    a[2] = new Employee("Jane","Fonda");
    a[3] = new Employee("Henry","Fonda");
    a[4] = new Employee("Michael","Douglas");

    // Use .sort() method with Comparator class.
    Arrays.sort(a, new EmployeeSort());

    // Print out the sorted Employees
    for (int i=0; i < a.length; i++) {
      System.out.println(a[i]);
    }
  }
}
```
*This example results in the following output*:
```java
( Brooks, Mel )
( Douglas, Kirk )
( Douglas, Michael )
( Fonda, Henry )
( Fonda, Jane )
```
*This demonstrates how to use the Comparator interface to define custom sorting orders for classes in Java*.
