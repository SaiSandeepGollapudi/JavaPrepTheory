# JavaPrepTheory

**Benefits of using Java?
**

Simple 
Structured
Object-oriented
Secure
Portable
Robust
Distributed
Dynamic
open source 
Fast 
powerful
Huge community support
 
 Acronym "S PROF PODS SH"

**Why is Java a platform-independent language
**

When we write Java code, it is compiled into an intermediate form called bytecode rather than machine-specific code. This bytecode is executed by the Java Virtual Machine (JVM), which is platform-specific.  This allows Java programs to run on any device or operating system

**Can Java be said to be the complete object-oriented programming language?
**

Java is often regarded as a complete object-oriented programming language, as it strongly supports fundamental OOP principles like encapsulation, inheritance, and polymorphism(overloading and overriding)However, debates arise due to the inclusion of primitive data types and static methods. Java mitigates this with the concept of "wrapper" classes that encapsulate primitive types in objects, enabling them to participate in the object-oriented paradigm and its class-based structure encourages the creation and utilization of objects.

**Class** 

A class is a blueprint for creating objects. It represents properties and methods that objects will have. It has member variables and member methods.

For example, a Car class may have fields like make, model, and year, and methods like start() and drive().

Object: An object is an instance of a class. It represents a real-world entity and has  (properties) and (methods) defined by its class. For example, if a Car is a class, an object myCar could represent a specific car with its make, model, and year.

 Constructor: It’s a special method used to initialize objects and allocate memory. 

 Notes:
 it is called when an object is created, it can be used to set initial values for object attributes. constructors have the same name as the class. Constructors may accept parameters for initialization.

If a Grandchild class object is created then as we know Grandchild class inherits the Child class constructor and the Child class inherits the Parent class constructor so if the Grandchild object First executes then all the constructors are executed automatically from the parent class and then level by level. 


**Class Name
**
Java Class should always start with an uppercase, and the name of the file should be the same as the class name with .java 

**Rules for naming variables 
**

Variables  should start with a lowercase letter, and cannot contain whitespace

**Static method
**

It is a method that can be accessed without creating an object 
Attributes and methods belong to the class, rather than any object

Notes
Static members can be accessed just by using the class name.
Static methods can access only static members
The public method needs an object to be accessed


**Recursion**

is the technique of making a function call itself.

** Access modifiers:**  It is used to set access to classes, attributes, constructors, method

Classes, we can use public or default 

The public can be accessed by any other class
Default: can be accessed only by classes in the same package, this is used when we don’t specify any modifier

Non-Access Modifiers for classes

Final: class cannot be inherited by another class
Abstract: class cannot be used to create objects

For attributes, methods, constructors

Public and default are the same as for classes
Private: can be accessed within the declared class
Protected: can be accessed in the same package and subclasses  


For attributes and methods

Final: same as class
Static: Attributes and methods belong to the class, rather than any object
Abstract: can only be used in the abstract class and can only be used on methods. The method does not have a body, for eg; abstract void run();


Encapsulation:
Encapsulation refers to integrating (variables) and (methods) into a single unit. It restricts direct access to some internal variables and methods and prevents the accidental modification of data.

Notes
Declare class variables as private
To allow controlled access to these private variables, public getter and setter methods are provided. 
Exposing only the necessary functionality through public methods, while hiding the internal implementation details.
Class variables can be made read-only (if you only use the get method), or write-only (if you only use the set method)

Package
It is used to group related classes, package are 2 types:  built-in ( packages from Java API) and user-defined

Notes
Java API is included in the JDE Java development environment
We can import a single class( along with its attributes and methods) or the whole package 

Abstraction

Data abstraction is the process of hiding complex   details and showing only essential information to the user.

Notes
An abstract class is a class that cannot be instantiated on its own but can contain abstract methods, which are methods without a body.
Abstract classes may also contain concrete methods (methods with a body) along with abstract methods.
Subclasses of an abstract class must either implement all the abstract methods defined in the superclass or be declared abstract themselves.

For Eg: Users interact with bank accounts through a common interface (BankAccount), allowing them to perform operations like depositing and withdrawing funds without needing to know the internal details of each account type.

Interfaces

It defines a contract for classes to follow. Specifying a set of methods that a class implementing the interface must provide.

Notes
An interface can be called an Abstract Class with all abstract methods.
Like abstract classes, interfaces cannot be used to create objects
Interface methods do not have a body - the body is provided by the "implement" class
On implementation of an interface, you must override all of its methods
Interface methods are by default abstract and public
Interface attributes are by default public, static, and final
An interface cannot contain a constructor (as it cannot be used to create objects)

EG; In a banking application, interfaces like `BankAccount` define common operations such as deposit and withdraw, while concrete classes like `SavingsAccount` and CheckingAccount provide specific implementations, ensuring consistent behavior across different account types.

Why And When To Use Interfaces?

Java does ​​not support "multiple inheritance" (a class can only inherit from one superclass). However, it can be achieved with interfaces, because the class can implement multiple interfaces. Note: To implement multiple interfaces, separate them with a comma. 

Difference between Enums and Classes

An enum, just like a class, has attributes and methods. The only difference is that enum constants/variables are public, static, and final (unchangeable - cannot be overridden).

Notes
An enum cannot be used to create objects, and it cannot extend other classes (but it can implement interfaces).

Why And When To Use Enums?
Use enums when you have values that you know aren't going to change, like month days, days, colors, deck of cards, etc.

Error:
Errors are abnormal conditions that cannot be handled by the program and usually result from system failures or resource exhaustion, such as out-of-memory errors or stack overflow errors. 

Exceptions:
An exception is an event that might disrupt the normal flow of the program. But Exception handling handles these situations and prevents program crashes.

try
The try block has a code that may throw exceptions.

catch
The catch block specifies how to handle different types of exceptions. When an exception occurs in the try block, it is transferred to the appropriate catch block to handle the exception.

finally
The finally block is used to execute code that should be run regardless of whether an exception is thrown or caught
Throw:
Throw is used to explicitly throw an exception within a method 
You can throw both built-in exceptions (e.g., NullPointerException, ArithmeticException) and custom exceptions that extend the Exception class or one of its subclasses.

Syntax
throw new NullPointerException("Custom message for NullPointerException");
throw new CustomException("Custom message for CustomException");

throws:
The throws keyword is used in the method signature when a method can potentially throw an exception but does not handle it internally. 

Compile Time:

Compilation detects errors such as syntax errors, type mismatches, and other compile-time errors. These errors prevent the program from being successfully compiled into bytecode.

Runtime:
Runtime refers to the phase during which the compiled Java bytecode is executed by the Java Virtual Machine (JVM).
The program's behavior during runtime includes dynamic memory allocation, object instantiation, method invocation, and exception handling.
Errors that occur during runtime are known as runtime errors or exceptions. These errors occur while the program is running and may be due to logical errors, resource unavailability, input data issues, or unexpected conditions.
Examples of runtime errors include NullPointerException, ArrayIndexOutOfBoundsException, and ArithmeticException.


Checked Exception: 
Exceptions that are checked at compile time. They must be either handled or declared using the throws keyword in the method signature. 
Checked exceptions typically represent recoverable conditions that the program can handle.

Examples include IOException and SQLException. 
IOException: This exception is thrown when an I/O operation fails or is interrupted.
SQLException: It is thrown when there is an error in the database access or SQL operations.
ClassNotFoundException: This exception is thrown when an application tries to load a class by name but the class cannot be found.
FileNotFoundException: Thrown when an attempt to access a file that doesn't exist occurs.




