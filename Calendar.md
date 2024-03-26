# ***Calendar***

*The Calendar class is an abstract class that represents dates and time.* The class has methods for converting between a given moment in time and a number of calendar attributes such as ***`YEAR`***, ***`MONTH`***, ***`DAY_OF_MONTH`***, ***`HOUR`***, and so on*.

## ***Syntax***

```java
Calendar calendar = Calendar.getInstance();
```
***Note***: *The ***`.getInstance()`*** function creates an object that represents the current date and time.*

### ***Example***

*In the example below, a Calendar object is created using the ***`getInstance()`*** method. Then the ***`set()`*** method is used to set the ***year***, ***month***, ***date***, ***hour***, ***minute***, and ***second***. Finally, the getTime() method is used to get the date. Note that the month is zero-based, so January is 0, February is 1, and so on. Also, the set() overload could have been used that takes all the parameters at once*.
```java
import java.util.Date;
import java.util.Calendar;

public class CalendarExample {
    public static void main(String[] args) {

        Calendar calendar = Calendar.getInstance();
        calendar.set(Calendar.YEAR, 2023);
        calendar.set(Calendar.MONTH, 0);
        calendar.set(Calendar.DATE, 8);
        calendar.set(Calendar.HOUR_OF_DAY, 0);
        calendar.set(Calendar.MINUTE, 0);
        calendar.set(Calendar.SECOND, 0);

        // calendar.set(2023, 0, 8, 0, 0, 0);

        Date date = calendar.getTime();

        System.out.println(date);
    }
}
```
*The above code will output*:

## ***Fields***

*There are many fields in the Calendar class. Here are some of the most important ones*:

***`YEAR`***: *The field indicating the year*.\
***`MONTH`***: *The field indicating the month*.\
***`DAY_OF_MONTH`***: *The field indicating the day of the month*.\
***`DATE`***: *Synonym for ***DAY_OF_MONTH****.\
***`HOUR`***: *The field indicating the hour of the day*.\
***`MINUTE`***: *The field indicating the minute within the hour*.\
***`SECOND`***: *The field indicating the second within the minute*.\
***`MILLISECOND`***: *The field indicating the millisecond within the second*.

### ***Methods***

*Methods of the Calendar class include:*

- ***`.add()`***
  *Adds or subtracts a specified amount of time to/from the given Calendar field.*

- ***`.after()`***
  *Compares whether the current instance of Calendar occurs after the time represented by the specified object.*

- ***`.before()`***
  *Returns a boolean based on whether one Calendar instance is before the other given instance.*

- ***`.clear()`***
  *A method designed to reset or clear specific fields of a Calendar instance.*

- ***`.clone()`***
  *Returns a copy of a Calendar object.*

- ***`.compareTo()`***
  *Compares a passed Calendar object with an existing Calendar object.*

- ***`.complete()`***
  *A method to fill in any empty fields of a Calendar instance.*

- ***`.computeFields()`***
  *Synchronizes the time of a Calendar object with the set field values.*

- ***`.equals()`***
  *Used to determine if two Calendar objects are equal.*

- ***`.get()`***
  *Returns the value of the given calendar field.*

- ***`.getActualMaximum()`***
  *Returns the actual maximum value for a specific calendar field, conditional on the time value of the calendar.*

- ***`.getActualMinimum()`***
  *Returns the minimum value allowed for a given calendar field.*

- ***`.getAvailableCalendarTypes()`***
  *A method that is used to get list of all available calendar types in Java.*

- ***`.getAvailableLocales()`***
  *Returns an array of locales, which represent specific geographical or cultural regions.*

- ***`.getCalendarType()`***
  *Retrieves the type or format of the calendar represented by the Calendar object, returns a string representing the calendar type.*

- ***`.getDisplayName()`***
  *Returns the string representation (display name) of the calendar field value in the given style and locale. If no string representation is applicable, null is returned.*

- ***`.getDisplayNames()`***
  *Returns a map containing all string representations of Calendar field values in the given style and locale.*

- ***`.getMinimum()`***
  *Returns the minimum value for the given calendar field.*

- ***`.getTime()`***
  *Returns the time value of the given Calendar object.*

- ***`.getTimeInMillis()`***
  *Returns the time in milliseconds.*

- ***`.getTimeZone()`***
  *Returns the current time-zone of a given Calendar.*

- ***`.getWeeksInWeekYear()`***
  *Returns the total number of weeks in a week year.*

- ***`.getWeekYear()`***
  *Returns the week year.*

- ***`.hashCode()`***
  *Returns the hash code for a Calendar object.*

- ***`.internalGet()`***
  *Returns the value of a given field.*

- ***`.isLenient()`***
  *Returns a boolean identifying a given calendar instance as lenient or not.*

- ***`.isSet()`***
  *Evaluates whether the given calendar field has a value set or not.*

- ***`.isWeekDateSupported()`***
  *Determines if the current Calendar object supports week dates.*

- ***`.roll()`***
  *Adds or subtracts a single unit of time from a given calendar.*

- ***`.setFirstDayOfWeek()`***
  *Sets the first day of the week.*

- ***`.setLenient()`***
  *Sets whether the date/time interpretation should be lenient or not.*

- ***`.setMinimalDaysInFirstWeek()`***
  *Sets how many minimal days required in the first week of the year.*
