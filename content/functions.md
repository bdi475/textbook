# Functions

Let's forget about Python for a moment and go back a few years all the way back to Algebra. Do you remember any expressions that resemble the form of `f(x) = x + 3`?

In this expression, `f` is a function that takes an input `x` and produces an output by adding `3` to it. This is the basic idea behind functions: they take inputs, process them, and produce outputs.

In programming, **functions** serve a similar purpose. They are reusable blocks of code that perform a specific task. Functions help to organize code, make it more readable, and allow for code reuse.

In Python, functions are defined using the `def` keyword, followed by the function name and parentheses.

Here's a simple example of a function that prints a greeting message.

```python
def my_function():
    print("Hello from my function!")
```

To call the function and execute its code, you simply use the function name followed by parentheses.

```python
my_function()
```

Here's the output of the above code:

```
# Output:
Hello from my function!
```

Functions can also take parameters, which are values that you can pass into the function to customize its behavior. Here's an example of a function that takes a parameter and uses it in the greeting message.

```python
def greet(name):
    """This function greets the person passed in as a parameter."""
    print(f"Hello, {name}!")
```

In the example above, we defined a function named `greet` that takes one parameter, `name`. The function prints a greeting message using the provided name.

## Parameters and Arguments

Functions can take multiple parameters, which are specified within the parentheses in the function definition. When calling the function, you provide arguments that correspond to these parameters.

```python
def add_numbers(a, b):
    return a + b

result = add_numbers(5, 10)
print(result)  # Output: 15
```

In this example, the `add_numbers` function takes two parameters, `a` and `b`, and returns their sum. When we call the function with the arguments `5` and `10`, it returns `15`.

:::{tip} What is the difference between parameters and arguments?

- **Parameters** are the variables listed in the function definition. They act as placeholders for the values that will be passed to the function when it is called.
- **Arguments** are the actual values that are passed to the function when it is called.

They are used interchangeably in casual conversation, but technically, parameters refer to the function's definition, while arguments refer to the function's invocation.
:::

## Return Values

Functions can return values using the `return` statement. This allows you to capture the output of a function and use it elsewhere in your code.

```python
def square(x):
    return x * x

result = square(4)
print(result)  # Output: 16
```

In this example, the `square` function takes a number `x` as a parameter and returns its square. When we call the function with the argument `4`, it returns `16`, which we then print.

:::{tip} What happens if a function does not have a return statement?
If a function does not have a `return` statement, it will return `None` by default. This means that if you try to capture the output of such a function, you will get `None`.
:::

:::{hint} What is a `None` value?
`None` is a special constant in Python that represents the absence of a value or a null.

It is often used to indicate that a variable has no value or that a function does not return anything meaningful.

```python
some_variable = None
print(some_variable)  # Output: None

if some_variable is None:
    print("The variable has no value.")

# You can use the logical not operator to check for a None value
if some_variable is not None:
    print("The variable has a value.")
```

:::

If we modify the previous `square()` function to remove the `return` statement:

```python
def square(x):
    print(x * x) # Note: No return statement

result = square(4)
print(result)  # Output: None
```

Here's the output of the above code:

```
16
None
```

The `16` is printed from within the `square` function, but since there is no `return` statement, the function returns `None`, which is then printed as the value of `result`.

:::{tip} Can a function return multiple values?

Yes, a function can return multiple values by separating them with commas in the `return` statement. When you call the function, it will return a tuple containing all the values.

```python
def get_coordinates():
    return 10, 20

coordinates = get_coordinates()
print(coordinates)  # Output: (10, 20)
```

:::

## Examples

Here are a few more examples of functions in Python:

```python
def multiply(a, b):
    return a * b
result = multiply(3, 4)
print(result)  # Output: 12
```

```python
def is_even(number):
    return number % 2 == 0
print(is_even(4))  # Output: True
print(is_even(5))  # Output: False
```

```python
def is_absolute_equal(a, b):
    return abs(a) == abs(b)
print(is_absolute_equal(-5, 5))  # Output: True
print(is_absolute_equal(-5, 4))  # Output: False
```

## Built-in Functions

Python comes with many built-in functions that you can use without needing to define them yourself. Some common built-in functions include:

- `print()`: Outputs text to the console.
- `len()`: Returns the length of a collection (like a list or string).
- `type()`: Returns the type of an object.
- `int()`, `float()`, `str()`: Convert values to integers, floats
- `sum()`: Returns the sum of a collection of numbers.
- `max()`, `min()`: Return the maximum or minimum value from a collection.
- `abs()`: Returns the absolute value of a number.
- `round()`: Rounds a floating-point number to the nearest integer or to a specified number of decimal places.
- `sorted()`: Returns a sorted list from the elements of any iterable.
- `range()`: Generates a sequence of numbers, often used in loops.
- `input()`: Reads a line of input from the user.
- `help()`: Provides help information about a function or module.
- `dir()`: Lists the attributes and methods of an object.
- `enumerate()`: Adds a counter to an iterable and returns it as an enumerate object.
