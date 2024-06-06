# Java-
Java is an object-oriented, high-level programming language created by Sun Microsystems, which Oracle Corporation eventually purchased. Java is built with the following fundamental ideas and characteristics:
Important Concepts of Java Object-Oriented: Java employs an object-oriented programming paradigm, which groups software architecture using objects and classes. Important ideas are abstraction, encapsulation, polymorphism, and inheritance.

Platform-Independent: Java programs are translated into bytecode, which is executable on any hardware that has a Java Virtual Machine installed (JVM). One of Java's biggest benefits is its "write once, run anywhere" flexibility.

Robust and Secure: Java places a high emphasis on memory management, runtime checking, and early error checking. Its robustness is enhanced by features like type checking, exception handling, and garbage collection. Furthermore, Java includes built-in security capabilities such as access control definitions in a security manager and bytecode verification.

Multithreaded: Java has built-in support for many threads, which makes it possible to create incredibly responsive and interactive programs.

Distributed: With a large number of libraries that make dealing with TCP/IP protocols like HTTP and FTP easier, Java is built to handle distributed computing. Methods that operate on remote objects can be invoked using the Remote Method Invocation (RMI) framework.

High Performance: Despite being an interpreted language, Java programs execute almost as quickly as native C or C++ programs thanks to innovations like Just-In-Time (JIT) compilers and performance optimization strategies.

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
