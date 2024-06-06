# Java-
Java is an object-oriented, high-level programming language created by Sun Microsystems, which Oracle Corporation eventually purchased. Java is built with the following fundamental ideas and characteristics:
Important Concepts of Java Object-Oriented: Java employs an object-oriented programming paradigm, which groups software architecture using objects and classes. Important ideas are abstraction, encapsulation, polymorphism, and inheritance.

Platform-Independent: Java programs are translated into bytecode, which is executable on any hardware that has a Java Virtual Machine installed (JVM). One of Java's biggest benefits is its "write once, run anywhere" flexibility.

Robust and Secure: Java places a high emphasis on memory management, runtime checking, and early error checking. Its robustness is enhanced by features like type checking, exception handling, and garbage collection. Furthermore, Java includes built-in security capabilities such as access control definitions in a security manager and bytecode verification.

Multithreaded: Java has built-in support for many threads, which makes it possible to create incredibly responsive and interactive programs.

Distributed: With a large number of libraries that make dealing with TCP/IP protocols like HTTP and FTP easier, Java is built to handle distributed computing. Methods that operate on remote objects can be invoked using the Remote Method Invocation (RMI) framework.

High Performance: Despite being an interpreted language, Java programs execute almost as quickly as native C or C++ programs thanks to innovations like Just-In-Time (JIT) compilers and performance optimization strategies.

Difference between dynamically typed and Statically typed:
Dynamically typed:
Variable types are determined at runtime through context in the code.

Statically typed:
Variable types must be declared before the program can be compiled.


Core Components of Java
Java Development Kit (JDK): The JDK provides the tools necessary to develop Java applications, including the Java compiler (javac), libraries, and other development tools.

Java Runtime Environment (JRE): The JRE provides the libraries, JVM, and other components necessary to run Java applications.

Java Virtual Machine (JVM): The JVM executes Java bytecode and enables the platform-independent nature of Java.

Java Structure and Syntax
Although Java syntax is simpler and does away with many of the intricacies and dangers found in C++, it is nevertheless heavily influenced by C++. Here are a few essential elements:
Classes and Objects: The basic building blocks of Java programs. Classes define the structure and behavior (data members and methods) of objects.EG:
public class MyClass {
    int myNumber;
    String myString;

    // Constructor
    public MyClass(int number, String str) {
        myNumber = number;
        myString = str;
    }

    // Method
    public void display() {
        System.out.println("Number: " + myNumber + ", String: " + myString);
    }
}

// Creating an object
MyClass obj = new MyClass(25, "Hello");
obj.display();


Inheritance: Java supports inheritance, allowing new classes to be derived from existing classes, promoting code reuse and method overriding.EG:
public class Animal {
    public void eat() {
        System.out.println("This animal eats food.");
    }
}

public class Dog extends Animal {
    @Override
    public void eat() {
        System.out.println("The dog eats bones.");
    }
}

// Using the inherited method
Dog dog = new Dog();
dog.eat();

Interfaces and Abstract Classes: Java uses interfaces and abstract classes to achieve abstraction and multiple inheritance. Eg:
public interface Animal {
    void eat();
}

public class Dog implements Animal {
    public void eat() {
        System.out.println("The dog eats bones.");
    }
}



Decision Structres in Java:
Java decision structures let the program take alternative routes of execution depending on how particular conditions turn out. There are various kinds of decision-making statements available in Java:

if  Statement:
If the boolean expression is true, the if statement evaluates it and runs the code block inside.Eg:
int number = 10;
if (number > 0) {
    System.out.println("The number is positive.");
}

if-else Statement:
The if-else statement provides an alternative path of execution if the condition is false.Eg:
int number = -5;
if (number > 0) {
    System.out.println("The number is positive.");
} else {
    System.out.println("The number is not positive.");
}

if-else-if Ladder:
The if-else-if ladder allows multiple conditions to be checked sequentially. The first true condition's block is executed.Eg:
int number = 0;
if (number > 0) {
    System.out.println("The number is positive.");
} else if (number < 0) {
    System.out.println("The number is negative.");
} else {
    System.out.println("The number is zero.");
}

Nested if Statement:
int number = 5;
if (number > 0) {
    if (number % 2 == 0) {
        System.out.println("The number is positive and even.");
    } else {
        System.out.println("The number is positive and odd.");
    }
}

switch Statement
The switch statement is used to execute one block of code from multiple choices based on the value of an expression.
switch (expression).Eg:
{
    case value1:
        // code to be executed if expression == value1
        break;
    case value2:
        // code to be executed if expression == value2
        break;
    // more cases
    default:
        // code to be executed if none of the cases match
}


Methods in Java:



Inheritance:
Got two players a parent and a child, the parent is also called superclass, parent class or base class that passes down its stuff to the child, also known as subclass, child class.
Eg:
This 'Person' class contains attributes like 'name,' 'age,' and 'gender,' and we have methods to set and retrieve those. You can use the keyword "extends" in the 'Employee' class header to create a class that is similar to 'Person,' but has additional information specific to employees. 

#Remember, we cannot see the fields themselves because they are private in the Person class. Private stuff does not get inherited; only the protected and public stuff does. 

Constructor in inheritance:
When it comes to constructors and inheritance, some intriguing aspects are involved. Consider that you have two classes: one called "person" and the other named "employee," both of which have default constructors that read "in-person default constructor." The constructor of the 'person' superclass is called before the constructor of the 'employee' subclass is executed when a new instance of the class is created.


It must be the first thing the subclass constructor does when you explicitly invoke a superclass constructor. Java demands it. You will encounter a compilation issue if you move it to another location.
It is also necessary for the subclass to explicitly invoke one of the superclass's other constructors if the superclass lacks a default constructor. An error will appear if you remove the'super' call from the 'employee,' delete the default constructor from the 'person,' and more. One of the remaining constructors must be called in order to fix it. You're set to go once you place the "super" call back at the top. 

Overriding and Overloading Inherited Methods:
A subclass inherits everything (referred to as members) from its superclass automatically. Occasionally, a subclass want to modify a method's operation and carry it out in a slightly different way. Fear not—you may accomplish this by overriding the technique you were given.

It is a good idea to use the "override" annotation (that is the "@" symbol followed by "override"). It is not a requirement, but highly recommended. It tells Java that you are intentionally replacing the method from my super class. This helps avoid mix-ups. Without that "override" tag, you might think you are replacing a method when you are not, and Java will set you straight if you make that mistake. 

Remember, overriding means you keep the same method name and just change what it does, while overloading means you keep the name but change the input it can take. 

Chain of Inheritance:
A class in Java has only one superclass from which it can inherit, but that superclass can also inherit from other classes. As a result, a subclass inherits from its ancestor classes, forming a chain of inheritance. Take a Vehicle class, for example, which has mileage and color fields in addition to getter and setter methods. The Car class follows, which adds a doors field and associated methods after inheriting from Vehicle. The last class is the Coupe class, which has two doors and inherits from the Car class.

Let's construct an instance of Coupe, "myCar," and set its color to red to test this chain of inheritance. Surprisingly, myCar can be assigned a color even though the Coupe and Car classes lack a "setColor" method. This is so because it is inherited by Coupe from Vehicle, its ancestor.

Limiting Access in Inheritance:
A subclass does not inherit everything when it comes from a superclass. For example, constructors are not included in this inheritance. They fall behind because they are not seen as classmates. Regarding the other aspects of the superclass, such as the public and protected fields and methods, those are unquestionably inherited. These exclusive techniques and domains don't. They continue to be superclass only.

Sealed classes:
Java classes can decide what can be inherited by them. They can even declare, "No inheritance for anybody except a few," in which case they fall into the category known as "sealed classes." 
We may seal this in the code, for example, if we have classes for shapes like circle, rectangle, and square, and we only want the circle and rectangle to derive from the main shape class. All that needs to be done is add a "sealed" label before the class and a "permits" section just in front of the curly braces. List the classes that are permitted to inherit from this sealed one there. 

Sealed means they follow the same rules as their parent.
Non-sealed means they are open for anyone to extend them. 
Final, on the other hand, means they are off-limits for inheritance.

Polymorphism:
Basically allows objects of different classes to be treated as objects of a common superclass. It enables a single interface to be used for a general class of actions. The main benefit of it is that it helpts in designing systems that are extensible and maintainable.Eg
class Animal {
    void sound() {
        System.out.println("Animal sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

Animal animal = new Dog();
animal.sound(); // Outputs: Dog barks

Casting and Typing of Objects
Casting is the process of changing an object's type; object typing refers to the type given to a variable. Upcasting, or casting to a superclass type, and downcasting, or casting to a subclass type, are the two forms of casting.Eg:
Upcasting:
Dog dog = new Dog();
Animal animal = dog; // Implicit upcasting

Down Casting:
Animal animal = new Dog();
Dog dog = (Dog) animal; // Explicit downcasting

instanceof Operator:
The instanceof operator checks if an object is an instance of a specific class or subclass. It returns true or false.
Animal animal = new Dog();
if (animal instanceof Dog) {
    System.out.println("animal is a Dog");
}

Abstraction:
Is one of the key concept in OOP that focuses on hiding the complex implementation details and showinf only the essential features of an object. It allows you to create a clear seperation between what an object does and how it does it.

Abstract Classes
Concrete methods have a body, whereas abstract methods do not, and an abstract class might have both types of methods (methods without a body). It acts as a model for subsequent classes.
Declaring an Abstract Class:
abstract class Animal {
    // Abstract method (does not have a body)
    abstract void sound();

    // Regular method
    void sleep() {
        System.out.println("This animal is sleeping.");
    }
}

Inheriting from Abstract Classes
A subclass must provide implementations for all abstract methods declared in its abstract superclass. If the subclass does not implement all the abstract methods, it must also be declared as abstract.Eg:
class Dog extends Animal {
    // Providing implementation for the abstract method
    void sound() {
        System.out.println("Dog barks");
    }
}
Dog dog = new Dog();
dog.sound();  // Outputs: Dog barks
dog.sleep();  // Outputs: This animal is sleeping.

Creating Objects with Abstract Types
You cannot create an instance of an abstract class directly, but you can create references to the abstract type and instantiate subclasses that implement the abstract methods.This approach is often used to achieve polymorphism, where a parent class reference is used to refer to a child class object.Eg:
Animal myDog = new Dog();  // Polymorphic behavior
myDog.sound();  // Outputs: Dog barks
myDog.sleep();  // Outputs: This animal is sleeping.

Interfaces:
Java interfaces are abstract types that let you define the set of methods that a class has to have. They do not supply any implementation for the methods themselves, but they do create a contract that implementing classes have to meet.Eg:
public interface Animal {
    void sound();
    void sleep();
}

Implementing interfaces
A class implements an interface by providing concrete implementations for all the methods defined in the interface.Eg:
public class Dog implements Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks");
    }

    @Override
    public void sleep() {
        System.out.println("Dog sleeps");
    }
}

Instantiating Objects with Interface Types
You cannot instantiate an interface directly, but you can create a reference variable of the interface type and assign it to an object of a class that implements the interface. This allows for polymorphic behavior.Eg:
Animal myDog = new Dog();
myDog.sound();  // Outputs: Dog barks
myDog.sleep();  // Outputs: Dog sleeps

Default Methods:
Default methods are instance methods defined in the interface with a default implementation. Implementing classes can use or override these methods.Eg:
public interface Animal {
    void sound();

    default void sleep() {
        System.out.println("This animal is sleeping.");
    }
}

Static Methods:
Static methods are defined in the interface and can be called on the interface itself, not on instances of the implementing classes.Eg:
public interface Animal {
    void sound();

    static void info() {
        System.out.println("Animals can make sounds and sleep.");
    }
}

// Calling the static method
Animal.info();  // Outputs: Animals can make sounds and sleep.


Data Structure:
In Java, data structures are basic building blocks that are used to store and arrange data. They are necessary for effective data modification and administration. There are numerous built-in data structures in Java, each appropriate for a particular use case.

Arrays
Arrays are fixed-size data structures that store elements of the same type. They allow for fast access to elements using an index.
int[] numbers = {1, 2, 3, 4, 5};
System.out.println(numbers[2]);  // Outputs: 3


ArrayList
ArrayList is a resizable array implementation of the List interface. It allows dynamic resizing, and elements can be added or removed.
import java.util.ArrayList;

ArrayList<String> names = new ArrayList<>();
names.add("Alice");
names.add("Bob");
System.out.println(names.get(1));  // Outputs: Bob

LinkedList
LinkedList implements the List and Deque interfaces, providing a doubly linked list structure. It allows for fast insertions and deletions.

import java.util.LinkedList;

LinkedList<String> queue = new LinkedList<>();
queue.add("Alice");
queue.add("Bob");
System.out.println(queue.remove());  // Outputs: Alice


HashMap
HashMap is a hash table implementation of the Map interface. It stores key-value pairs and provides constant-time performance for basic operations like get and put.Eg:
import java.util.HashMap;

HashMap<String, Integer> ages = new HashMap<>();
ages.put("Alice", 25);
ages.put("Bob", 30);
System.out.println(ages.get("Alice"));  // Outputs: 25

HashSet
HashSet implements the Set interface and is backed by a hash table. It stores unique elements and provides constant-time performance for basic operations.Eg:
import java.util.HashSet;

HashSet<String> uniqueNames = new HashSet<>();
uniqueNames.add("Alice");
uniqueNames.add("Bob");
uniqueNames.add("Alice");  // Duplicate element
System.out.println(uniqueNames.size());  // Outputs: 2

Stack
Stack is a last-in, first-out (LIFO) data structure. Java provides the Stack class that extends Vector.Eg:
import java.util.Stack;

Stack<Integer> stack = new Stack<>();
stack.push(1);
stack.push(2);
System.out.println(stack.pop());  // Outputs: 2

Queue
Queue is a first-in, first-out (FIFO) data structure. Java provides several implementations like LinkedList and PriorityQueue.Eg:
import java.util.LinkedList;
import java.util.Queue;

Queue<String> queue = new LinkedList<>();
queue.add("Alice");
queue.add("Bob");
System.out.println(queue.remove());  // Outputs: Alice

PriorityQueue
PriorityQueue is a special type of queue where elements are ordered based on their natural ordering or a custom comparator.Eg:
import java.util.PriorityQueue;

PriorityQueue<Integer> pq = new PriorityQueue<>();
pq.add(5);
pq.add(1);
pq.add(3);
System.out.println(pq.poll());  // Outputs: 1 (the smallest element)

TreeMap
TreeMap is a Red-Black tree-based implementation of the NavigableMap interface. It stores key-value pairs in sorted order.Eg:
import java.util.TreeMap;

TreeMap<String, Integer> sortedMap = new TreeMap<>();
sortedMap.put("Bob", 30);
sortedMap.put("Alice", 25);
System.out.println(sortedMap.firstKey());  // Outputs: Alice

TreeSet
TreeSet implements the NavigableSet interface and is backed by a TreeMap. It stores unique elements in sorted order.Eg:
import java.util.TreeSet;

TreeSet<String> sortedSet = new TreeSet<>();
sortedSet.add("Bob");
sortedSet.add("Alice");
System.out.println(sortedSet.first());  // Outputs: Alice



Functional Interfaces
Java's Functional Interfaces
An interface having just one abstract method is called a functional interface. Method references, anonymous classes, or lambda expressions can be used to implement these interfaces.

Typical Functional Interfaces

Runnable: Denotes an executable task.
A callable task is one that yields a result.
Comparator: A tool for contrasting two items.
Function, Predicate, Supplier, Consumer: A group of functions that are represented by the java.util.function package.

Intermediate operations- Operations that return a resulting stream.

Streams-
A stream can be thought of as an array or collection of things on a conveyor belt. Unlike collections, which hoard items, it allows you to make changes to the data without affecting the original source. To carry out these tactics, you can find some useful tools in the java.util.stream package.

The stream API has parallel muscle flexing. In order to handle the stream items simultaneously, it will bring in several threads. Just be aware that the output will no longer be in a predetermined order; rather, it will behave more erratically, so each time you execute the code, expect some disruption.
To put it briefly, the stream API is a reliable method for shaping data.


Exception Handling in Java
Exception handling in Java is a mechanism to handle runtime errors, allowing the program to continue executing. This is done using try, catch, finally, and throw blocks.Eg:
try {
    // Code that may throw an exception
} catch (ExceptionType1 e1) {
    // Handling exception of type ExceptionType1
} catch (ExceptionType2 e2) {
    // Handling exception of type ExceptionType2
} finally {
    // Code that will always execute, regardless of an exception
}


Stack Trace and Exception Messages:
Stack Trace: A stack trace provides detailed information about the sequence of method calls that led to the exception. It helps in debugging by showing the exact point in the code where the exception occurred.Eg:
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    e.printStackTrace();  // Outputs the stack trace to the console
}

Exception Messages: Exception messages provide information about the error. They can be accessed using the getMessage() method.Eg:
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println(e.getMessage());  // Outputs: / by zero
}

Handling Multiple Exceptions
Java allows handling multiple exceptions either by using multiple catch blocks or by catching multiple exceptions in a single catch block using the multi-catch feature introduced in Java 7.Eg:
Multi-Catch Blocks:
try {
    // Code that may throw multiple exceptions
} catch (IOException e) {
    // Handle IOException
} catch (SQLException e) {
    // Handle SQLException
}

Multi-Catch block:
try {
    // Code that may throw multiple exceptions
} catch (IOException | SQLException e) {
    // Handle both IOException and SQLException
    System.out.println(e.getMessage());
}

