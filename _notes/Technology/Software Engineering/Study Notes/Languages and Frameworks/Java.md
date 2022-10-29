---
title : Java
notetype : feed
date : 29-10-2022
---

##### Wrapper Classes
	- Classes that wrap primitive type to their object instances
	- Immutable

```
Integer number = new Integer(55);//int 
Integer number2 = new Integer("55");//String
```

use Integer.valueof() for memory and performance reasons

##### Autoboxing
Process of converting primitive types into their corresponding Wrapper classes
 
```
Integer nineA = new Integer(9); new object
Integer nineB = 9; //uses existing objects
```

##### Casting
Converting from one data type to another
```
Long a = 5;// implicit casting
int b = (int)34.5;// explicit casting
```

##### Strings
- Strings are immutable
- Stored in `string constant pool` in heap memory. reuses if it is already existing in heap. 
	- String a = new String always creates as new object
- str2.contact("a") creates new string object so use string builder for memory and performance
-

##### Class
- Class is a template and it has state and behavior. 
- Object is an instance of a class
- state of an object -> values assigned to 

**toString**
	- Used to print content of an object
	- default toString from Object class gives objectname@hashcode
	- can be overridden in our class
**equals** 	
	- default checks if two classes point to same object
	- override to check for specific member variables
**hashcode**	
	- It is like a number for an object and used to store in a bucket
	- used to retrieve the location when contains is called
	- https://stackoverflow.com/questions/3563847/what-is-the-use-of-hashcode-in-java
	
##### Inheritance 
It is inheriting or extending properties of another (parent) class

**Method overloading**
		- methods with different parameters and return type
		- child class overloading with a different param
		- or constructor with different params
		- or a collection having different methods like
				addAll(index, collection)
				addAll(collection)
**Method overriding**
		- methods with same params 
		- HashMap public int size() overrides AbstractMap public int size()
		
**RunTime Polymorphism**
- superclass can have reference to subclass. This can be used in method signatures in compile time so any subclass can be passed and superclass can handle it

```
public void animalDoctor(Animal snimal){
}
animslDoctor(new Dog())
```

- The methods overridden in subclass will be invoked even when using superclass reference.

A class can't extend multiple classes

##### Interface
- Interface can have public abstract methods
- It has by default public static final member variables
- It can have default definitions for methods from Java 1.8
- A class can implement multiple interfaces
- An interface can extend another interface


**Interface vs Abstract**
- When you have similar functionalities in multiple classes, you group them and create abstract class. Abstract class can't be instantiated
- When you want to have an abstraction and communicate between two, you agree upon a contract which is an interface and they can all this interface