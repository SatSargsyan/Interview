# Iterview

### What is the difference between Interface and Abstract Class?

Theoretically their are some differences between Abstract Class and Interface which are listed below:

A class can implement any number of interfaces but a subclass can at most use only one abstract class.
An abstract class can have non-abstract methods (concrete methods) while in case of interface all the methods has to be abstract.
An abstract class can declare or use any variables while an interface is not allowed to do so.
In an abstract class all data member or functions are private by default while in interface all are public, we can’t change them manually.
In an abstract class we need to use abstract keyword to declare abstract methods while in an interface we don’t need to use that.
An abstract class can’t be used for multiple inheritance while interface can be used as multiple inheritance.
An abstract class use constructor while in an interface we don’t have any type of constructor.
To know more about the difference between Abstract Class and Interface go to the following link:


### What is enum in C#?


An enum is a value type with a set of related named constants often referred to as an enumerator list. The enum keyword is used to declare an enumeration. It is a primitive data type, which is user defined.

An enum type can be an integer (float, int, byte, double etc.). But if you used beside int it has to be cast.

An enum is used to create numeric constants in .NET framework. All the members of enum are of enum type. Their must be a numeric value for each enum type.

The default underlying type of the enumeration element is int. By default, the first enumerator has the value 0, and the value of each successive enumerator is increased by 1.
enum Dow {Sat, Sun, Mon, Tue, Wed, Thu, Fri};  
Some points about enum
Enums are enumerated data type in c#.
Enums are not for end-user, they are meant for developers.
Enums are strongly typed constant. They are strongly typed, i.e. an enum of one type may not be implicitly assigned to an enum of another type even though the underlying value of their members are the same.
Enumerations (enums) make your code much more readable and understandable.
Enum values are fixed. Enum can be displayed as a string and processed as an integer.
The default type is int, and the approved types are byte, sbyte, short, ushort, uint, long, and ulong.
Every enum type automatically derives from System.Enum and thus we can use System.Enum methods on enums.
Enums are value types and are created on the stack and not on the heap.
For more details follow the link:


### What is the difference between “continue” and “break” statements in C#?


Using break statement, you can 'jump out of a loop' whereas by using continue statement, you can 'jump over one iteration' and then resume your loop execution.
```C#
Eg. Break Statement 
using System;  
using System.Collections;  
using System.Linq;  
using System.Text;  
  
namespace break_example {  
    {  
        Class brk_stmt {  
            public static void main(String[] args) {  
                for (int i = 0; i <= 5; i++) {  
                    if (i == 4) {  
                        continue;  
                    }  
                    Console.ReadLine(“The number is” + i);  
  
                }  
            }  
        }  
  
    }  
}  
Output 

The number is 0; 
The number is 1; 
The number is 2; 
The number is 3;

Eg.Continue Statement

using System;  
using System.Collections;  
using System.Linq;  
using System.Text;  
  
namespace continue_example  
{  
    Class cntnu_stmt   
    {  
        public static void main(String[]   
        {  
            for (int i = 0; i <= 5; i++)   
            {  
                if (i == 4)   
                {  
                    continue;  
                }  
                Console.ReadLine(“The number  
                  
            }  
        }  
    }  
      
}  
  
          
Output

The number is 1;
The number is 2;
The number is 3;
The number is 5; 
```

### What is the difference between constant and read only in c#?


Constant (const) and Readonly (readonly) both looks like same as per the uses but they have some differences: 

Constant is known as “const” keyword in C# which is also known immutable values which are known at compile time and do not change their values at run time like in any function or constructor for the life of application till the application is running.

Readonly is known as “readonly” keyword in C# which is also known immutable values and are known at compile and run time and do not change their values at run time like in any function for the life of application till the application is running. You can assay their value by constructor when we call constructor with “new” keyword.
```C#

We have a Test Class in which we have two variables one is readonly and another is constant.
class Test {  
    readonly int read = 10;  
    const int cons = 10;  
    public Test() {  
        read = 100;  
        cons = 100;  
    }  
    public void Check() {  
        Console.WriteLine("Read only : {0}", read);  
        Console.WriteLine("const : {0}", cons);  
    }  
}  
```
Here I was trying to change the value of both the variables in constructor but when I am trying to change the constant it gives an error to change their value in that block which have to call at run time.



So finally remove that line of code from class and call this Check() function like the following code snippet:
```C#
class Program {  
    static void Main(string[] args) {  
        Test obj = new Test();  
        obj.Check();  
        Console.ReadLine();  
    }  
}  
class Test {  
    readonly int read = 10;  
    const int cons = 10;  
    public Test() {  
        read = 100;  
    }  
    public void Check() {  
        Console.WriteLine("Read only : {0}", read);  
        Console.WriteLine("const : {0}", cons);  
    }  
}
```
Output:




### Can “this” be used within a static method?


We can't use this in static method because keyword 'this' returns a reference to the current instance of the class containing it. Static methods (or any static member) do not belong to a particular instance. They exist without creating an instance of the class and call with the name of a class not by instance so we can’t use this keyword in the body of static Methods, but in case of Extension Methods we can use it the functions parameters. Let’s have a look on “this” keyword.

The "this" keyword is a special type of reference variable that is implicitly defined within each constructor and non-static method as a first parameter of the type class in which it is defined. For example, consider the following class written in C#.

For more follow this link:

"this" Keyword in C#
this keyword in C#

###Define Property in C#.net?


Properties are members that provide a flexible mechanism to read, write or compute the values of private fields, in other words by the property we can access private fields. In other words we can say that a property is a return type function/method with one parameter or without a parameter. These are always public data members. It uses methods to access and assign values to private fields called accessors.

Now question is what are accessors?

The get and set portions or blocks of a property are called accessors. These are useful to restrict the accessibility of a property, the set accessor specifies that we can assign a value to a private field in a property and without the set accessor property it is like a read-only field. By the get accessor we can access the value of the private field, in other words it returns a single value. A Get accessor specifies that we can access the value of a field publically.

We have the three types of properties 
Read/Write.
ReadOnly.
WriteOnly


### What is extension method in c# and how to use them?

Extension methods enable you to add methods to existing types without creating a new derived type, recompiling, or otherwise modifying the original type. An extension method is a special kind of static method, but they are called as if they were instance methods on the extended type.

How to use extension methods?

An extension method is a static method of a static class, where the "this" modifier is applied to the first parameter. The type of the first parameter will be the type that is extended.

Extension methods are only in scope when you explicitly import the namespace into your source code with a using directive.

Like: suppose we have a class like bellow:
public class Class1 {  
    public string Display() {  
        return ("I m in Display");  
    }  
  
    public string Print() {  
        return ("I m in Print");  
    }  
}  
Now we need to extend the definition of this class so m going to create a static class to create an extinction method like:
public static class XX {  
    public static void NewMethod(this Class1 ob) {  
        Console.WriteLine("Hello I m extended method");  
    }  
}  
Here I just create a method that name is NewMethod with a parameter using this to define which type of data I need to be extend, now let’s see how to use this function.



class Program {  
    static void Main(string[] args) {  
        Class1 ob = new Class1();  
        ob.Display();  
        ob.Print();  
        ob.NewMethod();  
        Console.ReadKey();  
    }  
}  
Output will be: 



For more details you can read this article:
Extension Methods in C# 
Extension Method In C#
Or watch my video article link

Extension Methods in C#
14. What is the difference between dispose and finalize methods in c#?

Answer: finalizer and dispose both are used for same task like to free unmanaged resources but have some differences see. 

Finalize:

Finalize used to free unmanaged resources those are not in use like files, database connections in application domain and more, held by an object before that object is destroyed.
In the Internal process it is called by Garbage Collector and can’t called manual by user code or any service.
Finalize belongs to System.Object class.
Implement it when you have unmanaged resources in your code, and make sure that these resources are freed when the Garbage collection happens.
Dispose:

Dispose is also used to free unmanaged resources those are not in use like files, database connections in Application domain at any time.
Dispose explicitly it is called by manual user code.
If we need to dispose method so must implement that class by IDisposable interface.
It belongs to IDisposable interface.
Implement this when you are writing a custom class that will be used by other users.
For more details follow this link:


### What is the difference between string and StringBuilder in c#?

StringBuilder and string both use to store string value but both have many differences on the bases of instance creation and also for performance:

String: 

String is an immutable object. Immutable like when we create string object in code so we cannot modify or change that object in any operations like insert new value, replace or append any value with existing value in string object, when we have to do some operations to change string simply it will dispose the old value of string object and it will create new instance in memory for hold the new value in string object like:



Note:

It’s an immutable object that hold string value.

Performance wise string is slow because its’ create a new instance to override or change the previous value.

String belongs to System namespace.
StringBuilder:

System.Text.Stringbuilder is mutable object which also hold the string value, mutable means once we create a System.Text.Stringbuilder object we can use this object for any operation like insert value in existing string with insert functions also replace or append without creating new instance of System.Text.Stringbuilder for every time so it’s use the previous object so it’s work fast as compare than System.String. Let’s have an example to understand System.Text.Stringbuilder like:



Note:

StringBuilder is a mutable object.
Performance wise StringBuilder is very fast because it will use same instance of StringBuilder object to perform any operation like insert value in existing string.
StringBuilder belongs to System.Text.Stringbuilder namespace.
For More details read this article by following link:

### What is delegates in C# and uses of delegates?

C# delegates are same as pointers to functions, in C or C++. A delegate Object is a reference type variable that use to holds the reference to a method. The reference can be changed at runtime which is hold by an object of delegate, a delegate object can hold many functions reference which is also known as Invocation List that refers functions in a sequence FIFO, we can new functions ref in this list at run time by += operator and can remove by -= operator. 

Delegates are especially used for implementing events and the call-back methods. All delegates are implicitly derived from the System.Delegate class.

Let’s see how to use Delegate with Example:



18. What are partial classes?

Answer: 

A partial class is only use to splits the definition of a class in two or more classes in a same source code file or more than one source files. You can create a class definition in multiple files but it will be compiled as one class at run time and also when you’ll create an instance of this class so you can access all the methods from all source file with a same object.

Partial Classes can be create in the same namespace it’s doesn’t allowed to create a partial class in different namespace. So use “partial” keyword with all the class name which you want to bind together with the same name of class in same namespace, let’s have an example:


### What is boxing and unboxing?


Boxing and Unboxing both using for type converting but have some difference:

Boxing:

Boxing is the process of converting a value type data type to the object or to any interface data type which is implemented by this value type. When the CLR boxes a value means when CLR converting a value type to Object Type, it wraps the value inside a System.Object and stores it on the heap area in application domain. 

Example:



Unboxing:

Unboxing is also a process which is use to extracts the value type from the object or any implemented interface type. Boxing may be done implicit but unboxing have to be explicit by code. 

Example:



The concept of boxing and unboxing underlies the C# unified view of the type system in which a value of any type can be treated as an object.

### What is IEnumerable<> in c#? 

IEnumerable is the parent interface for all non-generic collections in System.Collections namespace like ArrayList, HastTable etc. that can be enumerated. For the generic version of this interface as IEnumerable`<T>` which a parent interface of all generic collections class in System.Collections.Generic namespace like List`<>` and more. 

In System.Collections.Generic.IEnumerable`<T>` have only a single method which is GetEnumerator() that returns an IEnumerator. IEnumerator provides the power to iterate through the collection by exposing a Current property and Move Next and Reset methods, if we doesn’t have this interface as a parent so we can’t use iteration by foreach loop or can’t use that class object in our LINQ query.



### What is difference between late binding and early binding in c#?

Early Binding and Late Binding concepts belongs to polymorphism so let’s see first about polymorphism:

Polymorphism is an ability to take more than one form of a function means with a same name we can write multiple functions code in a same class or any derived class.

Polymorphism we have 2 different types to achieve that:

Compile Time also known as Early Binding or Overloading.
Run Time also known as Late Binding or Overriding.
Compile Time Polymorphism or Early Binding:

In Compile time polymorphism or Early Binding we will use multiple methods with same name but different type of parameter or may be the number or parameter because of this we can perform different-different tasks with same method name in the same class which is also known as Method overloading.

See how we can do that by the following example:



Run Time Polymorphism or Late Binding:

Run time polymorphism also known as late binding, in Run Time polymorphism or Late Binding we can do use same method names with same signatures means same type or same number of parameters but not in same class because compiler doesn’t allowed that at compile time so we can use in derived class that bind at run time when a child class or derived class object will instantiated that’s way we says that Late Binding. For that we have to create my parent class functions as partial and in driver or child class as override functions with override keyword. 

### What are the differences between IEnumerable and IQueryable?


Before the differences learn what is IEnumerable and IQueryable.

IEnumerable:

Is the parent interface for all non-generic collections in System.Collections namespace like ArrayList, HastTable etc. that can be enumerated. For the generic version of this interface as IEnumerable<T> which a parent interface of all generic collections class in System.Collections.Generic namespace like List<> and more. 

IQueryable:

As per MSDN IQueryable interface is intended for implementation by query providers. It is only supposed to be implemented by providers that also implement IQueryable `<T>`. If the provider does not also implement IQueryable`<T>`, the standard query operators cannot be used on the provider's data source.

The IQueryable interface inherits the IEnumerable interface so that if it represents a query, the results of that query can be enumerated. Enumeration causes the expression tree associated with an IQueryable object to be executed. The definition of "executing an expression tree" is specific to a query provider. For example, it may involve translating the expression tree to an appropriate query language for the underlying data source. Queries that do not return enumerable results are executed when the Execute method is called.


### What happens if the inherited interfaces have conflicting method names?


If we implement multipole interface in the same class with conflict method name so we don’t need to define all or in other words we can say if we have conflict methods in same class so we can’t implement their body independently in the same class coz of same name and same signature so we have to use interface name before method name to remove this method confiscation let’s see an example:

```C#
interface testInterface1 {  
    void Show();  
}  
interface testInterface2 {  
    void Show();  
}  
class Abc: testInterface1,  
testInterface2 {  
  
    void testInterface1.Show() {  
        Console.WriteLine("For testInterface1 !!");  
    }  
    void testInterface2.Show() {  
        Console.WriteLine("For testInterface2 !!");  
    }  
}  
Now see how to use those in a class:
class Program {  
    static void Main(string[] args) {  
        testInterface1 obj1 = new Abc();  
        testInterface1 obj2 = new Abc();  
        obj1.Show();  
        obj2.Show();  
  
        Console.ReadLine();  
    }  
}  
```
Output:



For one more example follow the link:
Inherit Multiple Interfaces and They have Conflicting Method Name
24. What are the Arrays in C#.Net?

Answer: 

Arrays are powerful data structures for solving many programming problems. You saw during the creation of variables of many types that they have one thing in common, they hold information about a single item, for instance an integer, float and string type and so on. So what is the solution if you need to manipulate sets of items? One solution would be to create a variable for each item in the set but again this leads to a different problem. How many variables do you need? 

So in this situation Arrays provide mechanisms that solves problem posed by these questions. An array is a collection of related items, either value or reference type. In C# arrays are immutable such that the number of dimensions and size of the array are fixed. 

Arrays Overview

An array contains zero or more items called elements. An array is an unordered sequence of elements. All the elements in an array are of the same type (unlike fields in a class that can be of different types). The elements of an array accessed using an integer index that always starts from zero. C# supports single-dimensional (vectors), multidimensional and jagged arrays. 

Elements are identified by indexes relative to the beginning of the arrays. An index is also commonly called indices or subscripts and are placed inside the indexing operator ([]). Access to array elements is by their index value that ranges from 0 to (length-1).

Array Properties

The length cannot be changed once created.
Elements are initialized to default values.
Arrays are reference types and are instances of System.Array.
Their number of dimensions or ranks can be determined by the Rank property.
An array length can be determined by the GetLength() method or Length property.
For more detail follow the link:

Overview of Arrays in C#
Doing Arrays - C#
25. What is the Constructor Chaining in C#?

Answer: constructor chaining is a way to connect two or more classes in a relationship as Inheritance, in Constructor Chaining every child class constructor is mapped to parent class Constructor implicitly by base keyword so when you create an instance of child class to it’ll call parent’s class Constructor without it inheritance is not possible.

For more example follow the link:

Constructor Chaining In C#
Constructors In C#
26. What’s the difference between the System.Array.CopyTo() and System.Array.Clone()?

Answer: 

Clone: 

Method creates a shallow copy of an array. A shallow copy of an Array copies only the elements of the Array, whether they are reference types or value types, but it does not copy the objects that the references refer to. The references in the new Array point to the same objects that the references in the original Array point to.

CopyTo:

The Copy static method of the Array class copies a section of an array to another array. The CopyTo method copies all the elements of an array to another one-dimension array. The code listed in Listing 9 copies contents of an integer array to an array of object types. 

To learn about arrays go with following link:

Working with Arrays in C#
27. Can Multiple Catch Blocks executed in c#?

Answer: 

we can use multiple Catches block with every try but when any Exceptions is throw by debugger so every catches match this exception type with their signature and catch the exception by any single catch block so that means we can use multiple catches blocks but only one can executed at once like:
using System;  
class MyClient {  
    public static void Main() {  
        int x = 0;  
        int div = 0;  
        try {  
            div = 100 / x;  
            Console.WriteLine("Not executed line");  
        } catch (DivideByZeroException de) {  
            Console.WriteLine("DivideByZeroException");  
        } catch (Exception ee) {  
            Console.WriteLine("Exception");  
        } finally {  
            Console.WriteLine("Finally Block");  
        }  
        Console.WriteLine("Result is {0}", div);  
    }  
}  
To learn more about Exception Handling following link:
Exception Handling in C#
28. What is Singleton Design Patterns and How to implement in C#?

Answer: 

What is Singleton Design Pattern?

Ensures a class has only one instance and provides a global point of access to it.
A singleton is a class that only allows a single instance of itself to be created, and usually gives simple access to that instance.
Most commonly, singletons don't allow any parameters to be specified when creating the instance, since a second request of an instance with a different parameter could be problematic! (If the same instance should be accessed for all requests with the same parameter then the factory pattern is more appropriate.)
There are various ways to implement the Singleton Pattern in C#. The following are the common characteristics of a Singleton Pattern.

• A single constructor, that is private and parameterless.
• The class is sealed.
• A static variable that holds a reference to the single created instance, if any.
• A public static means of getting the reference to the single created instance, creating one if necessary.
This is the example how to write the code with Singleton:
namespace Singleton {  
    class Program {  
        static void Main(string[] args) {  
            Calculate.Instance.ValueOne = 10.5;  
            Calculate.Instance.ValueTwo = 5.5;  
            Console.WriteLine("Addition : " + Calculate.Instance.Addition());  
            Console.WriteLine("Subtraction : " + Calculate.Instance.Subtraction());  
            Console.WriteLine("Multiplication : " + Calculate.Instance.Multiplication());  
            Console.WriteLine("Division : " + Calculate.Instance.Division());  
  
            Console.WriteLine("\n----------------------\n");  
  
            Calculate.Instance.ValueTwo = 10.5;  
            Console.WriteLine("Addition : " + Calculate.Instance.Addition());  
            Console.WriteLine("Subtraction : " + Calculate.Instance.Subtraction());  
            Console.WriteLine("Multiplication : " + Calculate.Instance.Multiplication());  
            Console.WriteLine("Division : " + Calculate.Instance.Division());  
  
            Console.ReadLine();  
        }  
    }  
  
    public sealed class Calculate {  
        private Calculate() {}  
        private static Calculate instance = null;  
        public static Calculate Instance {  
            get {  
                if (instance == null) {  
                    instance = new Calculate();  
                }  
                return instance;  
            }  
        }  
  
        public double ValueOne {  
            get;  
            set;  
        }  
        public double ValueTwo {  
            get;  
            set;  
        }  
  
        public double Addition() {  
            return ValueOne + ValueTwo;  
        }  
  
        public double Subtraction() {  
            return ValueOne - ValueTwo;  
        }  
  
        public double Multiplication() {  
            return ValueOne * ValueTwo;  
        }  
  
        public double Division() {  
            return ValueOne / ValueTwo;  
        }  
    }  
}  
To read more about Singleton in depth so follow the link:
Singleton Design Pattern in C#
Implementing Singleton Design Patterns
29. Difference between Throw Exception and Throw Clause. 

Answer: 

The basic difference is that the Throw exception overwrites the stack trace and this makes it hard to find the original code line number that has thrown the exception.

Throw basically retains the stack information and adds to the stack information in the exception that it is thrown.

Let us see what it means rather speaking so many words to better understand the differences. I am using a console application to easily test and see how the usage of the two differ in their functionality.
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Text;  
  
namespace TestingThrowExceptions {  
    class Program {  
        public void ExceptionMethod() {  
            throw new Exception("Original Exception occurred in ExceptionMethod");  
  
        }  
  
        static void Main(string[] args) {  
            Program p = new Program();  
            try {  
                p.ExceptionMethod();  
            } catch (Exception ex) {  
  
                throw ex;  
            }  
        }  
    }  
}  
Now run the code by pressing the F5 key of the keyboard and see what happens. It returns an exception and look at the stack trace:

For More Details use following link:
Difference Between Throw Exception and Throw Clause
30. What are Indexer in C# .Net?

Answer: 

Indexer allows classes to be used in more intuitive manner. C# introduces a new concept known as Indexers which are used for treating an object as an array. The indexers are usually known as smart arrays in C#. They are not essential part of object-oriented programming.

An indexer, also called an indexed property, is a class property that allows you to access a member variable of a class using the features of an array.

Defining an indexer allows you to create classes that act like virtual arrays. Instances of that class can be accessed using the [] array access operator.

Creating an Indexer
< modifier > <  
return type > this[argument list] {  
    get {  
        // your get block code  
    }  
  
    set {  
        // your set block code  
    }  
}  
In the above code:

<modifier>

can be private, public, protected or internal.

<return type>

can be any valid C# types.

For more details use following link:
Indexers in C#
INDEXER in C#
31. What is multicast delegate in c#?



<a href=http://www.c-sharpcorner.com/uploadfile/nipuntomar/jit-just-in-time-compiler/>JIT</a>

<a href=http://www.telerik.com/blogs/understanding-net-just-in-time-compilation>.net</a>
