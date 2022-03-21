# Intro to Java 

**Java runs on many different platforms, but programmers write it all the same way** -- this is achieved by running an instance of the Java Virtual Machine on any given operating system, which can then handle the same code no matter the system. 
The Java Virtual Machine cannot, however, read human-written code. So after a programmer writes their code as a .java file, that code is *compiled* into a .class file  

(For a comprehensive overview of Java, the [**Official Documentation Tutorials**](https://docs.oracle.com/javase/tutorial/tutorialLearningPaths.html) are a great place to start. The information in these notes has been drawn from a variety of courses, including Oracle's Java Tutorials. 

<br> 

## Hello World

The folllowing file is named ```HelloYou.java``` -- Java files have a ```.java``` extension. Some programs are one file, others are hundreds of files

This file, [```HelloYou.java```](/00_Java_Files/HelloYou.java), is the traditional "**Hello World**" printer:
```java
public class HelloYou {
  public static void main(String[] args) {
    System.out.println("Hello CBL2C");
  }
}
```
Java is a *Verbose* Object-Oriented Language, so something as simple as printing a string takes quite a bit more setup than it would in, say, Ruby, or JavaScript. 

<br>

**Let's examine the components that make up this simple exercise:** 

Inside ```HelloYou.java```, we have a class:

```java
public class HelloYou {
```
The ```HelloYou``` class concept is: printer for the string "```Hello <programmer name>```" 
  
The scope of this outer public class is marked using curly braces: ```{ }``` Syntax inside the curly braces is part of the class's scope

Each file has one primary class named after the file. The class name (```HelloYou```) and the file name (```HelloYou.java``)` are always the same 
-- every word is capitalized, as this uses PascalCase

<br>

The next line is inside the class, where we have a ```main()``` function, (or ```main()``` method) which lists our program tasks:
```java
  public static void main(String[] args) {
```
Inside the class we have a ```main()``` function, (or ```main()``` method) which lists our program tasks:

Like classes, it uses curly braces ```{ }``` to mark the beginning and end of a function/method

 ```public```, ```static```, and ```void``` are syntax that will be gotten to in future notes. For now, remember that it is boilerplate code (and must be present for the program to run)

```String[] args``` is the type of data being passed to the program  Inside the class we have a ```main()``` function/method which lists our program tasks:

<br>

The program also displays the text "```Hello <programmer name>```" on the screen. This is accomplished using a print statement:

```java
    System.out.println("Hello CBL2C");
```
```System``` is a built-in Java class that contains useful tools for programs

```out``` is short for “output”

```println``` is short for “print line”

<br>

The closing curly braces ```{ }``` signify the ends of the ```main()``` function and the ```HelloYou``` class, respectively: 
```java
  }
}
```

<br>

<br>

## ```println()``` vs. ```print()``` 
**Note: the following is a *different* code example from a *separate* file** - please keep in mind that the code below is in a *separate* file, named [```HideAndSeek.java```](/00_Java_Files/HideAndSeek.java)   
The code in these notes is combined as an easy way to organize learning exercises and notes. In real-word files, there can only be one outer class and the filename must match the class, as it does in each of the corresponding ```.java``` files

The following file will reside in ```HideAndSeek.java```, etc etc

<br>

This file, [```HideAndSeek.java```](/00_Java_Files/HideAndSeek.java) is almost the same code as the [**first example**](#hello-world) above:
```java
public class HideAndSeek {
  public static void main(String[] args) {
    System.out.print("Let's play hide and seek.");
    // prints: Let's play hide and seek.
  }
}
```

The key difference is the usage of ```print()``` instead of ```println)_``` on line 3:
```java
System.out.print("Let's play hide and seek.");
```

It's possible to output information using ```System.out.print()``` -- notice that using ```print()``` has different behavior than ```println()``` that may not be immediately apparent

Unlike using ```System.out.println()```, our second example's use of ```System.out.print()```  outputs **everything *on the same line***

Using ```println()``` would result in:
```java
System.out.println("Hello ");
System.out.println("World");

// Hello 
// World
```

While using ```print()``` would result in:
```java 
System.out.print("Hello ");
System.out.print("World");

// "Hello World"
```