A function is a piece of prewritten code that performs an operation. 
Python has numerous built-in functions that perform various operations. 
Perhaps the most fundamental built-in function is the print function, which displays output on the screen. 
Here is an example of a statement that executes the print function:
```
print('Hello World')
```
In interactive world if you type this statement and press ```enter``` key, the message ```Hello World``` is Displayed.
Heres the Example: vvv
```
>>> print('Hello World')
Hello World
```
When Programmers excute a function, they say that they are "calling the function".
When you call the ```print```. Followed by a set of parentheses. Inside the parentheses, you type an ARGUMENT, 
which is data that you want displayed on the screen. 
In the previous example, the argument is ``` 'Hello World' ```. Notice the quote marks are not displayed when the statement ecxecutes. 
The Quote marks simply specify the beginning and the end of the text that you wish to display
Suppose your instructor tells you to write a program that displays your name and address on the computer screen. The Example (shown below) shows an example of such a program, with the output that it will prodice when it runs.
vvv
(output.py)
```
print('Andy Alonso')
print('123 Your moms house place')
print('Miami, FL 22269')
```
PROGRAM OUTPUT:
```
Andy Alonso
123 Your moms house place
Miami, FL 22269
```
Strings and String Literals 
============================
These pieces of data are sequences of characters. in programming terms, a sequence of characters that is used as data is called a string. When a string appears in the actual code of a program, it is called a string literal. In Python code, string literals must be enclosed in quote marks. As mentioned earlier, the quote marks simply mark where the string data begins and ends.

In Python, you can enclose string literals in a set of single-quote marks (') or a set of double-quote marks ("). The string literals in ```Displaying Output with the print Function``` are enclosed on single quotes, but the program can also be written as shown below
vvvv
```
print("Andy Alonso")
print("123 Your moms House Place")
print("Miami, FL 22269")
```
If you want a string literal to contain either a single-quote or an apostrophe as part of the string, you can enclose the string literal in double-quote marks.
```
print("Don't Fear Genesis!")
print("Andy's Here")
```
Likewise, you can use single-quote marks to enclose a string literal that contains double-quotes as part of the string.
```
print('Your assignment is to read "Hamlet" by tomorrow.')
```
Python also allows you to enclose string literals in triple quotes (either """ or '''). 

Triple-quoted strings can contain both single quotes and double quotes as part of the string. The following statement shows an example:
```
print("""I'm reading "Hamlet" tonight.""")
```
Triple quotes can also be used to surround multiline strings, something for which single and double quotes cannot be used. Here is an example:
```
print("""One
Two
Three""")
```
OUTPUT
```
One
Two
Three
```
