Functions in Python are blocks of code that only run when they are called. They can accept parameters and can return data as a result. To define a function, use the def keyword:
```
def greet(name):
    print(f"Hello, {name}!")
```
You can call the function by using its name followed by parentheses:
```
greet("Faizan")  # Output: Hello, Faizan!
```
Functions can be as simple or as complex as needed, and they are a great way to organize and reuse code.

Functions can also return values and can be used to execute blocks of code with different arguments.
```
# A function that returns a value
def add_numbers(a, b):
    return a + b

result = add_numbers(5, 3)
print(result)  # Output: 8

# Using a function with a variable number of arguments
def print_names(*names):
    for name in names:
        print(name)

print_names("Faizan", "Yasin", "John")

# Output:
# Faizan
# Yasin 
# John
```
