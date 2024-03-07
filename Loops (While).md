While loops in Python repeat as long as a certain boolean condition is met. Here’s the basic syntax:
```
while condition:
    # block of code to be executed as long as the condition is true
```
Example:
```
i = 1
while i <= 5:
    print(i)
    i += 1
```
The loop above prints the numbers from 1 to 5.

While loops can be used for repeated actions until a condition is no longer true. You can also use break to exit a loop early.
```
# Using break to exit a loop
i = 1
while True:
    print(i)
    if i == 5:
        break  # Exits the loop
    i += 1
```
