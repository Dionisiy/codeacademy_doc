### Introduction to Objects

The very basic building block of JavaScript are primitive data types. We know of three primitives:

* **strings** \(_e.g._ `"dogs go woof!"`\)
* **numbers** \(_e.g._ `4`, `10`\)
* **booleans** \(_e.g._ `false`, `5 > 4`\)

Arrays filled with objects will work just like arrays filled with numbers and strings.

In the same way we may loop through an array of numbers to print them out or calculate a sum, we can loop through an array of objects and access properties or methods.

We know two ways of storing data types. We can use variables or arrays. We use variables to store data \(like strings or numbers\) that we’d later want to access.

An array is exactly the same as a variable in that it stores data. The difference is that an array can store many more values while a variable can only store one.

To access arrays, we use bracket notation and remember that arrays use 0-based indexing \(i.e., the first value in an array is at position 0\).

data type: **objects**. This data type is a little bit more complex. Objects allow us to represent in code real world things and entities \(such as a person or bank account\). We do this by storing all relevant information in one place—an object.

### Properties

Let's review what we previously covered. Each piece of information we include in an object is known as a **property**. Think of a property like a**category label** that belongs to some object. When creating an object, each property has a name, followed by `:`and then the **value** of that property.

In addition to dot notation, we can also access properties using **bracket notation**. In this case we use`ObjectName["PropertyName"]` to access the desired property. Note, we need `" "`around the property's name.

### **Another Way to Create**

The method we've used to create objects uses **object literal notation**—that is, creating a new object with `{ }`and defining properties within the brackets.

Another way of creating objects without using the curly brackets `{ }` is to use the keyword `new`. This is known as creating an object using a **constructor**.

The `new` keyword creates an empty object when followed by `Object()`. The general syntax is:

```
var objectName = new Object();

```

We then have to fill this object with properties and labels.

**Function Review**

Methods are an important part of object oriented programming \(OOP\). OOP is an important part of programming which we'll dive into later.

Methods are similar to functions. To prepare for methods, let's do a quick refresher on functions.

Functions are defined using the`function` keyword followed by:

1. A pair of parentheses `( )` with optional parameters inside.
2. A pair of curly braces with the function's code inside `{ }`.
3. A semicolon `;`.

In the last section, we discussed properties. We can think of properties as variables associated with an object. Similarly, a **method** is just like a_function_ associated with an object.

### **Why Are Methods Important?**

Methods serve several important purposes when it comes to objects.

* They can be used to change object property values.

* They can be used to make calculations based on object properties. Functions can only use parameters as an input, but methods can make calculations with object properties.


### **The "this" Keyword**

The keyword `this` acts as a placeholder, and will **refer to whichever object called that method** when the method is actually used.

### **More Kinds of Methods**

### **The Object Constructor**

We mentioned the term **constructor **back in section one, when we talked about making an object using the keyword `new`. A **constructor** is a way to create an object.

This means we have to add our properties one at a time, just like we've been doing. To review, we've created `bob` using the constructor and defined the `name` property for you.

### **Custom Constructors**

But this approach of adding in properties one at a time for every object is tedious! Instead of always using the boring `Object` constructor, we can make our own constructors.

This way we can set the properties for an object right when it is created. So instead of using the `Object`constructor which is empty and has no properties, _we can make our own constructors which have properties_.

To see how this works, look at our`Person` constructor in [lines 1](javascript:void(0)\)–4. This constructor is used to make `Person`objects. Notice it uses the keyword`this` to define the `name` and `age`properties and set them equal to the parameters given.

Now we can use this constructor to make our good friends `bob` and `susan`in only one line each! Look at [lines 7](javascript:void(0)\)–8: once we have the constructor, it's way easier to make people because we can include their `name` and `age` as arguments to their respective constructors.

### **Constructors With Methods**

In addition to setting properties, constructors can also define methods. This way, as soon as the object is created it will have its own methods as well.

Here we have a `Rectangle` constructor, which sets the `height` and `width`properties equal to the arguments, just like our `Person` did with `name` and`age`.

```
function Rectangle(height, width) {
  this.height = height;
  this.width = width;
  this.calcArea = function() {
      return this.height * this.width;
  };
  // put our perimeter function here!
 this.calcPerimeter = function(){
     return (this.height+this.width)*2 ;
     }
}

var rex = new Rectangle(7,3);
var area = rex.calcArea();
var perimeter = rex.calcPerimeter();
```

Constructors are a way to make objects with the keyword `new`. The most basic constructor is the `Object`constructor, which will make an object with no methods or properties.

For more complicated objects we can make our own constructors and put in whatever properties and methods we want.

### **Arrays of Objects**

Remember that an object is just another _type_, like a string or number but more complex. This means that just as we can make arrays of numbers and strings, we can also make arrays of objects.

```
// Our person constructor
function Person (name, age) {
    this.name = name;
    this.age = age;
}

// Now we can make an array of people
var family = new Array();
family[0] = new Person("alice", 40);
family[1] = new Person("bob", 42);
family[2] = new Person("michelle", 8);
// add the last family member, "timmy", who is 6 years old
family[3] = new Person("timmy", 6);

```

### **Passing Objects into Functions**

In addition to making arrays of Objects, we can use objects as parameters for functions as well. That way, these functions can take advantage of the methods and properties that a certain object type provides.

**What Are Objects For?**

Objects provide us with a way to represent real-world or virtual things. We can do this by storing information inside the object's properties. There are two basic ways to make objects:

**Literal Notation**, where we use

```
var Name = { };

```

**Constructor Notation**, where we use the keyword `new`.

### **Properties**

Properties are like variables that belong to an object, and are used to hold pieces of information. Properties can be accessed in two ways:

* **Dot notation**, with`ObjectName.PropertyName`

### **Customizing Constructors**

In addition to the basic `Object`constructor, we can define our own custom constructors. These are helpful for two reasons:

1. We can assign our objects properties through parameters we pass in when the object is created.
2. We can give our objects methods automatically.

### **Methods**

**Methods** are like functions that are associated with a particular object.

They are especially helpful when you want to either:

1. Update the object properties
2. Calculate something based on an object's properties.

