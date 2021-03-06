# Introduction to Object-Oriented JavaScript

### **Object-oriented programming**

Object-oriented programming \(OOP\) is a programming paradigm that uses [abstraction](https://developer.mozilla.org/en-US/docs/Glossary/abstraction "abstraction: Abstraction in computer programming is a way to reduce complexity and allow efficient design and implementation in complex software systems. It hides the technical complexity of systems behind simpler APIs.") to create models based on the real world. OOP uses several techniques from previously established paradigms, including [modularity](https://developer.mozilla.org/en-US/docs/Glossary/modularity "modularity: The term Modularity refers to the degree to which a system's components may be separated and recombined, it is also division of a software package into logical units. The advantage of a modular system is that one can reason the parts independently"), [polymorphism](https://developer.mozilla.org/en-US/docs/Glossary/polymorphism "polymorphism: Polymorphism is the presentation of one interface for multiple data types.
 For example, integers, floats, and doubles are implicitly polymorphic: regardless of their different types, they can all be added, subtracted, multiplied, and so on."), and [encapsulation](https://developer.mozilla.org/en-US/docs/Glossary/encapsulation "encapsulation: Encapsulation is the packing of data and functions into one component (for example, a class) and then controlling access to that component to make a "blackbox" out of the object. Because of this, a user of that class only needs to know its interface (that is, the data and functions exposed outside the class), not the hidden implementation."). Today, many popular programming languages \(such as Java, JavaScript, C\#, C++, Python, PHP, Ruby and Objective-C\) support OOP.

OOP envisions software as a collection of cooperating objects rather than a collection of functions or simply a list of commands \(as is the traditional view\). In OOP, each object can receive messages, process data, and send messages to other objects. Each object can be viewed as an independent little machine with a distinct role or responsibility.

OOP envisions software as a collection of cooperating objects rather than a collection of functions or simply a list of commands \(as is the traditional view\). In OOP, each object can receive messages, process data, and send messages to other objects. Each object can be viewed as an independent little machine with a distinct role or responsibility.

### Terminology

**Namespace**
A container which lets developers bundle all functionality under a unique, application-specific name.

**Class**
Defines the object's characteristics. A class is a template definition of an object's properties and methods.

**Object**
An instance of a class.

**Property**
An object characteristic, such as color.

**Method**
An object capability, such as walk. It is a subroutine or function associated with a class.

**Constructor**
A method called at the moment an object is instantiated. It usually has the same name as the class containing it.

**Inheritance**
A class can inherit characteristics and capabilities from another class.
**Encapsulation**
A technique which involves bundling the data and the methods that use the data together.
**Abstraction**
The conjunction of an object's complex inheritance, methods, and properties to adequately reflect a reality model.
**Polymorphism**
Poly means "many" and morphism means "forms". Different classes might define the same method or property.

## **JavaScript object oriented programming**

### Namespace

A namespace is a container which allows developers to bundle up functionality under a unique, application-specific name. **In JavaScript a namespace is just another object containing methods, properties, and objects.**

> It's important to note that in JavaScript, there's no language-level difference between regular objects and namespaces. This differs from many other object-oriented languages, and can be a point of confusion for new JavaScript programmers.

The idea behind creating a namespace in JavaScript is simple: create one global object, and all variables, methods, and functions become properties of that object. Use of namespaces also reduces the chance of name conflicts in an application, since each application's objects are properties of an application-defined global object.

Let's create a global object called MYAPP:

```
// global namespace
var MYAPP = MYAPP || {};
```

In the above code sample, we first checked whether `MYAPP` is already defined \(either in same file or in another file\). If yes, then use the existing MYAPP global object, otherwise create an empty object called `MYAPP` which will encapsulate methods, functions, variables, and objects.

The following is code syntax for creating a namespace and adding variables, functions, and a method:

```
// Create container called MYAPP.commonMethod for common method and properties
MYAPP.commonMethod = {
  regExForName: "", // define regex for name validation
  regExForPhone: "", // define regex for phone no validation
  validateName: function(name){
    // Do something with name, you can access regExForName variable
    // using "this.regExForName"
  },

  validatePhoneNo: function(phoneNo){
    // do something with phone number
  }
}

// Object together with the method declarations
MYAPP.event = {
    addListener: function(el, type, fn) {
    // code stuff
    },
    removeListener: function(el, type, fn) {
    // code stuff
    },
    getEvent: function(e) {
    // code stuff
    }

    // Can add another method and properties
}

// Syntax for Using addListener method:
MYAPP.event.addListener("yourel", "type", callback);
```

### Custom objects

#### The class

JavaScript is a prototype-based language and contains no `class` statement, such as is found in C++ or Java. This is sometimes confusing for programmers accustomed to languages with a`class` statement. Instead, JavaScript uses functions as constructors for classes. Defining a class is as easy as defining a function. In the example below we define a new class called Person with an empty constructor.

```
var Person = function () {};
```

#### The object \(class instance\)

To create a new instance of an object `obj` we use the statement `new obj`, assigning the result \(which is of type `obj`\) to a variable to access it later.

In the example above we define a class named `Person`. In the example below we create two instances \(`person1` and `person2`\).

```
var person1 = new Person();
var person2 = new Person();
```

#### The constructor

The constructor is called at the moment of instantiation \(the moment when the object instance is created\). The constructor is a method of the class. In JavaScript the function serves as the constructor of the object, therefore there is no need to explicitly define a constructor method. Every action declared in the class gets executed at the time of instantiation.

The constructor is used to set the object's properties or to call methods to prepare the object for use. Adding class methods and their definitions occurs using a different syntax described later in this article.

In the example below, the constructor of the class `Person` logs a message when a `Person` is instantiated.

var Person = function \(\) {

console.log\('instance created'\);

};

var person1 = new Person\(\);

var person2 = new Person\(\);

#### The property \(object attribute\)

Properties are variables contained in the class; every instance of the object has those properties. Properties are set in the constructor \(function\) of the class so that they are created on each instance.

The keyword `this`, which refers to the current object, lets you work with properties from within the class. Accessing \(reading or writing\) a property outside of the class is done with the syntax:`InstanceName.Property`, just like in C++, Java, and several other languages. \(Inside the class the syntax `this.Property` is used to get or set the property's value.\)

In the example below, we define the `firstName` property for the `Person` class at instantiation:

```
var Person = function () {
  console.log('instance created');
};

var person1 = new Person();
var person2 = new Person();
```

#### The property \(object attribute\)

Properties are variables contained in the class; every instance of the object has those properties. Properties are set in the constructor \(function\) of the class so that they are created on each instance.

The keyword `this`, which refers to the current object, lets you work with properties from within the class. Accessing \(reading or writing\) a property outside of the class is done with the syntax:`InstanceName.Property`, just like in C++, Java, and several other languages. \(Inside the class the syntax `this.Property` is used to get or set the property's value.\)

In the example below, we define the `firstName` property for the `Person` class at instantiation:

```
var Person = function (firstName) {
  this.firstName = firstName;
  console.log('Person instantiated');
};

var person1 = new Person('Alice');
var person2 = new Person('Bob');

// Show the firstName properties of the objects
console.log('person1 is ' + person1.firstName); // logs "person1 is Alice"
console.log('person2 is ' + person2.firstName); // logs "person2 is Bob"
```

#### The methods

Methods are functions \(and defined like functions\), but otherwise follow the same logic as properties. Calling a method is similar to accessing a property, but you add `()` at the end of the method name, possibly with arguments. To define a method, assign a function to a named property of the class's `prototype` property. Later, you can call the method on the object by the same name as you assigned the function to.

In the example below, we define and use the method `sayHello()` for the `Person` class.

```
var Person = function (firstName) {
  this.firstName = firstName;
};

Person.prototype.sayHello = function() {
  console.log("Hello, I'm " + this.firstName);
};

var person1 = new Person("Alice");
var person2 = new Person("Bob");

// call the Person sayHello method.
person1.sayHello(); // logs "Hello, I'm Alice"
person2.sayHello(); // logs "Hello, I'm Bob"
```

In JavaScript methods are regular function objects bound to an object as a property, which means you can invoke methods "out of the context". Consider the following example code:

```
var Person = function (firstName) {
  this.firstName = firstName;
};

Person.prototype.sayHello = function() {
  console.log("Hello, I'm " + this.firstName);
};

var person1 = new Person("Alice");
var person2 = new Person("Bob");
var helloFunction = person1.sayHello;

// logs "Hello, I'm Alice"
 person1.sayHello();

// logs "Hello, I'm Bob"
person2.sayHello();

// logs "Hello, I'm undefined" (or fails
// with a TypeError in strict mode)
helloFunction();                                    

// logs true
console.log(helloFunction === person1.sayHello);

// logs true
console.log(helloFunction === Person.prototype.sayHello);

// logs "Hello, I'm Alice"
helloFunction.call(person1);
```

Inheritance

Inheritance is a way to create a class as a specialized version of one or more classes \(JavaScript only supports single inheritance\). The specialized class is commonly called the child, and the other class is commonly called the parent. In JavaScript you do this by assigning an instance of the parent class to the child class, and then specializing it. In modern browsers you can also use Object.create to implement inheritance.

In the example below, we define the class `Student` as a child class of `Person`. Then we redefine the `sayHello()` method and add the `sayGoodBye()` method.

```
// Define the Person constructor
var Person = function(firstName) {
  this.firstName = firstName;
};

// Add a couple of methods to Person.prototype
Person.prototype.walk = function(){
  console.log("I am walking!");
};

Person.prototype.sayHello = function(){
  console.log("Hello, I'm " + this.firstName);
};

// Define the Student constructor
function Student(firstName, subject) {
  // Call the parent constructor, making sure (using Function#call)
  // that "this" is set correctly during the call
  Person.call(this, firstName);

  // Initialize our Student-specific properties
  this.subject = subject;
}

// Create a Student.prototype object that inherits from Person.prototype.
// Note: A common error here is to use "new Person()" to create the
// Student.prototype. That's incorrect for several reasons, not least 
// that we don't have anything to give Person for the "firstName" 
// argument. The correct place to call Person is above, where we call 
// it from Student.
Student.prototype = Object.create(Person.prototype); // See note below

// Set the "constructor" property to refer to Student
Student.prototype.constructor = Student;

// Replace the "sayHello" method
Student.prototype.sayHello = function(){
  console.log("Hello, I'm " + this.firstName + ". I'm studying "
              + this.subject + ".");
};

// Add a "sayGoodBye" method
Student.prototype.sayGoodBye = function(){
  console.log("Goodbye!");
};

// Example usage:
var student1 = new Student("Janet", "Applied Physics");
student1.sayHello();   // "Hello, I'm Janet. I'm studying Applied Physics."
student1.walk();       // "I am walking!"
student1.sayGoodBye(); // "Goodbye!"

// Check that instanceof works correctly
console.log(student1 instanceof Person);  // true 
console.log(student1 instanceof Student); // true
```

#### Encapsulation

In the previous example, `Student` does not need to know how the `Person` class's `walk()`method is implemented, but still can use that method; the `Student` class doesn't need to explicitly define that method unless we want to change it. This is called **encapsulation**, by which every class packages data and methods into a single unit.

Information hiding is a common feature in other languages often as private and protected methods\/properties. Even though you could simulate something like this on JavaScript, this is not a requirement to do Object Oriented programming.[3](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript#cite-3)

#### Abstraction

Abstraction is a mechanism that allows you to model the current part of the working problem, either by inheritance \(specialization\) or composition. JavaScript achieves specialization by inheritance, and composition by letting class instances be the values of other objects' attributes.

The JavaScript Function class inherits from the Object class \(this demonstrates specialization of the model\) and the `Function.prototype` property is an instance of `Object` \(this demonstrates composition\).



```
var foo = function () {};

// logs "foo is a Function: true"
console.log('foo is a Function: ' + (foo instanceof Function));

// logs "foo.prototype is an Object: true"
console.log('foo.prototype is an Object: ' + (foo.prototype instanceof Object));
```



#### Polymorphism

Just as all methods and properties are defined inside the prototype property, different classes can define methods with the same name; methods are scoped to the class in which they're defined, unless the two classes hold a parent-child relation \(i.e. one inherits from the other in a chain of inheritance\).



