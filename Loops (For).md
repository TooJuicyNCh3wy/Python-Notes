A count-controlled loop iterates a specific number of times. In Python, you use the for statement to write a count-controlled loop.

For loops in Python are used for iterating over a sequence (such as a list, tuple, dictionary, set, or string). The basic syntax is:
```
for element in sequence:
    # block of code to be executed for each element in the sequence
```
Example:
```
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

# Output:
# apple
# banana
# cherry
```
Python programmers commonly refer to the variable that is used in the for clause as the target variable because it is the target of an assignment at the beginning of each loop iteration. 

The values that appear in the list do not have to be a consecutively ordered series of numbers. For example, this code shown below, uses a for loop to display a list of odd numbers. There are five numbers in the list, so the loop iterates five times.
```
# This program also demonstrates a simple for
# loop that uses a list of numbers.

print('I will display the odd numbers 1 through 9.')
for num in [1, 3, 5, 7, 9]:
    print(num)
```
OUTPUT
```
I will display the odd numbers 1 through 9.
1
3
5
7
9
```
the code shown below, shows another example. In this program, the for loop iterates over a list of strings. Notice that in line 4 contains the 3 string 'winken', 'blinken', and 'nod'. As a reult, the loop iterates 3 times
```
for name in ['Winken', 'Blinken', 'Nod']
    print(name)
```
OUTPUT
```
Winken
Blinken
Nod
```
Using The Range Function with the ```For``` loop
=================================================
The loop above prints the name of each fruit in the fruits list.

For loops can also iterate over ranges, strings, and even dictionaries. Here are a few more examples:
```
# Iterating over a range of numbers
for i in range(1, 4):  # Will iterate from 1 to 3
    print(i)

# Iterating over a string
for char in "Hello":
    print(char)
```
Python provides a built-in function named range that simplifies the process of writing a count-controlled for loop. The range function creates a type of object known as an iterable. An iterable is an object that is similar to a list. It contains a sequence of values that can be iterated over with something like a loop. Here is an example of a for loop that uses the range function:
```
for num in range(5):
    print(num)
```
Notice instead of using a list of values, we call to the range function passing 5 as an argument. In this statement, the range function will generate an iterable sequence of integers in the range of 0 up to (but not including) 5. This code works the same as the following:
```
for num in [0,1,2,3,4}
    print(num)
```
As you can see, the list contains the list contains 5 numbers, so they loop will iterate 5x. The code below uses the range function with a for loop to display "Hello World" 5x
```
# This function demostrates how the range
# frunctiojn can be used with a for loop

# Print a message five times
for x in range(5):
    print('Hello World')
```
OUTPUT
```
Hello World
Hello World
Hello World
Hello World
Hello World
```
If you pass two arguments to the range function, the first argument is used as the starting value of the sequence, and the second argument is used as the ending limit. Here is an example:
```
for num in range(1, 5):
    print(num)
```
OUTPUT
```
1
2
3
4
```
By default, the range function produces a sequence of numbers that increase by 1 for each successive number in the list. If you pass a third argument to the range function, that argument is used as step value. Instead of increasing by 1, each successive number in the sequence will increase by the step value. Here is an example:
```
for num in range(1, 10,2):
    print(num)
```
in this for statement, three arguments are passed to the range function:
- The first argument, 1, is the starting value for the sequence.
- The second argument, 10, is the ending limit of the list. This means that the last number in the sequence will be 9.
- The third argument, 2, is the step value. This means that 2 will be added to each successive number in the sequence.
This code will display the following:
```
1
3
5
7
9
```

Using the Target Variable inside the loop
========================================
In a for loop, the purpose of the target variable is to reference each item in a sequence of items as the loop iterates. In many situations it is helpful to use the target variable in a calculation or other task within the body of the loop.

For example, suppose you need to write a program that displays the numbers 1 through 10 and their respective squares, in a table similar to the following:

1 = 1

2 = 4

3 = 9

4 = 16

5 = 25

6 = 36

7 = 49

8 = 64

9 = 81

10 = 100

This ca be accomplished by writing a for loop that iterates over the values 1 - 10. During the first iteration, the target variable will be assigned the value 1, during the first iteration, the target variable will be assigned the value 1, during the second iteration it will be assigned the value 2, and so forth. Because the target variable will reference the values one to ten during the loop's execution, you can use it in the calculation inside the loop

As Shown Below
```
print('Number\tSquare')
print('--------------')

for number in range(1, 11):
    square = number**2
    print(f'{number}\t{square}')
```
OUTPUT
```
Number    Square
------------------
1            1
2            4
3            9
4            16
5            25
6            36
7            49
8            64
9            81
10           100
```
Woah
Look at line 1
```
print('Number\tSquare')
```
Notice the ```\t``` command?
that command is like pressing the tab key, it causes the output cursor to move over the next tab position.This causes the space that you see between the words Number and Square in the sample output. 

The for loop that begins in line 11 uses the range function to produce a sequence containing the numbers 1 through 10. During the first iteration, number will reference 1, during the second iteration number will reference 2, and so forth, up to 10. Inside the loop, the statement in line 12 raises number to the power of 2 and assigns the result to the square variable. The statement in line 13 prints the value referenced by number, tabs over, then prints the value referenced by square. (Tabbing over with the \t escape sequence causes the numbers to be aligned in two columns in the output.)

