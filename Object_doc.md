#Compiled by “Team Moses”: Joshua Wilkerson, Asiah Bennett, Nyah Macklin,  Eric Espinoza, Finesse Carter, Zahmir Jacobs, and Vanessa Charles

# OBJECTS in JavaScript

# What is an object?
# An object is an unordered list of properties, methods, and attributes which are made up of a key and a value associated with # it.
# EX: Car is the object
# Properties: are the specific characteristics of the object. It is what differentiates two or more objects from each other. ex: a car is the object. The properties could be the model, the color, the brand or weight.
#  make- Chevy, model- Cruz, year-2018
# Method: start(), stop(), move()
# Object example
# Here is the JavaScript representation of a blue Bic ballpoint pen.
# const pen = {
# type: "ballpoint",
# color: "blue",
# brand: "Bic"
# };
# How are objects useful in JavaScript?
# JavaScript objects can be created by simply setting their properties within a pair of curly braces: {...}. Each property is a # key/value pair (A Key points to a value stored in memory). This is called an object literal.
The advantage is that the things that belong together are put together in code. Such as anything key/value pair associated with the object “pen” should be in that object.
Objects allow for leeway to be creative. Nothing is definite.
Higher-order Functions- are functions inside of functions (allow for higher abstrations)
What is Object Oriented Programming(OOP)?
Programming languages that use objects in programming. The main aim of OOP is to bind together the data and the functions that operate on them so that no other part of the code can access this data except that function.

Primitive and Reference Types
Both are accessed through objects
Primitive Types
The 7 primitive Types- pieces of data that are stored as is; boolean, number, string, Null, undefined, bigInt, symbol.
Variable containing primitive value directly holds the primitive value As opposed to a pointer
Typeof operator is the best way to find type of primitive value
Reference Type-
represent objects in JS that are the closest thing to classes
Reference values are instances of reference types and are synonymous with objects
Reference Types do not store the object directly into the variable but points to the location in memory where the object exists

Using Constructor (a  function that uses new to create an object
Dereferencing Objects-


There are a couple of OOP concepts one should know
Encapsulation: is when methods, properties, and attributes are bundled within an object.
Abstraction:  refers to hiding the details of the implementation from the outside the class.
Inheritance: -inheritance can occur between objects with no class like structure defining the relationship...aka prototypes
Polymorphism:
Aggregation:

How Do You Create New Objects?
1. Use an object initializer
Simply setting its value in a set of curly braces
2. (Create a constructor function and then instantiate an object invoking that function in conjunction with the new operator.)\
How to access the properties and methods in objects?
Let's look at built-in JavaScript properties and methods
Array.isArray- method best fit for identifying arrays
You can assign numbers, strings, and even other objects to property





How to manipulate those properties and methods in objects?
“delete “ - the Delete operator removes the intended property from the table. If at any point you target a property that does not exist the return will be undefined.
Functions and Arrays in Objects:


	Primitive and Reference Values
Primitive Vs Reference Values
Both are accessed through objects
Primitive- pieces of data that are stored as is; boolean, number, string,
Null, undefined
Variable containing primitive value directly holds the primitive value
As opposed to a pointer
typeof operator is the best way to find a type of primitive value
Reference Type- represent objects in JS that are the closest thing to classes
Reference values are instances of reference types and are synonymous with objects
Objects are an unordered list of properties consisting of a name (string) and a value
Many ways to instantiate an object including
Using Constructor (a  function that uses new to create an object
Reference Types do not store the object directly into the variable
Reference holds a pointer (or reference) to the location in memory where the object exists
Dereferencing Objects- JS is garbage collection language memory allocations are recycled-- best practice to dereference objs no longer needed
Built-in Types-Array, Date, Error, Function, Object, RegEXP
	Array- ordered list of numerically indexed values
Array.isArray- method best fit for identifying arrays
Primitive Wrapper Types(PWT)- (String, Number, and Boolean)
PWT- reference types that are created behind the scenes whenever string numbers or booleans are read
JS has no classes but it uses types, variables or data is associated with specific primitive or reference types



Object-Oriented
Encapsulation: is when methods, properties, and attributes are bundled within an object.
Abstraction:  refers to hiding the details of the implementation from the outside the class.
Inheritance:  Allows to uses properties from other objects
Polymorphism:
Aggregation:


Spaghetti code:  is unstructured and difficult to read code that can cause problems. This can break the code.









Chapter 1:



Chapter 2:
	Functions are objects - they behave differently than functions in other languages
Deceleration Vs. Expressions- two literal terms of functions
Deceleration- starts with a function keyword and includes the name of the function right after it
Ex:
	Function add(num1, num2){
		Return num1 + num2	;
}

Expressions- these functions do not require a name after, and is considered an anonymous object function
Ex:
	Var add = function(num1, num2){
		Return num1 + num2
};
Functions as Values
You can use a function anywhere you would use any other reference value





Chapter 3: Defining properties:
Properties are the specific characteristics of the object. It is what differentiates two or more objects from each other. ex: a car is an object. The properties could be the model, the color, the brand of the car or the weight. Both use the same object but are created to be something new.
 Var car1 = {brand: toyota};
Var car2 = new object()

Car1.color = “red”;
Car2.color = “blue”;

Car1.weight = “805 kg”;
Car1.weight = “8o5 kg”;

Removing Properties
	For removing properties the Delete operator removes the intended property from the table. If at any point you target a property that does not exist the return will be undefined. Lastly there are some things that cannot be deleted, an example of this is

var person1 = {
name: "Nicholas"
};
console.log("name" in person1); // true
delete person1.name; // true - not output
console.log("name" in person1); // false
 console.log(person1.name); // undefined

The return comes back false when the delete is applied, meaning it didn’t work! When the property comes back truthy or true is when the property has been deleted properly from the object.

Types of properties
There are two types of properties. The first is the data, they contain a value like a name property.
	The second is the accessor properties. This one defines the function call, but they do not have a value inside of them.
For the accessor properties, they can only use getter or setter as well as using both of them at the same time. The getter is when the function is read. The setter is when the function to call is written.
The getter: Are expected to return a value.
The setter: Received the value being assigned to the property as an argument.

Preventing Object Modification
	Object.preventExtensions() is the method that is used to stop any kind of changes to the properties again. This is one of the ways to create a non extensible object.  An example of this:
var person1 = {
name: "Nicholas"
};
❶ console.log(Object.isExtensible(person1)); // true
❷ Object.preventExtensions(person1);
console.log(Object.isExtensible(person1)); // false
❸ person1.sayName = function() {
console.log(this.name);
};
console.log("sayName" in person1); // false

Number one of the example is showing the extension being checked. Number two is the extension being prevented. It is now non-extensible. Number three will not be added because the method was successful.

Chapter 4: Constructors and Prototypes:
What is a constructor?

A Constructor is a normal function that is called with a new operator.

*The only visual difference between a regular function and a constructor is that the function name should be capitalized when it is a constructor.*

ie: function person(){ vs function Person(){

Pros: Objects created with the same constructor have the same properties and methods.
What is a Prototype?
Think of prototypes as recipes for objects. Every cake has to have a recipe. Every function has a prototype property.
How do you identify it?
[[Prototype]] is a pointer back to the prototype object that the instance is using. -- When you create a new object using new, constructor’s prototype property is assigned to the [[Prototype]] property of that new object.
How do you use them?


Chapter 5: Inheritance
What is inheritance?
In traditional object-oriented languages classes inherit properties from other classes. In Javascript-inheritance can occur between objects with no class like structure defining the relationship...aka prototypes
What are the two names prototypes are referred to as? What do they do?
Prototype chaining/Prototype inheritance: child objects inherit methods and attributes from their parents.
Defining these objects and their inheritance structures is a matter of creating classes that extend one another. A class is a definition of attributes and behaviors, an object is an instance of a given class.
EX:  you might have a base Animal class with methods that allow animals to eat() and sleep(). Then, your Dog class inherits the eat() and sleep() methods from its Animal parent class while also defining its own methods like bark() and be_undyingly_loyal().

Why is inheritance important?
It helps build reusable and modular components of software applications because we can inherit from and extend the parent class in many different ways.
What is constructor inheritance?
The constructor property returns a reference to the object constructor function that created the instance object. The value is only read-only for primitive values such as 1, true, and "test"
EX: 	input
	function Tree(name) { this.name = name }
let theTree = new Tree('Redwood')
console.log('theTree.constructor is ' + theTree.constructor)
output
theTree.constructor is function Tree(name) { this.name = name }
Chapter 6: Object Patterns
In Javascript there are different ways to create objects. You can create your own custom types and generic objects to accomplish your goals. There are Private and Privileged Members, Module Patterns, Scope-Safe Constructors and Mixins to make more complex objects.

The module pattern is an object-creation pattern designed to create singleton objects with private data. The basic approach is to use an immediately invoked function expression that returns an object.

var yourObject = (function() {
// private data variables
return {
// public methods and properties
}; }());

Mixins allow us to use functions of one class as a function of another class without inheritance.

function mixin(receiver, supplier) { for (var property in supplier) { if (supplier.hasOwnProperty(property)) { receiver[property] = supplier[property] } }

Scope-safe constructors are constructors that you can call with or without new to create a new object instance. This pattern takes advantage of the fact that this is an instance of the custom type as soon as the constructor begins to execute, which lets you alter the constructor’s behavior depending on whether or not you used the new operator.

function Book(name, year) {
  if (!(this instanceof Book)) {
    return new Book(name, year);
  }
  this.name = name;
  this.year = year;
}

var person1 = new Book("js book", 2014);
var person2 = Book("js book", 2014);

console.log(person1 instanceof Book);    // true
console.log(person2 instanceof Book);    // trueBook(name, year) {
  if (!(this instanceof Book)) {
    return new Book(name, year);
  }
#   this.year = year;
# }

# var person1 = new Book("js book", 2014);
# 
# console.log(person1 instanceof Book);    // true
# console.log(person2 instanceof Book);    // true
