# Iterview

What is the difference between Interface and Abstract Class?

Answer: 

Theoretically their are some differences between Abstract Class and Interface which are listed below:

A class can implement any number of interfaces but a subclass can at most use only one abstract class.
An abstract class can have non-abstract methods (concrete methods) while in case of interface all the methods has to be abstract.
An abstract class can declare or use any variables while an interface is not allowed to do so.
In an abstract class all data member or functions are private by default while in interface all are public, we can’t change them manually.
In an abstract class we need to use abstract keyword to declare abstract methods while in an interface we don’t need to use that.
An abstract class can’t be used for multiple inheritance while interface can be used as multiple inheritance.
An abstract class use constructor while in an interface we don’t have any type of constructor.
To know more about the difference between Abstract Class and Interface go to the following link:

Abstract Class vs Interface
Explore Interface Vs Abstract Class
7. What is enum in C#?

Answer: 

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

Enums in C#
Enumeration In C#
8. What is the difference between “continue” and “break” statements in C#?

Answer: 

Using break statement, you can 'jump out of a loop' whereas by using continue statement, you can 'jump over one iteration' and then resume your loop execution.

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

For more details follow link:

Difference Between Break Statement and Continue Statement in C#
Break and Continue Statements in C#
9. What is the difference between constant and read only in c#?

Answer: 

Constant (const) and Readonly (readonly) both looks like same as per the uses but they have some differences: 

Constant is known as “const” keyword in C# which is also known immutable values which are known at compile time and do not change their values at run time like in any function or constructor for the life of application till the application is running.

Readonly is known as “readonly” keyword in C# which is also known immutable values and are known at compile and run time and do not change their values at run time like in any function for the life of application till the application is running. You can assay their value by constructor when we call constructor with “new” keyword.

See the example

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
Here I was trying to change the value of both the variables in constructor but when I am trying to change the constant it gives an error to change their value in that block which have to call at run time.



So finally remove that line of code from class and call this Check() function like the following code snippet:
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
Output:



To know more go to the following link:
Difference Between Const, ReadOnly and Static ReadOnly in C#
Constant VS ReadOnly In C#
10. What is the difference between ref and out keywords?

Answer: 

In C Sharp (C#) we can have three types of parameters in a function. The parameters can be in parameter (which is not returned back to the caller of the function), out parameter and ref parameter. We have lots of differences in both of them.



For more details go to the following link:

Ref Vs Out Keywords in C#
Ref And Out Keywords in C#
11. Can “this” be used within a static method?

Answer: 

We can't use this in static method because keyword 'this' returns a reference to the current instance of the class containing it. Static methods (or any static member) do not belong to a particular instance. They exist without creating an instance of the class and call with the name of a class not by instance so we can’t use this keyword in the body of static Methods, but in case of Extension Methods we can use it the functions parameters. Let’s have a look on “this” keyword.

The "this" keyword is a special type of reference variable that is implicitly defined within each constructor and non-static method as a first parameter of the type class in which it is defined. For example, consider the following class written in C#.

For more follow this link:

"this" Keyword in C#
this keyword in C#
12. Define Property in C#.net?

Answer:

Properties are members that provide a flexible mechanism to read, write or compute the values of private fields, in other words by the property we can access private fields. In other words we can say that a property is a return type function/method with one parameter or without a parameter. These are always public data members. It uses methods to access and assign values to private fields called accessors.

Now question is what are accessors?

The get and set portions or blocks of a property are called accessors. These are useful to restrict the accessibility of a property, the set accessor specifies that we can assign a value to a private field in a property and without the set accessor property it is like a read-only field. By the get accessor we can access the value of the private field, in other words it returns a single value. A Get accessor specifies that we can access the value of a field publically.

We have the three types of properties 
Read/Write.
ReadOnly.
WriteOnly
For more details follow the link:

Property in C#
Properties In C#
13. What is extension method in c# and how to use them?

Answer: 

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

Back To Basics - Dispose Vs Finalize
15. What is the difference between string and StringBuilder in c#?

Answer: 

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

Comparison of String and StringBuilder in C#
String and StringBuilder Classes
16. What is delegates in C# and uses of delegates?

Answer: 

C# delegates are same as pointers to functions, in C or C++. A delegate Object is a reference type variable that use to holds the reference to a method. The reference can be changed at runtime which is hold by an object of delegate, a delegate object can hold many functions reference which is also known as Invocation List that refers functions in a sequence FIFO, we can new functions ref in this list at run time by += operator and can remove by -= operator. 

Delegates are especially used for implementing events and the call-back methods. All delegates are implicitly derived from the System.Delegate class.

Let’s see how to use Delegate with Example:



For More details read this article:

C# Delegates
Delegates in C#
17. What is sealed class in c#?

Answer: 

Sealed classes are used to restrict the inheritance feature of object oriented programming. Once a class is defined as a sealed class, the class cannot be inherited. 

In C#, the sealed modifier is used to define a cla
