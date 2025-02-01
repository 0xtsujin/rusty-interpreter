# Language Spec

# What
This doc describes the language features which our interpreter will implement.

# Syntax
TODO

# Features
* Variable Binding
* Arithmetic Expressions
* Built-in Functions
    *  std lib
* First-class Functions
    * Treat functions as values - assign to variables, pass around ([stack](https://stackoverflow.com/questions/10141124/any-difference-between-first-class-function-and-high-order-function))
* Higher-Order Functions
    * Functions which can accept other functions as input and return other functions ([stack](https://stackoverflow.com/questions/10141124/any-difference-between-first-class-function-and-high-order-function))
* Closures
    * Persistent scope for functions to hold onto their local variables even after execution
    * [stack post](https://stackoverflow.com/questions/36636/what-is-a-closure)
    * [r/cseli5](https://www.reddit.com/r/csELI5/comments/1q1eh8/eli5_closures/)
* Explicit and Implicit Returns
* Comments

# Data Types
* Integers
* Booleans
* String
* Array
* Hash

# Examples
Variable Binding
```
let age = 1;
let name = "Monkey";
let result = 10 * (20 / 2);
```

Arrays
```
let myArray = [1, 2, 3, 4, 5];
myArray[0] // => 1
```

Hashes
```
let thorsten = {"name": "Thorsten", "age": 28};
thorsten["name"] // => "Thorsten"
```

Functions
```
// explicit return
let add = fn(a, b) { return a + b; };

// implicit return
let add = fn(a, b) { a + b; };

// invoking a function
add(1, 2);
```

Higher-Order Functions
```
let twice = fn(f, x) { return f(f(x));
};
let addTwo = fn(x) { return x + 2;
};
twice(addTwo, 2); // => 6
```
