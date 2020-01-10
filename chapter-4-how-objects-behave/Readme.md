### Table of contents

- A class describes what an object knows and does
- The size affects the bark
- You can send things to a method
- You can get things back from a method

### A class describes what an object knows and does

—  A class is the blueprint for an object. When you write a class, you're describing how the JVM should make an object of that type.

### The size affects the bark

—  A small Dog's bark is different from a big Dog's bark. The Dog class has an instance variable size, that the bark() method uses to decide what kind of bark sound to make

```java
class Dog {
    int size;
    String name;

    void bark() {
        if (size > 60) {
            System.out.println("Woof! Woof!");
        } else if (size > 14) {
            System.out.println("Ruff! Ruff!");
        } else {
            System.out.println("Yip! Yip!");
        }
    }
}

class DogTestDrive {
    public static void main(String[] args) {
        Dog one = new Dog();
        one.size = 70;

        Dog two = new Dog();
        two.size = 8;

        Dog three = new Dog();
        three.size = 35;

        one.bark();
        two.bark();
        three.bark();
    }
}
```
### You can send things to a method

—  You can pass values into your methods. You might, for example, want tot tell a Dog object how many times to bark

```java
d.bark(3);
```
### You can get things back from a method

—  Methods can return values. Every method is declared with a return type, but until now we've made all of our methods with a void return type, which means they don't give anything back.

```java
void go() {

}
```
But we can declare a method to give a specific type of value back to the caller, such as:

```java
int giveSecret() {
    return 42;
}
```
If you declare