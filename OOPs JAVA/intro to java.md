## structure
---
```java
public class Main {
  public static void main(String[] args) {
    System.out.println("Hello World");
  }
}
```


##### printing plain txt
```java
System.out.println("Hello World!");
System.out.println("I am learning Java.");
System.out.println("It is awesome!");
```

##### printing numbers
```java
System.out.println(3 + 3);
```
as we can see its same a the txt one we dont need to put something type dictators like in C

#### variables 
---
```java
int myNum = 5;               // Integer (whole number)
float myFloatNum = 5.99f;    // Floating point number
char myLetter = 'D';         // Character
boolean myBool = true;       // Boolean
String myText = "Hello";     // String
```
it is mostly like C so we dont need to learn something extra

#### type casting
---


#### STRINGS
---
declaration of a string
```java
String greeting = "Hello";
```

###### concatenation

method 1
```java
String firstName = "John";
String lastName = "Doe";
System.out.println(firstName + " " + lastName);
```

method 2
```java
String firstName = "John ";
String lastName = "Doe";
System.out.println(firstName.concat(lastName));
```

### *note*
`java uses + for both concatenation and addition... if it is an INT then it will be a simple addition but if it is string it will concat`

```java
int x = 10;
int y = 20;
int z = x + y;  // z will be 30 (an integer/number)
```
addition

```java
String x = "10";
String y = "20";
String z = x + y;  // z will be 1020 (a String)
```
concat



## if else statement
---
```java
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}
```
its mostly same as c so we dont need to learn something completely different

## switch statements
---
```java
int day = 4;
switch (day) {
  case 6:
    System.out.println("Today is Saturday");
    break;
  case 7:
    System.out.println("Today is Sunday");
    break;
  default:
    System.out.println("Looking forward to the Weekend");
}
```
again its the same as c so yea 

## while loop
---
```java
int i = 0;
while (i < 5) {
  System.out.println(i);
  i++;
}
```

mostly the same as c but the print statement is different

- do while part

```java
int i = 0;do {
  System.out.println(i);
  i++;
}
while (i < 5);
```


## for loop 
---
```java
for (int i = 0; i < 5; i++) {
  System.out.println(i);
}
```


- ***nesting***

```java
// Outer loop
for (int i = 1; i <= 2; i++) {
  System.out.println("Outer: " + i); // Executes 2 times
  
  // Inner loop
  for (int j = 1; j <= 3; j++) {
    System.out.println(" Inner: " + j); // Executes 6 times (2 * 3)
  }
} 
```


## for each loop
---
There is also a "**for-each**" loop, which is used exclusively to loop through elements in an [**array**](https://www.w3schools.com/java/java_arrays.asp)

```java
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (String i : cars) {
  System.out.println(i);
}
```

it can iterate through all the elements of an array till the last element so we dont need a count function to be called like in C to check the upper limit of a list


# method
---
`A **method** is a block of code which only runs when it is called.

`You can pass data, known as parameters, into a method.

`Methods are used to perform certain actions, and they are also known as **functions**.

`Why use methods? To reuse code: define the code once, and use it many times.


basically the main function in C

```java
public class Main {
  static void myMethod() {
    System.out.println("I just got executed!");
  }

  public static void main(String[] args) {
    myMethod();
  }
}

// Outputs "I just got executed!"
```
