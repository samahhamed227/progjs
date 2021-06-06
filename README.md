# Control flow
The control flow is the order in which the computer executes statements in a script.

Code is run in order from the first line in the file to the last line, unless the computer runs across the (extremely frequent) structures that change the control flow, such as conditionals and loops. 

# Function declarations
A function definition (also called a function declaration, or function statement) consists of the function keyword, followed by:

1. The name of the function.
2. A list of parameters to the function, enclosed in parentheses and separated by commas.
3. The JavaScript statements that define the function, enclosed in curly brackets, {...}.

# Function expression
The function keyword can be used to define a function inside an expression.

You can also define functions using the Function constructor and a function declaration.

# Calling functions
Defining a function does not execute it. Defining it names the function and specifies what to do when the function is called.

Calling the function actually performs the specified actions with the indicated parameters. For example, if you define the function square, you could call it as follows:

square(5);


# Function scope
Variables defined inside a function cannot be accessed from anywhere outside the function, because the variable is defined only in the scope of the function. However, a function can access all variables and functions defined inside the scope in which it is defined.

# Scope and the function stack
Recursion
A function can refer to and call itself. There are three ways for a function to refer to itself:

1. The function's name
2. arguments.callee
3. An in-scope variable that refers to the function

# Within the function body, the following are all equivalent:

bar()
arguments.callee()
foo()

# Nested functions and closures
The inner function can be accessed only from statements in the outer function.
The inner function forms a closure: the inner function can use the arguments and variables of the outer function, while the outer function cannot use the arguments and variables of the inner function.

 # Name conflicts
When two arguments or variables in the scopes of a closure have the same name, there is a name conflict. More nested scopes take precedence. So, the inner-most scope takes the highest precedence, while the outer-most scope takes the lowest. This is the scope chain.
 
 # Closures
Closures are one of the most powerful features of JavaScript. JavaScript allows for the nesting of functions and grants the inner function full access to all the variables and functions defined inside the outer function (and all other variables and functions that the outer function has access to).

# Using the arguments object
The arguments of a function are maintained in an array-like object. Within a function, you can address the arguments passed to it as follows:

arguments[i]

# Function parameters
Starting with ECMAScript 2015, there are two new kinds of parameters: default parameters and rest parameters.

# Default parameters
In JavaScript, parameters of functions default to undefined. However, in some situations it might be useful to set a different default value. This is exactly what default parameters do.

* Without default parameters (pre-ECMAScript 2015)
In the past, the general strategy for setting defaults was to test parameter values in the body of the function and assign a value if they are undefined.

# Arrow functions
An arrow function expression (previously, and now incorrectly known as fat arrow function) has a shorter syntax compared to function expressions and does not have its own this, arguments, super, or new.target. Arrow functions are always anonymous. See also this hacks.mozilla.org blog post: "ES6 In Depth: Arrow functions".

# No separate this
Until arrow functions, every new function defined its own this value (a new object in the case of a constructor, undefined in strict mode function calls, the base object if the function is called as an "object method", etc.).

