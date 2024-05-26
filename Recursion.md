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
