---
layout: default
title: Java
nav_order: 1
parent: Prerequisites
---

# Introduction to Java Programming language

> "Java is a very general-purpose language. It’s designed to span many different domains. You can write server-side programs; you can write apps for mobile phones; you can write scientific programs; you can write software that travels between planets."
>
> <cite>James Gosling, Founder and lead designer of the Java programming language</cite>


In 1991, a project called "Green" was started in Sun Microsystems. The goal of this project was to create a programming language that can run on all hardware. This goal was a very big goal. This project was called "Java" at the end of the work. When Java was being developed, C and C++ dominated other programming languages. However, their major weaknesses plague many programmers. For example, if you wanted to write a program in C language and run it on computers made by different companies, you would have to compile its source code in each of the machines and run the executable code in the desired machine. So far, the problem was not very difficult, but the point was that you had to change the source code every time to compile the program. In addition, you had to always maintain several different versions of the source code, which greatly increased the cost of software production.

In 1995, the first version of Java language was introduced to the world along with a shocking technology called Applet. The new language claimed to work on all existing operating systems. You don't need to create and maintain different source codes for your application. The motto of the new language was "Write Once, Run Anywhere". A new language had come to shape the future of the web. The new language gave everyone hope. It did not have the major drawbacks of previous languages such as C and C++, and therefore it was welcomed by programmers all over the world.

This language followed its natural course and changes were made according to the opinions of the programmers. However, Java strongly believed in adhering to its motto and was able to defend its claim with authority. In 1999, Sun divided the Java language into three main branches:

* Java 2 Standard Version or J2SE: This branch contains all the standard features of the Java language.
* Java 2 Enterprise Edition or J2EE: This branch is for server-side programming.
* Java 2 micro version or J2ME: This branch is for programming consumer electronic devices such as mobile phones.

The natural growth of Java continued and every now and then new versions and modifications of Java were introduced to the programming community. 

In 2005 Sun decided to change its naming convention. The name of the Java language along with its version number would be something like j2sdk_1.4.06. After this year and due to the many changes made in the Java language, this language chose the name Java 5.

The three main branches of the Java language were also renamed while maintaining the previous goals and features. The new names for each are as follows: Java SE or Java Standard Edition, Java EE or Java Enterprise Edition and Java ME or Java Micro Edition.

TODO: Java Open Source

TODO: Oracle Acquisition of Sun Microsystems
In 2009 Oracle acquired Sun Microsystems ...

Since that year Oracle has presented a new version of Java language every year. Currently, the latest long term supported (LTS) version of Java is Java 17. 

# Java, JDK, JRE and JVM

# Install Java

## About Java Versions

# First Java Application
It is time for a cup of "Java"! We already have installed Java. We don't want to use any IDE for our first Java program! So, Open your preferred text editor (For example Notepad in windows) and write this code (please, do not copy for this time!):

```java
public class FisrtCupApp {
    public static void main(String[] args) {
        System.out.println("My first cup of Java!");
    }
}
```

Save the file with `FisrtCupApp.java`. 

Warning: The file name must be as the same as clss name. It is case-sensitive and, for example `FisrtCupApp.java` is different with `FisrtcupApp.java` and the second one won't compile.

Now, it is time to compile our Java program. Open your terminal (in windows, open `Command Prompt`), change directory to the `FisrtCupApp.java` directory and then run this command:

```
javac FisrtCupApp.java
```

After successfull compile, you will see a new generated file: `FisrtCupApp.class`. This is compiled version of our app that we can run it on every machine with Java Runtime Environment (JRE) installed.

To run the program, run this command in the terminal:

```
java FisrtCupApp
```

If everything goes well, you can see a message in your terminal:

```
My first cup of Java!
```

This program includes one `class`. Classes are the main building block of Object Oriented Programming (OOP). 

In this class, there is a method called main(). This method is the starting point of all Java programs. The Java Virtual Machine (JVM) executes this method to start a Java program, and as soon as this method is finished, the execution of the program ends. 

Inside this method there is a statement. Running this line will show `My first cup of Java!` in the output window.

# Java Class Structure

# Java Data Types

In any program we deal with a number of values. The program may work with numbers, or with characters. For example, suppose we want to take two different numbers from the input in a program, perform mathematical operations on them, and print the result in the output. We call this program `SimpleCalculator`:

```java
/**
 * A very simple calculator.
 */
public class SimpleCalculator {
    public static void main(String[] args) {
    }
}
```

Now we need to change the program so that it can store two numbers with different names and values:

```java
/**
 * A very simple calculator.
 */
public class SimpleCalculator {
    public static void main(String[] args) {
        int first;
        int second;        
    }
}
```
Now our `main()` method has two variables called `first` and `second`. In programming terms, `first` and `second` are called `variables`. 

As you have seen so far, each variable contains a name and a type. In the `SimpleCalculator` example, we have two variables named `first` and `second`, both of which are `int` type. 

Each variable has a value in addition to name and type. Now we want to modify the `SimpleCalculator` class so that we can initialize our variables:


```java
/**
 * A very simple calculator.
 */
import java.util.Scanner;
 
public class SimpleCalculator {
 
    public static void main(String[] args) {
        int first;
        int second;
 
        Scanner input = new Scanner( System.in );
 
        System.out.print("Enter first integer: ");
        first = input.nextInt();
 
        System.out.print("Enter second integer: ");
        second = input.nextInt();
    }
}
```

For now, we have nothing to do with the `Scanner` class. Just know that we use the methods of this class to read the inputs of the program. 

After running the above program, the phrase `Enter first integer:` is displayed in the output console and you can enter the desired value in front of it. Then the next line will be displayed with the phrase `Enter second integer:` where you can enter the value you want for the second variable. 

Now we perform some mathematical operations on these two numbers and print the result in the output:


```java
/**
 * A very simple calculator.
 */
import java.util.Scanner;
 
public class SimpleCalculator {
 
    public static void main(String[] args) {
        int first;
        int second;
 
        Scanner input = new Scanner( System.in );
 
        System.out.print("Enter first integer: ");
        first = input.nextInt();
 
        System.out.print("Enter second integer: ");
        second = input.nextInt();
 
        System.out.println("first + second = " + ( first + second ) );
        System.out.println("first - second = " + ( first - second ) );
        System.out.println("first * second = " + ( first * second ) );
        System.out.println("first / second = " + ( first / second ) );
    }
}
```

The purpose of any computer program is to process data. For this, any program must be able to input data, process it, and display the result appropriately. 

To process data in the program, we need to be able to identify the data. We need to know what kind they are. We also need to know how much each of them has at any given moment. 

As you saw in the previous program, we assign three attributes to each variable: type, name and value. The general pattern of variable definition (also called declaration) in Java language is as follows:

```java
Type name;
```

After defining a variable, we must be able to assign a value to it. For this, we use the following pattern:

```java
name = Value;
```

If we want, we can do two steps of defining the variable and assigning a value to it in one command:

```java
Type name = Value;
```

Now some examples of declaring variables and assigning values to them:

```java
int a = 5;                   // An integer variable with value 5
char someChar = 'A';         // A character variable with value 'A'
double PI = 3.14;            // A floating point number with value 3.14 
String hello = "Hello Java"; // A String with value "Hello Java"
```

## Java Primitives
After getting acquainted with variables and how to define and value them, we can see the complete list of Java primitive data types:

| Syntax      | Range of allowed values                          | Description  |
| ----------- | -----------------------                          | ------------ |
| boolean     | `true` and `false`                               | Suitable for logical variables that always have one of two values, true or false |
| char        | From Unicode's zero to 2<sup>16</sup>-1 unicode  | Suitable for all types of literal variables. Considering that letter variables in Java Unicode are 16-bit, they can be used for all letters of all languages.|
| byte        | From -128 to 127                                 | Suitable for integer variables that are within the limit of allowed integer values. |
| short       | From -2<sup>-15</sup> to 2<sup>15</sup>-1        | Suitable for integer variables that are within the limit of allowed integer values (around -32,000 to +32,000).|
| int         | From -2<sup>-31</sup> to 2<sup>31</sup>-1        | Suitable for integer variables that are within the limit of allowed integer values (around -2,000,000,000 to +2,000,000,000).|
| long        | From -2<sup>-63</sup> to 2<sup>63</sup>-1        | Suitable for very, very large integer variables! |
| float       | IEEE754 (approx 3.4E38- to 3.4E38 with 8 digits of decimal precision)         | Suitable for floating point numbers with good precision for routine calculations |
| double      | IEEE754 (Approximately from 1.8E308-up to 1.8E308 with 16 digits decimal precision)   | Suitable for very high precision floating point numbers for double precision calculations |
| void        | No-Value        | For variables that have no type (we'll talk more about the `void` type later) |

## Java Wrapper classes for Primitive Types

## Literal Varialbles

In some Java programs you may want to use values directly. Consider the following statement:

```java
int a = 5;
```
In the above example, the number 5 is a literal variable. The Java compiler has some rules for literals. For example, it recognizes correct literal variables like the above example by default of `int` type. Now, if you want to assign the number 5 to a long variable in an assignment command using the = operator, you must do the following:

```java
long a = 5L;
```
The letter `L` immediately after the number 5 tells the Java compiler that the literal variable 5 is of `long` type. Also, the default for floating point literals in Java is of `double` type. Consider the following line of code:

```java
float a = 3.14;
```
Do you think this line code will compile? Try it! As you may have guessed and probably tested your guess, the Java compiler throws an error when executing the above code:

```
possible loss of precision
found:    double
required: float
float a = 3.14;
          ^
1 error
```
Did you get the cause of the error? The literal variable 3.14 is assumed by the Java compiler to be `double` by default. When it wants to put its value in a floating point variable of type `float`, the precision of the `double` must be reduced to `float`, and this is an error from the Java compiler's point of view. 

To solve this problem, you must explicitly tell the Java compiler that 3.14 is a `float` literal. For this, we do the same as the following command:

```java
float a = 3.14F;
```
The letter `F` immediately after 3.14 forces the Java compiler to consider the literal variable 3.14 to be of `float` type.

## Strings

Our variables are not always numeric types. In many cases, we need to input letters and words into our program, process them and display the result as a word or sentence. 

For example, suppose we have a program that takes the name of a student from the input and displays his/her grade. We need a variable in which we can store the name of the student. 

These types of variables are called `String`s. The Java language has extensive facilities for working with strings, which we will disscuss more in next chapters.

To define a string variable, proceed as follows:

```java
String name;
```

Of course, like other types of variables in Java language, it is possible to initialize it at the same time as defining a string variable in Java:

```java
String name = "Some text";
```
`String`s  are always placed between double qoutes.

## Java String handling

### String Length

### Concatenating Strings

### Format Strings

### Substrings

### Compare Strings

## Java StringBuilder



## Text Blocks

From Java 15, we have text blocks in Java! You can define a text block by wrapping your text inside `"""` (three double qoutes) as below:

```java
String html = """
    <html>
        <body>
            <span>example text</span>
        </body>
    </html>""";
```

## Constant Variables

Constant Variables are variables whose value cannot be changed! This definition is self-contradictory enough. A variable means something that changes, so a variable whose value cannot be changed is meaningless. 

But if we stop playing with words, we can see that many times in programs we may define variables that we don't want their value to change during the execution of the program, intentionally or unintentionally. 

For example, suppose we use the number pi (π) in mathematical calculations. The value of this variable should not change during program execution. For this we define this variable as `final`:

```java
final double PI = 3.14;
```

## Java Arrays

Suppose you want to take the grades of students in a class and calculate their average. The number of students in the class is 25. Are you defining 25 float variables? What would you do if there were 50 students in the class? What would you do for 200 people? 

As you might guess, the solution is not to use too many variables. If we could store a large number of variables of the same type with the same name and access them using an index, the problem would be solved. 

For example, we used to say that the list of students' grades includes 25 float variables, and then we said that the first student's grade is 15 and the second student's grade is 16, and so on. 

Such a data type is called an array. Array is a set of variables called element and all of them are of the same type. 

An array is identified by several things: its name, the number of variables it holds, called the length of the array, and the type of variables the array holds. 

Therefore, to define an array that stores students' grades, we act as follows:

```java
float[25] grades;
```
Pay attention to the parts of the above definition: 
`float` Specifies the array type. It actually says that the above array holds float elements. 

`[25]` declares that the length of the array is 25. [] represents the array and the integer inside it specifies the length of the array. 

`grades` is the name of the array. 

Now, if we want to value the elements of this array, we act as follows:

```java
grades[0] = 12.3f;
grades[1] = 15.5f;
// ...
grades[24] = 16f;
```
In Java, array index starts from 0. So in an array with 25 elements, the first item's index in 0 and latest item's index is 24.

## Naming rules for Variables

Naming variables in Java has limitations. Variables start with letters (a-z and A-Z) and an underscore (`_`) and can be followed by any number of letters or numbers.

Some examples of incorrect names for variables in Java:

```java
int 1i; // Wrong name
String #name = "My Name"; // Wrong name
```
However, there are rules for naming variables in the Java language that are not mandatory, but most Java programmers have accepted them, and of course it is recommended as a correct coding pattern in Java. Some of these rules are:

Variable names start with a lowercase letter. If the variable name is more than one word, the words are concatenated and the first letter of the second and subsequent words are capitalized. This naming method is known as Camel case. Some examples of good and bad names:


```java
int number;          // Good name!
int second_number;   // Bad name!
int secondNumber;    // Good name!
String Name;         // Bad name!
String name;         // Good name!
float _average;      // Bad name!
```

Constant variables (final) are usually written in capital letters and if the number of words is more than one word, they are separated by a underscore (-):

```java
double PI = 3.14;
String URL = "https://behzadian.info";
String DB_URL = "jdbc:mysql://127.0.0.1:3306/testDB";
```

## Variables Scopes

Variables are valid only in the same scope in which they are defined. For example, if we define a variable inside a method, we don't have access to it in other methods and we can't see its value or change it. See the example:

```java
public class VariableScopeTest {
 
    public void firstMethod() {
        int myNumber = 5;
    }       
 
    public void someMethod () {
        myNumber = 10; //?
    }
}
```
In this example, a variable named `myNumber` is defined and initialized in the `firstMethod` method. Although both `firstMethod` and `someMethod` belong to the same class, in `someMethod` we have no access to `myNumber` variable. If you try to compile the above class, the compiler will give you an error:

```
can not find symbol
symbol  : variable: myNumber
location: class VariableScopeTest
                myNumber = 10; // ?
                ^
1 error
```

The reason is quite clear: a variable defined in a method belongs to that method and does not exist outside of it. Therefore, we do not have access to it in other methods.

The variables' scope in Java language is divided as follows:

**Class scope**: Class properties are variables that are accessible throughout a class. For example, if a variable is in the scope of a class, all the methods of that class have access to it, and any of the methods that change that variable will change its value in other methods as well.

**Method scope**: These are variables that are defined in a method. These variables can only be accessed in the method in which they are defined.

**Block scope**: Sometimes we define variables inside iteration loops or some other conditional structures inside a method. These variables are not accessible outside that block. See the example:


```java
public class VariableScopeTest {
 
    public void someMethod () {
        for( int i = 0 ; i < 10 ; i++ ) {
            // Do something
        }       
 
        // Now what is i's value?
        System.out.println( "i = " + i );
    }
}
```

In the example above, the variable `i` is defined in the for loop. When we try to print the value of `i` to the output, we get an error:

```
can not find symbol
symbol  : variable: i
location: class VariableScopeTest
                System.out.println( "i = " + i );
                                             ^
1 error

```
The reason is that the scope of the variable `i` is only the for loop, and there is no variable `i` outside of it.

An important issue that needs to be explained in the field of variables is the issue of names of variables. Is it possible to have two variables with the same name? it depends! 

This is possible if the variables of the same name are in different scopes. For example, if a class has an attribute named someInt and one of the methods of that class has a variable with the same name, there is no error. 

The only important thing is that the variables of the same name are valid in the same scope in which they are defined. See the example:


```java
public class VariableScopeTest {
 
    int someInt;
 
    public void someMethod () {
        int someInt;
        someInt = 5; // ?
    }
}
```
In the above example, a variable named `someInt` is defined in the `VariableScopeTest` class and is among the properties of that class. A variable called `someInt` is also defined in the `someMethod` method. 

Now, what happens if we assign the value `5` to the `someInt` variable in the `someMethode` method? Does the variable defined in the function change or the property of that class? 

To answer this question, it should be noted that priority is given to the domain in which the variable is defined. So if we assign the value `5` to someInt, the variable defined in the method will change, not the class property of the same name. 

Now, what should we do if we want to change the class property called `someInt` in the `someMethod` method? For this, it is enough to use `this` keyword. See the example:

```java
public class VariableScopeTest {
 
    int someInt;
 
    public void someMethod () {
        int someInt;
        someInt = 5; // Method variable
        this.someInt = 7; // class variable
    }
}
```

# Java Operators

# Java Control Structures

## Selection in Java

## If Statement

## If-Else Statement

## Switch Statement

## Iteration in Java

# Object-Orientation in Java

## Java Classes

## Inheritance

## Abstract Classes

## Java Interfaces

## Java Enums

# Java Generics

# Exception Handling in Java

# Java Collections

## List

## Stack

## Queue

## Priority Queue

## Set

## Map

## Java Stream API

# Threads in Java

# Java Regular Expressions

# Functional Programming in Java

# Java Date and Time

# JDBC and database in Java
 
# File and IO in Java

