How to Create a Variable in Python
Variables in Python are like labels that you attach to values. They allow you to store and manipulate data in your programs. Creating a variable in Python is straightforward; you just assign a value to a name without needing to declare its type explicitly.

```
my_number = 10
my_name = "Faizan"
```

In this example, ```my_number```is a variable that holds the value 10, and ```my_name``` is another variable that holds the value "Faizan". Python understands the type of variable based on the value assigned to it.

Variables can also store different types of data. You can also change the value of a variable after it's been created.
```
# Changing the value
my_number = 10
my_number = 20
print(my_number)  # Output: 20

# Using the variable in operations
my_number = my_number + 5
print(my_number)  # Output: 25
```

Creating Variables with Assignment Statements
==============================================
You use an assignment statement to create a variable and make it reference a piece of data. Here is an example of an assignment statement:
```
age = 25
``` 
After this statement executes, a variable named age will be created, and it will reference the value 25. 

An assignment statement is written in the following general format:
```
variable = expression
```
The equal sign (=) is known as the assignment operator. In the general format, variable is the name of a variable and expression is a value, or any piece of code that results in a value. After an assignment statement executes, the variable listed on the left side of the = operator will reference the value given on the right side of the = operator.

To experiment with variables, you can type assignment statements in interactive mode, as shown here:
```
>>> width = 10 
>>> length = 5 
>>>
``` 
The first statement creates a variable named width and assigns it the value 10. The second statement creates a variable named length and assigns it the value 5. Next, you can use the print function to display the values referenced by these variables, as shown here:
```
>>> print(width) 
10 
>>> print(length) 
5 
>>>
``` 
When you pass a variable as an argument to the print function, you do not enclose the variable name in quote marks. To demonstrate why, look at the following interactive session:
```
>>> print('width') 
width 
>>> print(width) 
10 
>>>
``` 
In the first statement, we passed 'width' as an argument to the print function, and the function printed the string width. In the second statement, we passed width (with no quote marks) as an argument to the print function, and the function displayed the value referenced by the width variable.

In an assignment statement, the variable that is receiving the assignment must appear on the left side of the = operator. As shown in the following interactive session, an error occurs if the item on the left side of the = operator is not a variable:
```
>>> 25 = age
SyntaxError: can't assign to literal
>>>
```
Multiple Variable Assignment
============================
In Python you can assign values to multiple variables in a single statement. Such a statement is known as a multiple assignment statement. Here is an example:
```
x, y, z = 0, 1, 2 
```
In the statement, three variable names are shown on the left side of the = operator, separated by commas. On the right side of the = operator, three values appear, also separated by commas. When the statement executes, the variables on the left side of the = operator will be assigned their respective values shown on the right side of the = operator. In this example, x will be assigned 0, y will be assigned 1, and z will be assigned 2.

Here is another example:
```
name, id = 'Trinidad', 847
```
After this statement executes, the name variable will be assigned 'Trinidad' and the id variable will be assigned the value 847.

Variable Naming Rules
======================
Although you are allowed to make up your own names for variables, you must follow these rules:

- You cannot use one of Python’s keywords as a variable name.
- A variable name cannot contain spaces.
- The first character must be one of the letters a through z, A through Z, or an underscore character (_).
- After the first character you may use the letters a through z or A through Z, the digits 0 through 9, or underscores.
- Uppercase and lowercase characters are distinct. This means the variable name ```ItemsOrdered``` is not the same as ```itemsordered```.

In addition to following these rules, you should always choose names for your variables that give an indication of what they are used for. For example, a variable that holds the temperature might be named ```temperature```, and a variable that holds a car’s speed might be named ```speed```. You may be tempted to give variables names such as ```x``` and ```b2```, but names like these give no clue as to what the variable’s purpose is.

Because a variable’s name should reflect the variable’s purpose, programmers often find themselves creating names that are made of multiple words. For example, consider the following variable names:
```
grosspay 
payrate 
hotdogssoldtoday
```
Unfortunately, these names are not easily read by the human eye because the words aren’t separated. Because we can’t have spaces in variable names, we need to find another way to separate the words in a multiword variable name and make it more readable to the human eye.

One way to do this is to use the underscore character to represent a space. For example, the following variable names are easier to read than those previously shown:
```
gross_pay 
pay_rate 
hot_dogs_sold_today 
```
This style of naming variables is popular among Python programmers, and is the style we will use in this book. There are other popular styles, however, such as the camelCase naming convention. camelCase names are written in the following manner:

- The variable name begins with lowercase letters.
- The first character of the second and subsequent words is written in uppercase.



For example, the following variable names are written in camelCase:
```
grossPay 
payRate 
hotDogsSoldToday
```
