# Object Oriented Programming
> ## Index
 - Class and Objects
 - Methods
 - Constructor
 - Access Modifiers
 - this and final
 - Inheritance
 - super
 - Abstract Class and Method
 - Interface
 - Polymorphism
 - Encapsulation

> ## Class and Objects
```java
// class
class ClassName {
  // fields
  access_modifires data_type field_name;
  // methods
  access_modifires reurn_type func_name();
}

// objects
className object = new className();
// Access Members of a Class
object.field_name;
object.func_name();
```
```java
// Example of class and objects
class Bicycle {

  // field of class
  int gear = 5;

  // method of class
  void braking() {
    ...
  }
}

// create object
Bicycle sportsBicycle = new Bicycle();

// access field and method
sportsBicycle.gear;
sportsBicycle.braking();
```
[^ back to index](#index)
> ## Methods
```java

```
[^ back to index](#index)
> ## Constructor
```java
// Constructors
/*
* A constructor in Java is similar to a method that is invoked  when an object of the class is created.
* It has the same name as that of the class and doesn't have a return type.
*/
class Class_name {
  Class_name(data_type arge1,data_type arge2, data_type argen ) {
    // constructor body
  }
}
```
[^ back to index](#index)
> ## Access Modifires

> **Access Modifiers** are used to set the accessibility (visibility) of classes, interfaces, variables, methods, constructors, data members, and the setter methods.

| Modifier | Description |
|:--:|--|
| `default` | declarations are visible only within the package (package private) |
| `private` | declarations are visible within the class only |
| `protected` | declarations are visible within the package or all subclasses |
| `public` | declarations are visible everywhere |
> **Default Access Modifier**
>
> If we do not explicitly specify any access modifier for classes, methods, variables, etc, then by default the default access modifier is considered.
```java
package defaultPackage;
class Logger {
    void message(){
        System.out.println("This is a message");
    }
}
```
> **Private Access Modifier**
>
> When variables and methods are declared private, they cannot be accessed outside of the class.
```java
class Data {
    // private variable
    private String name;
}
```
> **Protected Access Modifier**
>
> When methods and data members are declared `protected`, we can access them within the same package as well as from subclasses
```java
class Animal {
    // protected method
    protected void display() {
        System.out.println("I am an animal");
    }
}
```
> **Public Access Modifier**
>
> When methods, variables, classes, and so on are declared public, then we can access them from anywhere. The public access modifier has no scope restriction.
```java
public class Animal {
    // public variable
    public int legCount;

    // public method
    public void display() {
        System.out.println("I am an animal.");
        System.out.println("I have " + legCount + " legs.");
    }
}
```
[^ back to index](#index)
> ## this and final

> **this**
>
> `this` keyword is used to refer to the current object inside a method or a constructor.
```java
class Main {
    int instVar;

    Main(int instVar){
        this.instVar = instVar;
        System.out.println("this reference = " + this);
    }

    public static void main(String[] args) {
        Main obj = new Main(8);
        System.out.println("object reference = " + obj);
    }
}
```
**Output**
```bash
this reference = Main@23fc625e
object reference = Main@23fc625e
```
> **final**
>
> In Java, the final keyword is used to denote constants. It can be used with variables, methods, and classes.
> - the final variable cannot be reinitialized with another value
> - the final method cannot be overridden
> - the final class cannot be extended
```java
class Main {
  public static void main(String[] args) {

    // create a final variable
    final int AGE = 32;

    // try to change the final variable
    AGE = 45;
    System.out.println("Age: " + AGE);
  }
}
```
**Output**
```bash
cannot assign a value to final variable AGE
    AGE = 45;
    ^
```
> **final Method**
> 
> In Java, the final method cannot be overridden by the child class.
```java
class FinalDemo {
    // create a final method
    public final void display() {
      System.out.println("This is a final method.");
    }
}

class Main extends FinalDemo {
  // try to override final method
  public final void display() {
    System.out.println("The final method is overridden.");
  }

  public static void main(String[] args) {
    Main obj = new Main();
    obj.display();
  }
}
```
**Output**
```bash
 display() in Main cannot override display() in FinalDemo
  public final void display() {
                    ^
  overridden method is final
```
> **final Class**
>
> the final class cannot be inherited by another class
```java
// create a final class
final class FinalClass {
  public void display() {
    System.out.println("This is a final method.");
  }
}

// try to extend the final class
class Main extends FinalClass {
  public  void display() {
    System.out.println("The final method is overridden.");
  }

  public static void main(String[] args) {
    Main obj = new Main();
    obj.display();
  }
}
```
**Output**
```bash
cannot inherit from final FinalClass
class Main extends FinalClass {
                   ^
```
[^ back to index](#index)
> ## Inheritance
```java
// The extends keyword is used to perform inheritance in Java.
class Animal {
  // methods and fields
}

// use of extends keyword
// to perform inheritance
class Dog extends Animal {

  // methods and fields of Animal
  // methods and fields of Dog
}
```
| Example
```Java
class Animal {

  // field and method of the parent class
  String name;
  public void eat() {
    System.out.println("I can eat");
  }
}

// inherit from Animal
class Dog extends Animal {

  // new method in subclass
  public void display() {
    System.out.println("My name is " + name);
  }
}

class Main {
  public static void main(String[] args) {

    // create an object of the subclass
    Dog labrador = new Dog();

    // access field of superclass
    labrador.name = "Rohu";
    labrador.display();

    // call method of superclass
    // using object of subclass
    labrador.eat();

  }
}
```
**Output**
```bash
My name is Rohu
I can eat
```
[^ back to index](#index)
> ## super

> The `super` keyword in Java is used in subclasses to access superclass members (attributes, constructors and methods).

```java
class Animal {
  // Parent Constructor
  Animal(String name) {
    // body...
  }
  // overridden method
  public void display(){
    System.out.println("I am an animal");
  }
}

class Dog extends Animal {
  // Child Constructor
  Dog(String name) {
    // this will call Parent Constructor
    super(name);
  }

  // overriding method
  @Override
  public void display(){
    System.out.println("I am a dog");
  }

  public void printMessage(){

    // this calls overriding method
    display(); // "I am a dog"

    // this calls overridden method
    super.display(); // "I am an animal"
  }
}

class Main {
  public static void main(String[] args) {
    Dog dog1 = new Dog();
    dog1.printMessage();
  }
}

```
[^ back to index](#index)
> ## Abstract Class and Method
```java

```
[^ back to index](#index)
> ## Inerface

> An **interface** is a fully abstract class. It includes a group of abstract methods (methods without a body).
```java
interface Language {
  public void getType();

  public void getVersion();
}

class Hindi implements Laguage {
  public void getType() {
    // Body
  }

  public void getVersion() {
    // Body
  }
}
```
| Example
```java
interface Polygon {
  void getArea(int length, int breadth);
}

// implement the Polygon interface
class Rectangle implements Polygon {

  // implementation of abstract method
  public void getArea(int length, int breadth) {
    System.out.println("The area of the rectangle is " + (length * breadth));
  }
}

class Main {
  public static void main(String[] args) {
    Rectangle r1 = new Rectangle();
    r1.getArea(5, 6); // The area of the rectangle is 30
  }
}
```
### Implementing Multiple Interfaces
```Java
interface A {
  // members of A
}

interface B {
  // members of B
}

class C implements A, B {
  // abstract members of A
  // abstract members of B
}
```
### Extending an Interface
```java
interface Line {
  // members of Line interface
}

// extending interface
interface Polygon extends Line {
  // members of Polygon interface
  // members of Line interface
}interface Line {
  // members of Line interface
}

// extending interface
interface Polygon extends Line {
  // members of Polygon interface
  // members of Line interface
}
```
### Extending Multiple Interfaces
```java
interface A {
   ...
}
interface B {
   ... 
}

interface C extends A, B {
   ...
}
```
### default methods in Java Interfaces
```java
public default void getSides() {
   // body of getSides()
}
```
```java
interface Polygon {
  void getArea();

  // default method 
  default void getSides() {
    System.out.println("I can get sides of a polygon.");
  }
}

// implements the interface
class Rectangle implements Polygon {
  public void getArea() {
    int length = 6;
    int breadth = 5;
    int area = length * breadth;
    System.out.println("The area of the rectangle is " + area);
  }

  // overrides the getSides()
  public void getSides() {
    System.out.println("I have 4 sides.");
  }
}

// implements the interface
class Square implements Polygon {
  public void getArea() {
    int length = 5;
    int area = length * length;
    System.out.println("The area of the square is " + area);
  }
}

class Main {
  public static void main(String[] args) {

    // create an object of Rectangle
    Rectangle r1 = new Rectangle();
    r1.getArea();
    r1.getSides();

    // create an object of Square
    Square s1 = new Square();
    s1.getArea();
    s1.getSides();
  }
}
```
[^ back to index](#index)
> ## Polymorphism
```java

```
[^ back to index](#index)
> ## Encapsulation
```java

```
[^ back to index](#index)