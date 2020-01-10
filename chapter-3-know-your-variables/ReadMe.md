### Table Of Contents

- Declaring a Variable
- assigning primitive variables
- You really don't want to spill that
- Objects
- Arrays

### Declaring a Variable

—  Java cares about type. It won't let you do something bizarre and dangerous like stuff a Giraffe reference into a Rabbit variable—what happens when someone tries to ask the so-called Rabbit to hop()? And it won't let you put a floating point number into an integer variable, unless you acknowledge to the compiler that you know you might lose precision (like, everything after the decimal point). There are two declaration rules to follow: variables must have a type and variables must have a name. The two types of variables are primitive and object reference. 

- Primitive - hold fundamental values (think: simple bit patterns) including integers, booleans, and floating point numbers.
- Object Reference - hold, well, references to objects

int count;

*When you see a statement like: "an object of type "X", think of type and class as synonyms.

### assigning primitive variables

—  When you think of Java variables, think of cups. Coffee cups, teacups, giant cups that hold lots and lots of beer, those big cups the popcorn comes in at the movies, cups with curvy handles, and cups with metallic. **A variable is just a cup. A container. It holds something.** It has a size and a type. 

In Java, primitives come in different sizes, and those sizes have names. When you declare a variable in Java you must declare it with a specific type. The four integer primitives in Java. Each cup holds a value, so for Java primitives, you say to the compiler, "I'd like an int variable with the number 90 please." and you also have to give your cup a name. So it's actually, "I'd like an int please, with the value of 2486, and name the variable 'height',". Each primitive variable has a fixed number of bits (cup size).  (ex: byte - 8, short - 16, int - 32, long - 64, float - 34, double - 64)

### You really don't want to spill that

—  You can't put a large value into a small cup. If you do there will be **spillage**. 

For example you can pour an int-full of stuff into a byte-sized container, as follows:

```java
int x = 24;
byte b = x;
// This won't work
```
Why doesn't this work? The value of "x" is 24 and 24 is definitely small enough to fit into a byte. We know this but all the compiler knows is that you are trying to put a big thing in a small thing and there is a chance of spillage. Don't expect the compiler to know what the value of "x" is. 

### Objects

- There's actually no such thing as an object variable
- There's only an object reference variable
- It doesn't hold the object itself, but it holds something like a pointer. Or an address. Except, in Java we don't really know what is inside a reverence variable. We do know that whatever it is, it represents one and only one object. And the JVM knows how to use the reference to get to the object.

### Arrays

1. Declare an int array variable. An array variable is a remote control to an array object.

int[] nums;

2. Create a new int array with a length of 7, and assign it to the previously declared int[] variable nums.

nums = new int[7]

3. Give each element in the array an int value. Remember, elements in an int array are just int variables.

```java
nums[0] = 6;
nums[1] = 19;
nums[2] = 44;
nums[3] = 42;
nums[4] = 10;
nums[5] = 20;
nums[6] = 1;
```
### Make an array of Dogs

1. Declare a Dog array variable

```java
Dog[] pets;
```
2. Create a new Dog array with a length of 7, and assign it to the previously-declared Dog[] variable pets

```java
pets = new Dog[7]
```
3. Create new Dog objects, and assign them to the array elements. Remember, elements in a Dog array are just Dog reference variables. We still need Dogs.

```java
pets[0] = new Dog();
pets[1] = new Dog();
```
### Control your Dog (with a reference variable)

```java
Dog fido = new Dog();
fido.name = "Fido";
```
—  I created a Dog object and used the dot operator on the reference variable "fido" to acces the name variable. We can use the fido reference to make the dog bark(), eat(), or chaseCat()

```java
fido.bark();
fido.chaseCat();
```
### Code Magnets

```java
class TestArrays {
    public static void main(String[] args) {
        int [] index = new int[4];

        index[0] = 1;
        index[1] = 3;
        index[2] = 0;
        index[3] = 2;

        String [] islands = new String[4];

        islands[0] = "Bermuda";
        islands[1] = "Fiji";
        islands[2] = "Azores";
        islands[3] = "Cozumel";

        int y = 0;

        int ref;

        while (y < 4) {
            ref = index[y];

            System.out.print("island = ");
            System.out.println(islands[ref]);

            y = y + 1;
        }
    }
}
```
### Overview

—  Variables must have a type and a name. The two types are Primitives and Object Reference. Primitive variable have a certain size and type. You cannot put something large in something small or you will get spillage. There are no object variables only object reference variables. A reference variable is like a remote, by using the dot operator on a reference variable is like mashing the button on a remote to access a method or instance variable.