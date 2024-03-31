# ***Regular Expressions***

Regular expressions are a language used for pattern-matching text content, and they are implemented in Java through the ***`Pattern`*** and ***`Matcher`*** classes. Both classes are part of ***`java.util.regex`***.

## ***Using the Pattern Class***

An instance of the ***`Pattern`*** class is used to hold a compiled version of a regular expression pattern.

## ***Syntax***

```java
Pattern p = Pattern.compile(re, flags);
```

Where re is a regular expression pattern, and flags is an optional int bit mask specifying the flags for the pattern.

## ***Flags***
- ***`Pattern.CASE_INSENSITIVE`***
- ***`Pattern.MULTILINE`***
- ***`Pattern.DOTALL`***
- ***`Pattern.UNICODE_CASE`***
- ***`Pattern.CANON_EQ`***
- ***`Pattern.UNIX_LINES`***
- ***`Pattern.LITERAL`***
- ***`Pattern.UNICODE_CHARACTER_CLASS`***
- ***`Pattern.COMMENTS`***

## ***Methods***

***`.compile(pattern, flags)`***: Returns a Pattern instance based on the given pattern and optional flags.

***`.pattern()`***: Returns the string pattern with which the instance was compiled.

***`.flags()`***: Returns the flags bit mask with which the instance was compiled.

***`.matcher(input)`***: Returns a Matcher instance that applies the Pattern instance against the supplied input text.

***`.matches(pattern, input)`***: Returns a boolean if the given pattern matches a string in the supplied input text.

***`.split(input, limit)`***: Returns an array that splits the input around the matches found by the compiled pattern.

## ***Using the Matcher Class***
An instance of the Matcher class is used to perform operations against input text using a compiled Pattern instance.
```java
Matcher m = pattern.matcher(input)
```
## ***Syntax***
***`.end(group)`*** : Returns the offset after the last character matched. If optional int group included, returns the index of the match made by the given subgroup during the last match operation. (Subgroups defined by enclosing parentheses (...))

***`.find(start)`*** : Attempts to find the next match in the input. If optional int start included, resets the Matcher instance and finds the next match after the specified index in the input.

***`.group(group)`*** : Returns the section of input last matched in the input. If optional int group specified, find the numbered subgroup matched in the input. (Subgroups defined by enclosing parentheses (...))

***`.hitEnd()`*** : Returns true if the last match hit the end of input.

***`.lookingAt()`*** : Attempts to find a match beginning at start of region. True if one found.

***`.matches()`*** : Attempts to find a match in the entire region. True if found.

***`.pattern()`*** : Returns the Pattern instance used by this Matcher instance.

***`.region(start, end)`*** : Sets the region of input used by this Matcher instance.

***`.regionEnd()`*** : Returns the end of region for this Matcher instance.

***`.regionStart()`*** : Returns the start of region for this Matcher instance.

***`.replaceAll(replacement)`*** : Replaces all incidences of matches with the given replacement string. Returns modified string.

***`.replaceFirst(replacement)`*** : Replaces first match in the input with the given replacement string. Returns modified string.

***`.reset(input)`*** : Resets this Matcher instance. If optional input specified, resets with new input text.

***`.start(group)`*** : Returns the offset of the first character matched. If optional int group included, returns the index of the match made by the given subgroup during the last match operation. (Subgroups defined by enclosing parentheses (...))

***`.usePattern(pattern)`*** : Sets Matcher instance to use new Pattern instance pattern.

## ***Example***
```java
import java.util.regex.*;

public class Example {
    public static void main(String args[]) {
      Pattern p = Pattern.compile("s.?e[a-z]+");
      Matcher m = p.matcher("Susie sells sea shells by the sea shore.");
      boolean matchFound = m.find();
      while ( matchFound ) {
          System.out.println(m.group());
          matchFound = m.find();
      }
    }
}
```
Output:
```java
sells
sea
shells
sea
```
