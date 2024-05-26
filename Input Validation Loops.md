 Input validation is the process of inspecting data that has been input to a program, to make sure it is valid before it is used in a computation. Input validation is commonly done with a loop that iterates as long as an input variable references bad data.

One of the most famous sayings among computer programmers is “garbage in, garbage out.” This saying, sometimes abbreviated as GIGO, refers to the fact that computers cannot tell the difference between good data and bad data. If a user provides bad data as input to a program, the program will process that bad data and, as a result, will produce bad data as output.
```
# This program displays gross pay. 
# Get the number of hours worked. 
hours = int(input('Enter the hours worked this week: ')) 
   
# Get the hourly pay rate. 
pay_rate = float(input('Enter the hourly pay rate: ')) 
   
# Calculate the gross pay. 
gross_pay = hours * pay_rate 
   
# Display the gross pay. 
print(f'Gross pay: ${gross_pay:,.2f}')
```
OUTPUT
```
Enter the hours worked this week: 400 [Enter]
Enter the hourly pay rate: 20 [Enter]
Gross pay: $8,000.00
```
Did you spot the bad data that was provided as input? The person receiving the paycheck will be pleasantly surprised, because in the sample run the payroll clerk entered 400 as the number of hours worked. The clerk probably meant to enter 40, because there are not 400 hours in a week. The computer, however, is unaware of this fact, and the program processed the bad data just as if it were good data. Can you think of other types of input that can be given to this program that will result in bad output? One example is a negative number entered for the hours worked; another is an invalid hourly pay rate.

Sometimes stories are reported in the news about computer errors that mistakenly cause people to be charged thousands of dollars for small purchases, or to receive large tax refunds to which they were not entitled. These “computer errors” are rarely caused by the computer, however; they are more commonly caused by bad data that was read into a program as input.

The integrity of a program’s output is only as good as the integrity of its input. For this reason, you should design your programs in such a way that bad input is never accepted. When input is given to a program, it should be inspected before it is processed. If the input is invalid, the program should discard it and prompt the user to enter the correct data. This process is known as input validation.

This shown below, shows a common technique for validating an item of input. In this technique, the input is read, then a loop is executed. If the input data is bad, the loop executes its block of statements. The loop displays an error message so the user will know that the input was invalid, and then it reads the new input. The loop repeats as long as the input is bad.

![Fig04-007](https://github.com/aalons012/Python-Notes/assets/75342059/60147f52-5b55-42be-b672-3e663b5dcfe7)

notice from the image above reads input in two places: 
- first just before the loop, and then
- inside the loop.
The first input operation—just before the loop—is called a priming read, and its purpose is to get the first input value that will be tested by the validation loop. If that value is invalid, the loop will perform subsequent input operations.

Let’s consider an example. Suppose you are designing a program that reads a test score and you want to make sure the user does not enter a value less than 0. The following code shows how you can use an input validation loop to reject any input value that is less than 0.
```
# Get a test score. 
score = int(input('Enter a test score: ')) 
   
# Make sure it is not less than 0. 
while score < 0: 
     print('ERROR: The score cannot be negative.') 
     score = int(input('Enter the correct score: '))
```
This code first prompts the user to enter a test score 

(this is the priming read)

then the ```while``` loop executes. Recall that the ```while``` loop is a pretest loop, which means it tests the expression ```score < 0``` before performing an iteration. If the user entered a valid test score, this expression will be false, and the loop will not iterate. If the test score is invalid, however, the expression will be true, and the loop’s block of statements will execute. The loop displays an error message and prompts the user to enter the correct test score. The loop will continue to iterate until the user enters a valid test score.

==============================================================================

**NOTE:** An input validation loop is sometimes called an error trap OR an error Handler

==============================================================================

This code rejects only negative test scores. What if you also want to reject any test scores that are greater than 100? You can modify the input validation loop so it uses a compound Boolean expression, as shown next.
```
# Get a test score. 
score = int(input('Enter a test score: ')) 
# Make sure it is not less than 0 or greater than 100. 
while score < 0 or score > 100: 
     print('ERROR: The score cannot be negative') 
     print('or greater than 100.') 
     score = int(input('Enter the correct score: '))
```
The loop in this code determines whether ```score``` is less than 0 or greater than 100. If either is true, an error message is displayed and the user is prompted to enter a correct score.
