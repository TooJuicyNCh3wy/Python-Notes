A recursive function is a function that calls itself.

You have seen instances of functions calling other functions. In a program, the main function might call function A, which then might call function B. It’s also possible for a function to call itself. A function that calls itself is known as a recursive function.

As the code shown below:
```
def main(): 
    message() 
   
def message(): 
    print('This is a recursive function.') 
    message() 
   
# Call the main function. 
if __name__ == '__main__': 
     main()

OUTPUT:

This is a recursive function.
This is a recursive function.
This is a recursive function.
This is a recursive function.
  
     . . . and this output repeats forever!
```
The message function displays the string ’This is a recursive function’ and then calls itself. Each time it calls itself, the cycle is repeated. Can you see a problem with the function? There’s no way to stop the recursive calls. This function is like an infinite loop because there is no code to stop it from repeating. If you run this program, you will have to press Ctrl+C on the keyboard to interrupt its execution.

Like a loop, a recursive function must have some way to control the number of times it repeats.In this program, the message function receives an argument that specifies the number of times the function should display the message.
```
def main(): 
    # By passing the argument 5 to the message 
    # function we are telling it to display the 
    # message five times. 
    message(5) 
   
def message(times): 
    if times > 0: 
        print('This is a recursive function.') 
        message(times − 1) 
   
# Call the main function. 
if __name__ == '__main__': 
     main()

OUTPUT:

This is a recursive function.
This is a recursive function.
This is a recursive function.
This is a recursive function.
This is a recursive function.
```
Problem Solveing with Recursion
=================================
A problem can be solved with recursion if it can be broken down into smaller problems that are identical in structure to the overall problem.

Using Recursion to Calculate tyhe Factorial of a number
========================================================
Let’s take an example from mathematics to examine an application of recursive functions. In mathematics, the notation n! represents the factorial of the number n. The factorial of a nonnegative number can be defined by the following rules:
```
If n=0 then    n! = 1
If n>0 then    n! = 1 × 2 × 3 × … × n
```
Let’s replace the notation n! with factorial(n), which looks a bit more like computer code, and rewrite these rules as follows:
```
if n = 0 then    Factorial(n) = 1
if n > 0 then    factorial(n) = 1 x 2 x 3 x ... x n
```
These rules state that when n is 0, its factorial is 1. When n is greater than 0, its factorial is the product of all the positive integers from 1 up to n. 

For instance, factorial(6) is calculated as  1×2×3×4×5×6.


When designing a recursive algorithm to calculate the factorial of any number, first we identify the base case, which is the part of the calculation that we can solve without recursion. That is the case where n is equal to 0 as follows:
```
if n = 0 then     factorial(n) = 1
```
This tells us how to solve the problem when n is equal to 0, but what do we do when n is greater than 0? That is the recursive case, or the part of the problem that we use recursion to solve. This is how we express it:
```
If n > 0 then     factorial(n) = n x factorial(n - 1)
```
This states that if n is greater than 0, the factorial of n is n times the factorial of n − 1. Notice how the recursive call works on a reduced version of the problem, n − 1. So, our recursive rule for calculating the factorial of a number might look like this:
```
if n = 0 then   factorial(n) = 1
if n > 0 then   factorial(n) = n x factorial(n - 1) 
```
The program below shows how we might design a factorial function in a program.
```
def main(): 
    # Get a number from the user. 
    number = int(input('Enter a nonnegative integer: ')) 
   
    # Get the factorial of the number. 
    fact = factorial(number) 
   
    # Display the factorial. 
    print(f'The factorial of {number} is {fact}.') 
   
# The factorial function uses recursion to 
# calculate the factorial of its argument, 
# which is assumed to be nonnegative.  
def factorial(num): 
    if num == 0: 
        return 1 
    else: 
        return num * factorial(num − 1) 
   
# Call the main function. 
if __name__ == '__ main__':  
     main()

OUTPUT:

Enter a nonnegative integer: 4 [Enter]
The factorial of 4 is 24.

```
In the sample run of the program, the factorial function is called with the argument 4 passed to num. Because num is not equal to 0, the if statement’s else clause executes the following statement:

```
return num * factorial(num − 1) 
```
Although this is a return statement, it does not immediately return. Before the return value can be determined, the value of factorial(num − 1) must be determined. The factorial function is called recursively until the fifth call, in which the num parameter will be set to zero
