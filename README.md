JavaPrepTheory

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

Unchecked Exceptions (Runtime Exceptions):
Unchecked exceptions are not checked at compile-time; hence, they do not require being handled explicitly using try-catch or declared using throws. These exceptions usually occur due to programming errors and can be prevented by writing robust code. Some common unchecked exceptions include:
NullPointerException: Occurs when a method tries to access a member of an object that is null.
ArrayIndexOutOfBoundsException: Thrown when an invalid index is used for accessing an array.
ArithmeticException: This exception occurs when an arithmetic operation encounters an exceptional condition (e.g., division by zero).


Inheritance: Inheritance  allows a class (subclass) to inherit fields and methods from another class (superclass). Subclasses can extend the functionality of their superclass and add their own unique features.

This vs Super
This is to reference variables, methods in same class, super is reference to a super class
Overriding: Method overriding  occurs when a subclass provides a specific implementation of a method that is already defined in its superclass
Dynamic Method Dispatch 

When a super class reference holding the object of sub class and overridden method is called then method of sub class will be called. It is useful for achieving Runtime Polymorphism.

Polymorphism: polymorphism means one name different actions. Polymorphism is achieved using method overriding and overloading.. Polymorphism promotes code reuse, enables flexibility and extensibility in code design 
Overloading: Method overloading  occurs when multiple methods in the same class have the same name but different parameter lists. Method overriding is used for runtime polymorphism
Overriding: Redefining the method of the Super Class in the Sub Class. Method overriding is achieved in Inheritance. In method overriding signature is same. Method overriding is used for runtime polymorphism
multiprogramming
Running more than one program that is running multiple programs on a single machine or a computer
						
Multi-Tasking 	
Single user runs multiple tasks simultaneously	

Multi threading
Different tasks going  	on under single app

Eg; on browser video playing, ads on the side, comments 		

Life Cycle of a Thread 

A thread  at any point of time exists in any one of the following states. A thread lies only in one of the shown states at any instant:
New State
Runnable State
Blocked State
Waiting State
Timed Waiting State
Terminated State

Priorities in threads is a concept where each thread is having a priority which in layman’s language one can say every object is having priority here which is represented by numbers ranging from 1 to 10

Whenever we create a thread , it always has some priority assigned to it. Priority can either be given by JVM while creating the thread or it can be given by the programmer explicitly. 


Thread Class  
A thread is a program that starts with a method() frequently used in this class only known as the start() method. This method looks out for the run() method which is also a method of this class and begins executing the body of the run() method. 

Note: Every class that is used as thread must implement Runnable interface and over ride it’s run method.
	
	Thread Lifecycle:
Threads  have a lifecycle consisting of various states, including New, Runnable, Blocked, Waiting, Timed Waiting, and Terminated.
The start() method is used to transition a thread from the New state to the Runnable state, initiating its execution.
Once started, a thread executes its run() method and may transition to other states based on various conditions, such as synchronization or waiting for I/O operations.
Thread Methods:
The Thread class provides methods for managing and controlling threads, such as start() to start a thread, sleep() to pause the execution of a thread for a specified period, join() to wait for a thread to complete its execution, and interrupt() to interrupt a thread's execution.
Other methods include getName() and setName() to get and set the name of a thread, isAlive() to check if a thread is alive, and isDaemon() and setDaemon() to check and set a thread's daemon status.

Daemon threads are dependent threads so if  main method is terminating then daemon also terminates making the thread above not print anything
Join
//Now even though daemon terminates, Instead of terminate Join will keep it waiting till the other thread is done
		sleep
		//to make the thread delay for some time, done in milliseconds
interrupt
//after the first print when the thread was sleeping for 1000 milliseconds it was interrupted/woken up by interrupt() to continue its execution
yield();
// A hint to the scheduler that the current thread is willing to yield its current use of a processor

Thread 	:
Synchronization is used to make sure by some synchronization method that only one thread can access the resource at a given point in time. 

Critical Section, Race Condition, and Mutual Exclusion: These terms are closely related and are fundamental concepts in concurrent programming. A critical section is a part of the code that accesses shared resources and must be executed atomically to prevent race conditions, where multiple threads may access shared resources concurrently and lead to inconsistent behavior. Mutual exclusion mechanisms, such as locks (including mutexes) or semaphores, are used to ensure that only one thread can access a critical section at a time, thus preventing race conditions.
Locks, Mutex (Mutual Exclusion), Semaphore, and Condition Variable: These are synchronization primitives used to coordinate access to shared resources and manage the execution of threads in concurrent systems. Locks, mutexes, and semaphores provide mechanisms for mutual exclusion, while condition variables allow threads to wait for specific conditions before proceeding. These mechanisms are often used together to implement complex synchronization patterns.

Java provides synchronization mechanisms such as synchronized blocks and methods, as well as wait() and notify() methods, to ensure thread safety and prevent race conditions.

monitor
		 	 	 	
A monitor is essentially a module that encapsulates a shared resource and provides access to that resource through a set of procedures. The procedures provided by a monitor ensure that only one process can access the shared resource at any given time, and that processes waiting for the resource are suspended until it becomes available.


Generics 

allows us to define classes, interfaces, and methods with type parameters. This enables you to create reusable code that can work with different data types while providing compile-time type safety.

Collection

Any group of individual objects which are represented as a single unit is known as collections.
 Eg: List of objects of Students, means his roll no, name, etc



 ArrayList

ArrayList provides us with dynamic arrays . The size of an ArrayList is increased automatically if the collection grows or shrinks if the objects are removed from the collection.

 LinkedList

 LinkedList is a linear data structure where elements are stored as individual nodes, each containing a reference to the next node in the sequence. 

ArrayDeque

It is a data structure that is a resizable array-based double-ended queue implementation. 

Priority queue

It is a data structure, in which elements are inserted and deleted based on the priority

Hashing

It is a technique to efficiently store and retrieve data in a data structure

HashSet

A `HashSet` is a collection that stores unique elements in an unordered manner, using a hash table-based implementation.

TreeSet

A `TreeSet` is a sorted collection that does not allow duplicate elements. 

Comparable interface

The Comparable interface is used to define a natural ordering for objects of a class.

TreeMap

A TreeMap is a sorted map implementation that stores key-value pairs

HashMap

 A HashMap​​ is a data structure that stores key-value pairs in a collection uses hashing 

​​LinkedHashMap

is a variation of the HashMap class that maintains a predictable iteration order of its entries based on the order in which they were inserted. 

LinkedHashSet

This data structure provides predictable iteration order, making it useful when you need both uniqueness and the preservation of the order in which elements were inserted.


						
FunctionalInterface

It is an interface that contains exactly one abstract method		

It enables the use of lambda expressions to provide implementations for the abstract method.	

Eg: Runnable Interface, comparable Interface,  		 								

Functional Interfaces are categorized into these
producer  -> which will not accept anything, but will give the data  ->  instagram or content feed.
 consumer  -> which will accept the parameter and will not return anything -> data analytics, form submit
predicate  -> which will accept the parameter and will return any parameter -> used in testing


// Implement the functional interface using a lambda expression
MyFunctionalInterface func = () -> System.out.println("My method implementation");


// Use a predefined functional interface (Supplier) with a lambda expression to generate a random number
Supplier<Double> randomNumber = () -> Math.random();

// Use a predefined functional interface (Consumer) with a lambda expression to print a string in uppercase
Consumer<String> printUpperCase = str -> System.out.println(str.toUpperCase());

Lambda expressions 
are used for developing anonymous expressions or nameless methods or functions.

Lambda expressions are defined with the help of interfaces.
Return keyword may not used in case of lambda expression.

Syntax

parameter -> expression
(parameter1, parameter2) -> expression
(parameter1, parameter2) -> { code block }

Using lambda with functional interfaces like Comparator:

Comparator<String> comparator = (String s1, String s2) -> s1.compareTo(s2);

Using lambda with functional interfaces like Runnable:

Runnable task = () -> System.out.println("Executing task");

Using lambda with functional interfaces and method references:

List<String> names = Arrays.asList("Alice", "Bob", "Charlie");
names.forEach(System.out::println);

Using lambda with conditional expressions:

IntPredicate greaterThanTen = x -> x > 10;

Using lambda with streams:

 If the lambda expression needs to return a value, then the code block should have a return statement.

stream 
is a sequence of objects that supports various methods that can be pipelined to produce the desired result.	
		
The features of Java stream are –
A stream is not a data structure instead it takes input from the Collections, Arrays, or I/O channels.

Streams don’t change the original data structure, they only provide the result as per the pipelined methods.

Each intermediate operation is lazily executed and returns a stream as a result, hence various intermediate operations can be pipelined. Terminal operations mark the end of the stream and return the result.

Benefits of using Stream:
No Storage
Pipeline of Functions
Lazy Evaluation is the concept in Java Streams where computation on the source data is only performed when the terminal operation is initiated, and source elements are consumed only as needed. It is called lazy because intermediate operations are not evaluated unless a terminal operation is invoked.
Can be infinite
Can be parallelized
Can be created from collections, arrays, Files Lines, and Methods in Stream, IntStream, etc.

1. Readable, Short and Efficient code:-

Every code starts with a source, followed by intermediate operations and terminal operation. Each intermediate operation is lazily executed and returns a stream as a result, hence various intermediate operations can be pipelined such as filter(), sort(), distinct() etc. Terminal operations mark the end of the stream and return the result such as sum(), average() etc. Thus it is readable, clean, and efficient.

2. Works great with Lambda Expressions and Method References:-

 Stream functions mainly takes action as an argument. These functions can take lambda expressions multiple times. Therefore during a pass-through, a lambda expression can pass both functions and method references. Together these provide a concise way of writing code.

3. Streams can be parallelised:-

 The streams provide options like parallel() to convert the sequential stream to a parallel stream.

4. Streams don't change the original structure:-

Streams don’t change the original data structure, they only provide the result as per the pipelined methods.

5. In Intermediate operations:- 

Each intermediate operation is lazily executed and transforming a stream into another stream, hence various intermediate operations can be pipelined. 


map: The map method is used to returns a stream consisting of the results of applying the given function to the elements of this stream. List number = Arrays.asList(2,3,4,5); List square = number.stream().map(x->x*x).collect(Collectors.toList());
filter: The filter method is used to select elements as per the Predicate passed as argument. List names = Arrays.asList("Reflection","Collection","Stream"); List result = names.stream().filter(s->s.startsWith("S")).collect(Collectors.toList());
sorted: The sorted method is used to sort the stream. List names = Arrays.asList("Reflection","Collection","Stream"); List result = names.stream().sorted().collect(Collectors.toList());


Terminal Operations
Terminal operations mark the end of the stream and return the result. Terminal Operations are the operations that on execution return a final result as an absolute value.

collect: The collect method is used to return the result of the intermediate operations performed on the stream. List number = Arrays.asList(2,3,4,5,3); Set square = number.stream().map(x->x*x).collect(Collectors.toSet());
forEach: The forEach method is used to iterate through every element of the stream. List number = Arrays.asList(2,3,4,5); number.stream().map(x->x*x).forEach(y->System.out.println(y));
reduce: The reduce method is used to reduce the elements of a stream to a single value. The reduce method takes a BinaryOperator as a parameter. List number = Arrays.asList(2,3,4,5); int even = number.stream().filter(x->x%2==0).reduce(0,(ans,i)-> ans+i);


filter(): The filter method is used to select elements as per the Predicate passed as an argument.
forEach(): This is a terminal operation. The forEach method is used to iterate through every element of the stream.
min(): This is a terminal operation. Used to find the minimum element in a stream.
max(): This is a terminal operation. Used to find the maximum element in a stream.
skip(): Used to skip the number of elements in a stream.
findFirst(): This is a terminal operation. Used to find the first element of the stream.
count(): This is a terminal operation. Used to count elements in a current stream.
distinct(): It is an intermediate operation. It returns the stream with distinct elements present in the current stream.
sorted(): It is an intermediate operation. It takes a stream and returns the sorted version of the stream.
reduce(): This is a terminal operation. Used to concatenate all the strings or add the elements.
collect(): This is a terminal operation. It Converts the stream into a collection.

sum(): This is a terminal operation. Used to find the sum of a stream.
average(): This is a terminal operation. Used to find the average of a stream.
boxed(): This takes a primitive type of stream and converts them into a non-primitive stream of wrapper class.

Arrays.stream(arrayName): It's a static method in the Arrays class to convert an array into a stream 

wherever the concept of the collection is applicable, stream concept can be applied there. 

 What is a Pipeline?
A Stream Pipeline is a concept of chaining operations together Terminal Operations and Intermediate Operations. A Pipeline contains a stream source, which is further followed by zero or more intermediate operations, and a terminal operation.

 
	List<String> names = Arrays.asList("Alice", "Bob", "Charlie");

        // Print each element in the list using streams and forEach
        names.stream().forEach(System.out::println);

        // Filter the list to get only names starting with 'A' using streams and filter
        List<String> filteredNames = names.stream().filter(name -> name.startsWith("A")).collect(Collectors.toList());
        System.out.println("Filtered names starting with 'A': " + filteredNames);

       Maven: Java build automation tool for managing dependencies and project builds.




Maven: Java build automation tool for automating project build processes and managing project dependencies. It manages project dependencies providing a uniform build system. 

Why Maven?

It simplifies Java development by automating project build processes and managing project dependencies, leading to faster and more efficient software development. 

maven plugin is a collection of one or more goals, when you created the project and built it the generate goal from the archetype plugin and the install goal from the install
