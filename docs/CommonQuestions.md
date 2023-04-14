# Common Java Interview Questions
[source: Simplilearn](https://www.youtube.com/watch?v=-rw8iIsAF5I)

## Sections
### Level One
### Level Two
---

# Level One - Beginner

1. What is the JIT?

JIT is an abbriveation of *Just-In-Time* complier which increases the effciency of the interpreter by compiling the `bytecode` at runtime to `machine code`. This helps raise the speed of code execution.

2. What is a ClassLoader?

ClassLoader in Java is a subsystem of the JVM ( Java Virtual Machine ) dedicated to loading class files when a program is executed. Examples of ClassLoaders in Java are the BootStrap, Extension, and Application ClassLoaders.

3. What are the memory allocations available in Java?

Java has several types of memory allocation types, but the five major ones are:

    1. Class Memory
    2. Heap Memory
    3. Stack Memory
    4. Program Counter Memory
    5. Native Method Stack Memory

4. Will the program run if I write it as `static public void main`?

Yes! Java does not have any specific rule for the order of specifiers. So both `public static void main` and `static public void main` are valid.

5. What is the default value stored in *local variables*?

When declared in languages such as `C` or `C++` the default value is a *garbage value* unless otherwise initialized as a value. In `Java`, neither the *local variables* nor any *primative types* and *Object references* have any sort of default value assigned to them.

6. What is the output of the following code segment?

```java
public class ExampleClass
{
    public static void main(String args[])
    {
      System.out.println("This is the area of a square with side length of 5cm: " + (5 * 5) + "cm^2." );
      System.out.println(100 + 100 + " addition of two numbers before the string.");
      System.out.println("Addition of two numbers after the string " + 100 + 100);
    }
}
```

The output would be:
```
This is the area of a square with side length 5cm: 25cm^2.
200 addition of two numbers before the string.
Addition of two numbers after the string 100100 
```

7. What is an Association?

An *association* can be defined as a relationship that has __no ownership over another__. For example, a `Person` can be associated with multiple `Banks` and a `Bank` can be associated with multiple `Person`s, but neither can own either.

8. What is a Copy Constructor?

A *copy constructor* in Java is a constructor that initalizes an object through another object in the same class.

Example
```java
class Person {
    private String name;
    private int age;
 
    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
 
    public Person(Person another) {
        this(another.name, another.age);
    }
    // ...
}
```
[source: geeksforgeeks](https://www.geeksforgeeks.org/copy-constructor-in-java/)

9. What is a *Marker Interface*?

A marker interface is an empty interface such as `Serializable` and `Cloneable`. It does not contain any variables or methods within it, it provides runtime information to the complier and JVM about objects. It is also often called a _tagging interface_.

10. What is Object Cloning?

It is the ability to recreate an object completely from an existing object and is used with the `.clone()` method that is provided by Java and offers the same functionality as the original.

11. Why is Java not completely object orientated?

Java is not considered as a 100% object-oriented language because it still uses of more than eight primative data types.

12. Define wrapper classes.

Wrapper classes allow you to delcare primative datatypes as objects or *reference* types.

13. Define a singleton class.

When a class constructor is set to `private`, then that particular class can only generate one single object.

14. Define a Java Package.

A package is a collection of classes and interfaces along with an neccesary libraries and JAR files. This assists in code-reusability as multiple projects can all reference a single package without needing its own implementation. For example, the `Math` package.

15. Can you implement pointers in Java?

Java Virtual Machine takes care of all memory management implicity, therefore you cannot use pointers.

16. Differentiate between instance and local variables.

Instance Variables - These are delcared inside a class and the scope is limited to only that specific object.

Local Variables - These can be anywhere inside a method or specific block of code and the scope is limited to the code block where the variable has been declared.

[More Details](https://www.geeksforgeeks.org/variables-in-java/)

17. What is a Java String Pool?

A collection of strings in heap memory. The JVM checks for the presence of any new String objects you attempt to declare in the heap and if a match is found, both reference the same String variable instead of creating a new object.

18. What is an Exception?

An exception is an unexpected event that can disrupt the flow of a program. These exceptions are handled through using Exception Handling.

19. What is the `final` keyword in Java?

If a variable is delcared as `final`, that means the value it is assigned will be constant and cannot change throughout the execution of the program.

20. What happens when `main()` isn't delcared as static?

When the main method is not declared as static, the program may compile correctly, but it will end up with a serious ambiguity and throw a `runtime error` that reads `NoSuchMethodError`.

# Level Two - Intermediate

1. What is JDK and what variants of the JDK exist?

JDK is an abbreviation for _Java Development Kit_ and is used in combination of JRE and Developer tools used for designing Java Applications and Applets. Oracle has the following variants:

    1. JDK Standard Edition
    2. JDK Enterprise Edition
    3. JDK Micro Edition

2. What is a Brief Access Specifier and their Types?

Access Specifiers are predefined keywords used to help the JVM with understanding the scope of a variable, method, and a class. There are four access specifiers:
    
    1. Public Access Specifier
    2. Private Access Specifier
    3. Protected Access Specifier
    4. Default Access Specifier

3. Can a constructor return a value?

Yes, a constructor can return a value however it is returning the current _instance_ of the class _implicitly_. You cannot make a constructor return a value _specifically_.

4. Explain the `this` keyword.

`this` is a special keyword that is designated as a reference keyword. It is referring to current class properties such as the _method_, _instance_, _variable_, and _constructors_.

5. Explain the `super` keyword.

`super` is a special keyword the is designated as a reference keyword and is used to reference the immediate parent class object.

6. Explain Method Overloading.

The process of creating multiple method signatures using one method name is called _method overloading_ and is created in the following steps.
    
    1. Varying the number of arguments.
    2. Varying the return type of a method.

7. Can we overload static methods?

No. We can not overload static methods.

8. Define Late Binding.

Binding is a process of unifying the method call with the method's code segment. Late binding occurs when the method's code segment is unknown until the method is called at runtime.

9. Define Dynamic Method Dispatch.

Dynamic method dispatch is a process where the method call is executed during runtime. The overridden method is called through a reference variable of `super` class. This process is also known as _Run-Time Polymorphism_.

10. Why is the delete function faster in a linked list than in an array?

An array is a complete segment block in memory, where as a linked list can be dispersed throughout available memory. This is because instead of having everything stored in _one collection_ in an array, a linked list will just reference the next value.

11. Briefly describe the lifecycle of a thread.

// TODO: FINISH SECTION - JF Apr. 14, 2023
https://www.youtube.com/watch?v=-rw8iIsAF5I