#Lab#0 APPOO Balan Dorin FAF-131

## Compare core OOP concepts of `Java` and `C#`

Comparing by definitions imply that compared elements can be equal. In my case,if we take as comparing criteria OOP concepts, then these 2 laguages are the same. I will show it with a few examples.

## 1.Inheritance 
One of the most important concepts in object-oriented programming is that of inheritance. Inheritance allows us to define a class in terms of another class, which makes it easier to create and maintain an application. This also provides an opportunity to reuse the code functionality and fast implementation time.
Inheritance example in C# 
```C#
class Shape 
   {
      public void setWidth(int w)
      {
         width = w;
      }
      public void setHeight(int h)
      {
         height = h;
      }
      protected int width;
      protected int height;
   }

   // Derived class
   class Rectangle: Shape
   {
      public int getArea()
      { 
         return (width * height); 
      }
   }
```
Class Rectangle inherits all Shape's proprieties. Also it can add another.
Inheritance example in Java.

```Java
class Shape 
   {
      public void setWidth(int w)
      {
         width = w;
      }
      public void setHeight(int h)
      {
         height = h;
      }
      protected int width;
      protected int height;
   }

   // Derived class
   class Rectangle extends Shape
   {
      public int getArea()
      { 
         return (width * height); 
      }
   }
```
Difference here is only in syntax, in Java we have the *extends* keyword. 

## 2.Polymorphism

Polymorphism is the ability of an object to take on many forms. The most common use of polymorphism in OOP occurs when a parent class reference is used to refer to a child class object.
The simpliest example is with function overloading.

C# Example
```C#
class Printdata
   {
      void print(int i)
      {
         Console.WriteLine("Printing int: {0}", i );
      }

      void print(double f)
      {
         Console.WriteLine("Printing float: {0}" , f);
      }

      void print(string s)
      {
         Console.WriteLine("Printing string: {0}", s);
      }
      
// calling these function will be in following way:
// Call print to print integer
    p.print(5);
         
// Call print to print float
    p.print(500.263);
         
// Call print to print string
    p.print("Hello C#");
```

Java example

```Java
class Printdata
   {
      void print(int i)
      {
         System.out.println("Printing int: {0}", i );
      }

      void print(double f)
      {
         System.out.println("Printing float: {0}" , f);
      }

      void print(string s)
      {
         System.out.println("Printing string: {0}", s);
      }
      
// calling these function will be in following way:
// Call print to print integer
    p.print(5);
         
// Call print to print float
    p.print(500.263);
         
// Call print to print string
    p.print("Hello C++");
```

## 3.Encapsulation
Encapsulation is defined 'as the process of enclosing one or more items within a physical or logical package'. Encapsulation, in object oriented programming methodology, prevents access to implementation details.

C# Example 
```C#
class Coordinates
{
	public int x;
    protected int y; 
    private int z; 
    internal int s; 
    protected internal int p;
    
    //...
}
```

Java Example: 

```Java
class Coordinates
{
	int x; // default packed
    public int y; 
    private int z; 
    protected int s; 
    
    //...
}
```
## Comparison
Because making a table in markdown is funless, I will just give some advantages and disadvantages:

* In Java, all methods are virtual by default and can only be made non-virtual by using the final keyword. In C#, all methods are non-virtual by default, and can only be made virtual through the same keyword.
* One disadvantage with C# is that the class designer has to guess which methods should be virtual and which methods should not, and if he guesses wrong, then problems ensue.
* Another C# disadvantage is that the class designer and developers inheriting from this class must do more work. In Java, the class designer creates a class, and assumes that any method not declared as final may be overridden by any subclass. In C#, the class designer must choose which methods to declare virtual, which requires more brainpower. Both he and the developers who subclass this base are also required to do more typing and thinking.
* One advantage to C# is that the code should run faster, because there should be fewer virtual methods. The compiler will more often determine at compile-time which actual functions should be called. In Java, methods must almost always be treated as virtual so these decisions must be put off until run time.
* In C# there are 5 access specifiers : public, protected, private, internal and protected internal. In Java we have 4 : default packed, public, private, protected. 

##Conclusion
 After all, all programming languages are equivalent. There is nothing that can be done in C++ that can't be done in C# that can't be done in Java that can't be done using assembly language that can't be done using 1's and 0's by a good typist with an incredible memory. 
