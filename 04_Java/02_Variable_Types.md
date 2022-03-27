# Variables
**There are many types of variables in Java**:

- [```int```](#int--integers) | **Integers**  -  whole numbers
- [```double```](#double--decimals) | **Decimals** - decimal numbers 
- [```boolean```](#boolean--true--false) | **Booleans** - true or false, 1 or 0
- [```char```](#char--single-character) | **Characters** - single alphabetic character or symbol

<br>

## ```int``` | Integers 

```int``` can only hold values between -2,147,483,648 and 2,147,483,647, inclusive

[```CountComment.java```](/00_Java_Files/CountComment.java) uses ```int```:
```java
public class CountComment {
    public static void main(String[] args) { 

    int numComments = 6;
    // This is the int variable numComments, which holds the value of 6

    System.out.println(numComments);
    // This prints out the value of numComments
      }
  }
```

<br>

<br>

## ```double``` | Decimals

```double``` can hold far larger and smaller numbers than ```int```

The maximum and minum values of ```double``` are huge:
- the maximum value is 1.797,693,134,862,315,7 E+308, which is approximately 17 followed by 307 zeros 
- the minimum value is 4.9 E-324, which is 324 decimal places

```double``` can also handle decimal places, while int cannot 

[```MarketShare.java```](/00_Java_Files/MarketShare.java) uses ```double```:
```java
public class MarketShare {
	public static void main(String[] args) {

    double androidShare = 81.7;
        // this is the double variable androidShare, which holds the value of 81.7

    System.out.println(androidShare);
        // this prints out the value of androidShare
	}
}
```

<br>

<br>

## ```boolean``` | True & False

```boolean``` is a type of variable that references one of two values: true or false

[```Booleans.java```](/00_Java_Files/Booleans.java) uses ```boolean```:
```java
public class Booleans {
	public static void main(String[] args) { 

    boolean intsCanHoldDecimals = false;
        // this is the boolean variable intsCanHoldDecimals, which holds the value of false


    System.out.println(intsCanHoldDecimals);
        // this prints out the value of intsCanHoldDecimals
	}
}
```

<br>

<br>

## ```char``` |  Single Character

```char``` is a type of variable that represents a single alphabetical character, or a symbol

[```Symbols.java```](/00_Java_files/Symbols.java)

```java
public class Symbols {
    public static void main(String[] args) { 

        char cashSymbol = $;
        // This is the char variable cashSymbol, which holds the value of $
    
        char firstInitial = M;
        // This is the char variable firstInitial, which holds the value of M

        System.out.println(cashSymbol);
        // This prints out the value of cashSymbol

        System.out.println(firstInitial);
        // This prints out the value of firstInitial
    }
}
```