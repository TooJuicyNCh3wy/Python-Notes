If statements are used for conditional execution. They run a block of code if a specified condition is true. The basic syntax of an if statement in Python is:
```
if condition:
    # block of code to be executed if the condition is true
```
Here's a simple example:
```
age = 20
if age >= 18:
    print("You are an adult.")
```
This code will print "You are an adult." because the condition age >= 18 is true.

You can also add ```elif``` (else if) and else blocks to handle multiple conditions.
```
age = 20
if age < 18:
    print("You are a minor.")
elif age < 65:
    print("You are an adult.")
else:
    print("You are a senior.")
```
