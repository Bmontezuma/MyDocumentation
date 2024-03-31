# ***Random***

The ***`Random`*** class is present in the ***`java.util`*** package. It is used to generate random values or streams of random values of specific data types.

## Usage

The ***`Random`*** class can be accessed by importing it as follows:

```java
import java.util.Random;
```
When an instance of the ***`Random`*** class is created, either a seed value is passed to the constructor or no values are passed at all.

The seed is a value that gets manipulated (using a linear congruential formula) to produce a stream of pseudorandom values. The ***`Random`*** class uses a 48-bit seed.
```java
Random rand1 = new Random();

long seed = (long)3.142;
Random rand2 = new Random(seed);
```

The value of the seed can be set or modified at any point during the execution of the program using the ***`.setSeed()`*** method.
```java
long newseed = (long)2.7182;
rand2.setSeed(newseed);
```

***Note***: If two objects of type ***`Random`*** are created with the same seed, they will generate the same sequence of numbers, provided they are subject to the same sequence of method calls.

## ***Generating Individual Values***
The following methods can be used to generate the next pseudorandom number from the generator’s sequence:

- ***`.nextDouble()`*** and ***`.nextFloat()`***: Return values in the range [0,1).
- ***`.nextInt()`*** and ***`.nextLong()`***: Have no limits.
- ***`.nextBoolean()`***: Returns a random boolean value.
```java
float f = rand1.nextFloat();
double d = rand1.nextDouble();
int i = rand1.nextInt();
long l = rand1.nextLong();
boolean b = rand1.nextBoolean();

System.out.println("Random float: " + f);
System.out.println("Random double: " + d);
System.out.println("Random integer: " + i);
System.out.println("Random long: " + l);
System.out.println("Random boolean: " + b);
```
The output will vary each time these methods are called.

The ***`.nextInt(int bound)`*** method can also be used to generate a random integer between 0 (inclusive) and the specified bound (exclusive).
```java
i = rand1.nextInt(25);
```
A byte array can be filled with random elements using the .***`nextBytes(byte[] bytes)`*** method.
```java
byte[] b = new byte [5];
rand1.nextBytes(b);
```
## ***Generating Streams***
***`IntStream`***, ***`DoubleStream`***, and ***`LongStream`*** objects can be produced using the ***`.ints()`***, ***`.doubles()`***, and ***`.longs()`*** methods, respectively.
```java
import java.util.stream.DoubleStream;
```
An unlimited stream of pseudorandom double values can be generated using the following code snippet:
```java
DoubleStream stream;
stream = rand1.doubles();
```
An effectively unlimited stream of pseudorandom double values, each in a specified range, can be generated using the following code snippet:
```java
stream = rand1.doubles(0,10);
```
A stream of specified size of values in range [0,1) can be generated using the following code snippet:
```java
stream = rand1.doubles(5);
```


