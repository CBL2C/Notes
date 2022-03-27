# Compiling

## What is Compliling?
Consider the following file, [```Compiling.java```](/00_Java_Files/Compiling.java):

```java
public class Compiling {
    public static void main(String[] args) {
        System.out.println("Java is a class-based language.");
        System.out.println("Java clases have a 'main' method.");
        System.out.println("Java statements end with a semicolon.");
        System.out.println("Programming is... fun!");
    }
}
```

As mentioned in [**Intro to Java**](../00_Intro_Printing/00_Intro_HelloYou.md) There are **two types of files** in Java: ```.java``` files, which are human-written and human-readable Java code, and ```.class``` files, which are compiled into byte code - which any computer or device can read using the Java Virtual Machine, or JVM (which is part of the Java Runtime Enviromnment, or JRE)

It is important to note that all ```.java``` files **must** be compiled to be run. The human-readable ```.java``` file is **not** readable by the JVM

To compile a ```.java``` file (such as ```Compiling.java```), open your Terminal of choice (I am partial to VSCode's terminal integration) and navigate to the directory containing your ```.java``` file.  
Then, type the following into your Terminal:

```
javac Compiling.java
```

If your ```.java``` file code does not have errors, the file will compile and return a new file in the same directory called [```Compiling.class```](/00_Java_Files/Compiling.class)

To run the file, type the following into Terminal:  (note that the "```.class```" is not used in this command)

```
java Compiling
```

<br>

## Compiling & Source Changes
So you have successfully compiled your ```.java``` file. You have a ```.class``` file your JRE can run. 

You happily run your file. It works! You celebrate. But amidst your haze of celebration, you see a problem in the output:

```
Java is a class-based language.
Java clases have a 'main' method.
Java statements end with a semicolon.
Programming is... fun!
```

You mis-spelled "classes" on the second printed line!

You open up [```Compiling.java```](/00_Java_Files/Compiling.java) and fix the code:

```java
public class Compiling {
    public static void main(String[] args) {
        System.out.println("Java is a class-based language.");
        System.out.println("Java classes have a 'main' method.");
        System.out.println("Java statements end with a semicolon.");
        System.out.println("Programming is... fun!");
    }
}
```
You save your change and call it a day, thinking that you're all done and you have updated your file 

**HOWEVER,** this change will *not* be reflected in [```Compiling.class```](/00_Java_Files/Compiling.class)!

After you have saved your ```.java``` file, you **must** re-compile your ```.class``` file so that it contains the latest changes. The ```.class``` file the JRE reads **does not auto-update** to reflect changes to the ```.java``` file  
