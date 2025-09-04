# Strings

A string is a sequence of characters enclosed in either single quotes (`'`) or double quotes (`"`). Strings are used to represent text data in Python.

## Creating Strings

You can create a string by enclosing characters in quotes. Both single and double quotes can be used interchangeably.

```python
my_string = "Hello, World!"
another_string = 'Python is fun!'
```

## String Operations

### Concatenation

You can concatenate (combine) strings using the `+` operator.

```python
greeting = "Hello, " + "World!"
print(greeting)  # Output: Hello, World!
```

### Repetition

You can repeat a string multiple times using the `*` operator.

```python
laugh = "Ha" * 3
print(laugh)  # Output: HaHaHa
```

### String Length

You can find the length of a string using the `len()` function.

```python
my_string = "BDI 475"
print(len(my_string))  # Output: 7
```

## String Methods

Strings come with a variety of built-in methods that allow you to manipulate and work with them. Here are some commonly used string methods:

### `lower()` and `upper()`

These methods convert a string to lowercase or uppercase, respectively.

```python
text = "Data Analytics"
print(text.lower())  # Output: data analytics
print(text.upper())  # Output: DATA ANALYTICS
```

### `strip()`

This method removes any leading and trailing whitespace from a string.

```python
text = "   I love data!   "
print(text.strip())  # Output: "I love data!"
```

### `replace()`

```python
text = "I love data!"
print(text.replace("data", "analytics"))  # Output: "I love analytics!"
```

This method replaces occurrences of a specified substring with another substring.

### `split()`

This method splits a string into a list of substrings based on a specified delimiter (default is whitespace).

```python
text = "I love data analytics"
words = text.split()
print(words)  # Output: ['I', 'love', 'data', 'analytics']
```

:::{tip} String Immutability
Strings in Python are immutable, meaning that once a string is created, it cannot be changed. Any operation that modifies a string will create a new string instead of altering the original one.

For example, using the `replace()` method does not change the original string but returns a new string with the modifications.
:::

### `join()`

This method joins a list of strings into a single string, with a specified separator.

```python
words = ['I', 'love', 'data', 'analytics']
sentence = ' '.join(words)
print(sentence)  # Output: "I love data analytics"
```

### `find()`

This method returns the lowest index of the substring if found in the string. If not found, it returns -1.

```python
text = "I love data analytics"
index = text.find("data")
print(index)  # Output: 7
```

## Strings as Ordered Collections

Although it is not a collection type like lists or dictionaries, strings can be treated as collections of characters, allowing you to iterate over them using loops.

```python
my_string = "ILLINI"

for char in my_string:
    print(char)
```

Here's the output of the above code:

```
# Output:
I
L
L
I
N
I
```

You can access individual characters in a string using indexing, similar to lists.

```python
first_char = my_string[0]     # 'I'
last_char = my_string[-1]     # 'I'
```

### Slicing a String

You can extract a substring from a string using slicing.

```python
my_string = "ILLINI"
substring = my_string[1:4]
print(substring)  # Output: LLI
```

Remember that the start index is inclusive, while the end index is exclusive.
