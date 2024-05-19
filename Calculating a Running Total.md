A running total is a sum of numbers that accumulates with each iteration of a loop. The variable used to keep the running total is called an accumulator. 

Many programming tasks require you to calculate the total of a series of numbers. For example, suppose you are writing a program that calculates a business’s total sales for a week. The program would read the sales for each day as input and calculate the total of those numbers.

Programs that calculate the total of a series of numbers typically use two elements:
- A loop that reads each number in the series.
- A variable that accumulates the total of the numbers as they are read.

The variable that is used to accumulate the total of the numbers is called an accumulator. It is often said that the loop keeps a running total because it accumulates the total as it reads each number in the series

![Fig04-006](https://github.com/aalons012/Python-Notes/assets/75342059/f47311ab-9792-4078-b145-abbb00851254)

When the loop finishes, the accumulator will contain the total of the numbers that were read by the loop. Notice the first step in the flowchart is to set the accumulator variable to 0. This is a critical step. Each time the loop reads a number, it adds it to the accumulator. If the accumulator starts with any value other than 0, it will not contain the correct total when the loop finishes.

As shown below
Lets look at a program that calculates a running total.
```
# This program calculates the sum of a series
# of numbers entered by the user. 
MAX = 5

# The maximum number
# Initialize an accumulator variable.
total = 0.0

# Explain what we are doing.
print('This program calculates the sum of ', end='')
print(f'{MAX} numbers you will enter.')

# Get the numbers and accumulate them.
for counter in range(MAX):
  number = int(input('Enter a number: ')) \
  total = total + number

# Display the total of the numbers.
print(f'The total is {total}.')
```
OUTPUT

after adding the number for the ```input``` press [ENTER]
```
This program calculates the sum of 5 numbers you will enter.
Enter a number: 1 
Enter a number: 2
Enter a number: 3 
Enter a number: 4 
Enter a number: 5 
The total is 15.0.
```
The total variable, created by the assignment statement in line 7, is the accumulator. Notice it is initialized with the value 0.0. The for loop, in lines 14 through 16, does the work of getting the numbers from the user and calculating their total. Line 15 prompts the user to enter a number then assigns the input to the number variable. Then, the following statement in line 16 adds number to total:
```
total = total + number
```
After this statement executes, the value referenced by the number variable will be added to the value in the total variable. It’s important that you understand how this statement works. First, the interpreter gets the value of the expression on the right side of the = operator, which is total + number. Then, that value is assigned by the = operator to the total variable. The effect of the statement is that the value of the number variable is added to the total variable. When the loop finishes, the total variable will hold the sum of all the numbers that were added to it. This value is displayed in line 19.

The Augmented Assignment Operators
===================================

Quite often, programs have assignment statements in which the variable that is on the left side of the = operator also appears on the right side of the = operator. Here is an example:
```
x = x+1
```
On the right side of the assignment operator, 1 is added to x. The result is then assigned to x, replacing the value that x previously referenced. Effectively, this statement adds 1 to x. You saw another example of this type of statement in below:
```
total = total + number
```
This statement assigns the value of total + number to total. As mentioned before, the effect of this statement is that number is added to the value of total. Here is one more example:
```
balance = balance - Withdrawl
```
This statement assigns the value of the expression balance − withdrawal to balance. The effect of this statement is that withdrawal is subtracted from balance.

The table shown below shows other examples of statements written this way

(Assuming x = 6 in each statement)
```
Statement	  What It Does	  Value of x after the Statement
x = x + 4	  Add 4 to x	                        10

x = x − 3	  Subtracts 3 from x	                 3

x = x * 10	Multiplies x by 10	                60

x = x / 2	  Divides x by 2	                    3

x = x % 4	  Assigns the remainder of x / 4 to x	 2
```
As you can see, the augmented assignment operators do not require the programmer to type the variable name twice. The following statement:
```
total = total + number
```
could be rewritten as
```
total += number
```
Similarly, the statement
```
balance = balance − withdrawal
``` 
could be rewritten as
```
balance −= withdrawal
```

