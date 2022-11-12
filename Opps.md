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
[^ back to index](#index)
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
> ## this and final
```java

```
[^ back to index](#index)
> ## Inheritance
```java

```
[^ back to index](#index)
> ## super
```java

```
[^ back to index](#index)
> ## Abstract Class and Method
```java

```
[^ back to index](#index)
> ## Inerface
```java

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