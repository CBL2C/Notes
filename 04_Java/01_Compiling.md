# Compiling

Consider the following file, [```Compiling.java```](/00_Java_Files/Compiling.java):

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

As mentioned in [**Intro to Java**](../00_Intro_Printing/00_Intro_HelloYou.md) There are **two types of files** in Java: ```.java``` files, which are human-written and human-readable Java code, and ```.class``` files, which are compiled into byte code - which any computer or device can read using the Java Virtual Machine

To compile a file (such as ```Compiling.java```), navigate to the directory containing your ```.java``` file and type the following into the Terminal:

```
javac Compiling.java
```

If your ```.java``` file code does not have errors, the file will compile and return a new file in the same directory called ```Compiling.class```

To run the file, type the following into Terminal:  (note that the "```.class```" is not used in this command)

```
java Compiling
```
