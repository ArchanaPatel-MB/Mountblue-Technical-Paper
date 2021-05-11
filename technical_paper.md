# OOPs (Object-Oriented Programming System)

Object means a real-world entity such as a pen, chair, table etc. Object-Oriented Programming is a methodology or paradigm to design a program using classes and objects. It simplifies software development and maintenance by providing some concepts:

    Object
    Class
    Inheritance
    Polymorphism
    Abstraction
    Encapsulatio

Apart from these concepts, there are some other terms which are used in Object-Oriented design:

    Coupling
    Cohesion
    Association
    Aggregation
    Composition

## Object

Any entity that has state and behavior is known as an object. For example, a chair, pen, table, keyboard, bike, etc. It can be physical or logical. An Object can be defined as an instance of a class. An object contains an address and takes up some space in memory. Objects can communicate without knowing the details of each other's data or code. The only necessary thing is the type of message accepted and the type of response returned by the objects. Example: A dog is an object because it has states like color, name, breed, etc. as well as behaviors like wagging the tail, barking, eating, etc.
### Create an Object

In Java, an object is created from a class. We have already created the class named MyClass, so now we can use this to create objects. To create an object of MyClass, specify the class name, followed by the object name, and use the keyword new: Example Create an object called "myObj" and print the value of x:
```java
public class Main { int x = 5;

public static void main(String[] args) { Main myObj = new Main(); System.out.println(myObj.x); } } 
```
## Class
Collection of objects is called class. It is a logical entity. A class can also be defined as a blueprint from which you can create an individual object. Class doesn't consume any space. Create a Class

To create a class, use the keyword class: Main.java

Create a class named "Main" with a variable x:
```java
public class Main { int x = 5; }
```

## Inheritance
When one object acquires all the properties and behaviors of a parent object, it is known as inheritance. It provides code reusability. It is used to achieve runtime polymorphism. Example
```java
class Vehicle { protected String brand = "Ford"; // Vehicle attribute public void honk() { // Vehicle method System.out.println("Tuut, tuut!"); } }

class Car extends Vehicle { private String modelName = "Mustang"; // Car attribute public static void main(String[] args) {

// Create a myCar object
Car myCar = new Car();

// Call the honk() method (from the Vehicle class) on the myCar object
myCar.honk();

// Display the value of the brand attribute (from the Vehicle class) and the value of the modelName from the Car class
System.out.println(myCar.brand + " " + myCar.modelName);

} }
```

## Polymorphism
If one task is performed in different ways, it is known as polymorphism. For example: to convince the customer differently, to draw something, for example, shape, triangle, rectangle, etc. In Java, we use method overloading and method overriding to achieve polymorphism. Another example can be to speak something; for example, a cat speaks meow, dog barks woof, etc.

Example
```java
class Animal { public void animalSound() { System.out.println("The animal makes a sound"); } }

class Pig extends Animal { public void animalSound() { System.out.println("The pig says: wee wee"); } }

class Dog extends Animal { public void animalSound() { System.out.println("The dog says: bow wow"); } }
```

## Abstraction
Data abstraction is the process of hiding certain details and showing only essential information to the user. Abstraction can be achieved with either abstract classes or interfaces (which you will learn more about in the next chapter).

The abstract keyword is a non-access modifier, used for classes and methods:

### Abstract class: is a restricted class that cannot be used to create objects (to access it, it must be inherited from another class).

### Abstract method: can only be used in an abstract class, and it does not have a body. The body is provided by the subclass (inherited from).

An abstract class can have both abstract and regular methods:
```java 
abstract class Animal { public abstract void animalSound(); public void sleep() { System.out.println("Zzz"); } }
```

From the example above, it is not possible to create an object of the Animal class:
```java 
Animal myObj = new Animal(); // will generate an error
```

To access the abstract class, it must be inherited from another class.


## Encapsulation
The meaning of Encapsulation, is to make sure that "sensitive" data is hidden from users. To achieve this, you must:

declare class variables/attributes as private
provide public get and set methods to access and update the value of a private variable

Syntax for both is that they start with either get or set, followed by the name of the variable, with the first letter in upper case: Example
```java
public class Person { private String name; // private = restricted access

// Getter public String getName() { return name; }

// Setter public void setName(String newName) { this.name = newName; } }
```
![oops image](https://images.app.goo.gl/FAC3qdmGPZBWzLpa7)
## Coupling
Coupling refers to the knowledge or information or dependency of another class. It arises when classes are aware of each other. If a class has the details information of another class, there is strong coupling. In Java, we use private, protected, and public modifiers to display the visibility level of a class, method, and field. You can use interfaces for the weaker coupling because there is no concrete implementation.

## Cohesion
Cohesion refers to the level of a component which performs a single well-defined task. A single well-defined task is done by a highly cohesive method. The weakly cohesive method will split the task into separate parts. The java.io package is a highly cohesive package because it has I/O related classes and interface. However, the java.util package is a weakly cohesive package because it has unrelated classes and interfaces.

## Association

Association represents the relationship between the objects. Here, one object can be associated with one object or many objects. There can be four types of association between the objects:

One to One
One to Many
Many to One, and
Many to Many

Real time example,i.e. One country can have one prime minister (one to one), and a prime minister can have many ministers (one to many). Also, many MP's can have one prime minister (many to one), and many ministers can have many departments (many to many). Association can be undirectional or bidirectional.


## Aggregation
Aggregation is a way to achieve Association. Aggregation represents the relationship where one object contains other objects as a part of its state. It represents the weak relationship between objects. It is also termed as a has-a relationship in Java. Like, inheritance represents the is-a relationship. It is another way to reuse objects.


## Composition
The composition is also a way to achieve Association. The composition represents the relationship where one object contains other objects as a part of its state. There is a strong relationship between the containing object and the dependent object. It is the state where containing objects do not have an independent existence. If you delete the parent object, all the child objects will be deleted automatically.


Links
[visit website] (https://www.geeksforgeeks.org/object-oriented-programming-oops-concept-in-java/)
