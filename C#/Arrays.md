# ***Arrays***

An ***array*** is a data structure used in C# to ***store a sequential collection of elements***. Its size is ***immutable*** (***cannot be changed after creation***). The elements of an array are all of the same type. 

## ***Syntax***

There are several ways to create an ***array*** in C#:

```csharp
// Create a variable of type "type[]" without initializing it:
type[] arrayName;

// Create the array variable and initialize it with an array of N items:
type[] arrayName = new type[N];

// Create the array variable and initialize it by specifying the contents:
type[] arrayName = new type[] { value1, value2, value3, ... valueN };

// Alternative way of creating the array and specifying the contents:
type[] arrayName = { value1, value2, value3, ... valueN };
```

***Note***: ***Arrays*** in C# have a ***fixed size***, meaning the number of elements they hold cannot be changed once the array has been created.

## ***Example***
Each element in an ***array*** is assigned a specific index starting at zero. To access or modify an element in the array, you refer to it by its index and operate on it accordingly.
```csharp
using System;

public class Example
{
  public static void Main(string[] args)
  {
    char[] vowels = {'a', 'e', 'i', 'o', 'u'};
    //      indexes:  0    1    2    3    4

    Console.WriteLine(vowels[0]); // Output: a

    vowels[0] = 'r';

    Console.WriteLine(vowels[0]); // Output: r
  }
}
```
In the example above, an ***array*** of chars was initialized with all the vowels. The first element in the array at index 0 was printed. Then, the element at index 0 was modified by assigning it a new value of 'r'. Then, the value at index 0 was printed again.

These examples demonstrate how ***arrays**** can be used to store various types of data commonly encountered in ***AR/VR development***, such as ***coordinates***, ***colors***, and ***GameObjects***.

# ***Example 1: Storing Coordinates***
```csharp
Vector3[] points = new Vector3[4];
points[0] = new Vector3(0, 0, 0);
points[1] = new Vector3(1, 0, 0);
points[2] = new Vector3(1, 1, 0);
points[3] = new Vector3(0, 1, 0);
```
# ***Example 2: Storing Colors***
```csharp
Color[] colors = { Color.red, Color.green, Color.blue };
```
# ***Example 3: Storing GameObjects***
```csharp
GameObject[] gameObjects = new GameObject[3];
gameObjects[0] = Instantiate(prefab1, position, rotation);
gameObjects[1] = Instantiate(prefab2, position, rotation);
gameObjects[2] = Instantiate(prefab3, position, rotation);
```
## ***Array Methods***

Arrays in C# are objects, not just contiguous blocks of memory as in C and C++. Array is the base type of all arrays, and any array can use the properties and methods of the Array object, a few of which are listed below:

***.Clear()***\
*Clears the contents of an array, returning each element to its default value*.
```csharp
int[] numbers = { 1, 2, 3, 4, 5 };
Array.Clear(numbers, 0, numbers.Length);
// Now 'numbers' array will contain all zeros: [0, 0, 0, 0, 0]
```

***.Copy()***\
*Copies elements in an array within a certain range*.
```csharp
int[] source = { 1, 2, 3, 4, 5 };
int[] destination = new int[3];
Array.Copy(source, 1, destination, 0, 3);
// Now 'destination' array will contain elements [2, 3, 4]
```
***.CopyTo()***\
*Copies the elements of an array to another array*.
```csharp
int[] source = { 1, 2, 3, 4, 5 };
int[] destination = new int[3];
Array.Copy(source, 1, destination, 0, 3);
// Now 'destination' array will contain elements [2, 3, 4]
```
***.Length***\
*Returns the total number of elements in the array*.
```csharp
int[] numbers = { 1, 2, 3, 4, 5 };
int length = numbers.Length;
// 'length' will be 5
```
***.Resize()***\
*Updates the size of an existing array*.
```csharp
int[] numbers = { 1, 2, 3 };
Array.Resize(ref numbers, 5);
// 'numbers' array will be resized to have length 5 and filled with default values
```

***.Reverse()***\
*Reverses the sequence of a subset of the elements in a one-dimensional array*.
```csharp
int[] numbers = { 1, 2, 3, 4, 5 };
Array.Reverse(numbers, 1, 3);
// 'numbers' array will be [1, 4, 3, 2, 5]
```
***.Sort()***\
*Arranges the elements of an array in ascending or alphabetical order*.
```csharp
int[] numbers = { 5, 3, 1, 4, 2 };
Array.Sort(numbers);
// 'numbers' array will be sorted in ascending order: [1, 2, 3, 4, 5]
```
