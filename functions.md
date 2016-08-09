### **Function syntax**

A function takes in inputs, does something with them, and produces an output.

```
var sayHello = function(name) {
    console.log('Hello ' + name);
};
```

1. First we declare a function using`var`, and then give it a name `sayHello`. The name should begin with a lowercase letter and the convention is to use lowerCamelCase where each word \(except the first\) begins with a capital letter.
2. Then we use the `function` keyword to tell the computer that you are making a function
3. The code in the parentheses is called a **parameter**. It's a placeholder word that we give a specific value when we call the function. Click "Stuck? Get a hint!" for more.
4. Then write your block of reusable code between `{ }`. Every line of code in this block must end with a `;`.

You can run this code by "calling" the function, like this:

```
sayHello("Emily");

```

Calling this function will print out `Hello Emily`.

### **How does a function work?**

```
var functionName = function( ) {
    // code code code
    // code code code
    // (more lines of code)
};
```

1. The `var` keyword declares a variable named `functionName`.
2. The keyword `function` tells the computer that `functionName` is a function and not something else.
3. Parameters go in the parentheses. The computer will look out for it in the code block.
4. The code block is the reusable code that is between the curly brackets `{ }`. Each line of code inside`{ }` must end with a semi-colon.
5. The entire function ends with a semi-colon.

To use the function, we **call** the function by just typing the function's name, and putting a parameter value inside parentheses after it. The computer will run the reusable code with the specific parameter value substituted into the code.

At the end of each line of code \(within the `{ }`\) and after the entire function \(after the `{ }`\), please put a semi-colon. The semi-colon acts like a period in a sentence. It helps the computer know where there are stopping points in the code.

### **Don't Repeat Yourself \(D.R.Y\)**

he D.R.Y. principle is really important in programming. No repeating!

Any time you find yourself typing the same thing, but modifying only one small part, you can probably use a function.

The 'small part' that you find yourself modifying will be the parameter. And the part that you keep repeating will be the code in the reusable block - the code inside `{ }`

### **Return keyword**

Sometimes, we just want it to`return` a value. We can then use that value \(ie. the output from the function\) in other code.

The `return` keyword simply gives the programmer back the value that comes out of the function. So the function runs, and when the `return`keyword is used, the function will immediately stop running and `return`the value.

### 

### **Functions with two parameters**

So far we've only looked at functions with one parameter. But often it is useful to write functions with more than one parameter. For example, we can have the following function:



```
var areaBox = function(length, width) {
    return length * width;
};

```


