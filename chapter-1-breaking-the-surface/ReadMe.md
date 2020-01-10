# Chapter 1:

### Table of Contents

- The Way Java Works
- History of Java
- What is the structure
- Anatomy of a class
- Writing a class with a main
- What can you say in the main method
- Conditional branching
- Coding a serious business application

### The Way Java Works

1. Create a source document. Use an established protocol (in this case, the Java language)
2. Run your document through a compiler to check for errors. 
3. The compiler creates a new document coded into Java (bytecode), so any machine capable of running Java will be able to run this.
4. Your friends don't have a physical Java Machine,  but they all have a virtual Java machine.

### History of Java

**Java 1.02**

- 250 classes
- slow
- lots of bugs
- Applets are the big thing

**Java 1.1**

- 500 classes
- A little faster
- More capable, friendlier
- Becoming very popular

**Java 2 (version 1.2 - 1.4)**

- 2300 classes
- Much faster
- powerful
- Becomes the language of choice

**Java 5.0 (tiger)**

- 3500 classes
- More power and easier to develop with
- New features popular in other languages

### What is the structure?

- Put a class in a source file
- Put methods in a class
- put statements in a method

—  A source file holds one class definition. The class represents a piece of your program, although a very tiny application might need just a single class. The class must go within a par of curly braces. 

```java
public class Dog {

}
```
—  A class has one or more methods. In the Dog class, the bark method will hold instructions for how the Dog should bark. Your methods must be declared inside a class (within the curly braces of the class).

```java
public class Dog {
    void bark() {
    }
}
```
—  Within the curly braces of a method, write your instructions for how that method should be performed. Method code is basically a set of statements, and for now you can think of a method kind of like a function or procedure.

```java
public class Dog {
    void bark() {
        statement1;
        statement2;
    }
}
```
### Anatomy of a class

—  When the JVM starts running, it looks for the class you give it at the command line. Then it starts looking for a specially-written method that look exactly like the following

```java
public static void main (String[] args) {
    
}
```
### Writing a class with a main

— In Java, everything goes into a class. You'll type your source code file, then compile it into a new class file. When you run your program, you're really running a class.

—  Running a program means telling the Java Virtual Machine (JVM) to "Load the Hello class, then start executing its main() method.

### What can you say in the main method?

—  Once you're inside main, the fun begins. You can say all the normal things that you say in most programming languages to make the computer do something. 

—  Your code can tell the JVM to:

1. Do something

```java
int x = 3;
String name = "Dirk";
x = x * 17;
System.out.print("x is " + x);
double d = Math.random();
```
2. Do something again and again:

```java
while (x > 12) {
    x = x -1;
}
for (int x = 0; x < 10; x = x + 1) {
    system.out.print("x is now " + x);
}
```
3. Do something under this condition:

```java
if (x == 10) {
    System.out.print("x must be 10");
} else {
        System.out.print("x isn't 10");
}
if ((x < 3) & (name.equals("Dirk"))) {
    System.out.println("Gently");
}
System.out.print("this line runs no matter what");
```
### Conditional branching

—  In Java, an if test is basically the same as the boolean test in a while loop - except instead of saying, "while there's still beer...", you'll say, "if there's still beer..."

### Coding a serious business application

```java
public class BeerSong {
    public static void main(String[] args) {
        int beerNum = 99;
        String word = "bottles";

        while (beerNum > 0) {
            if (beerNum == 1) {
                word = "bottle";
            }

            System.out.println(beerNum + " " + word + " of beer on the wall");
            System.out.println(beerNum + " " + word + " of beer.");
            System.out.println("Take one down.");
            System.out.println("Pass it around.");
            beerNum = beerNum - 1;

            if (beerNum > 0) {
                System.out.println(beerNum + " " + word + " of beer on the wall");
            } else {
                System.out.println("No more bottles of beer on the wall");
            }
        }
    }
}
```
### Code magnets

```java
class Shuffle1 {
    public static void main(String[] args) {
        int x = 3;
        while (x > 0) {

            if (x > 2) {
                System.out.print("a");
            }

            x = x - 1;
            System.out.print("-");

            if (x == 2) {
                System.out.print("b c");
            }

            if (x == 1) {
                System.out.print("d");
                x = x - 1;
            }
        }
    }
}
```
### Overview

—