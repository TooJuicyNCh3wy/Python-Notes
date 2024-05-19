A sentinel is a special value that marks the end of a sequence of values.

Consider the following scenario: You are designing a program that will use a loop to process a long sequence of values. At the time you are designing the program, you do not know the number of values that will be in the sequence. In fact, the number of values in the sequence could be different each time the program is executed. What is the best way to design such a loop? Here are some techniques that you have seen already in this chapter, along with the disadvantages of using them when processing a long list of values:

- Simply ask the user, at the end of each loop iteration, if there is another value to process. If the sequence of values is long, however, asking this question at the end of each loop iteration might make the program cumbersome for the user.
- Ask the user at the beginning of the program how many items are in the sequence. This might also inconvenience the user, however. If the sequence is very long, and the user does not know the number of items it contains, it will require the user to count them.

When processing a long sequence of values with a loop, perhaps a better technique is to use a sentinel. A sentinel is a special value that marks the end of a sequence of items. When a program reads the sentinel value, it knows it has reached the end of the sequence, so the loop terminates.

For example, suppose a doctor wants a program to calculate the average weight of all her patients. The program might work like this: A loop prompts the user to enter either a patient’s weight, or 0 if there are no more weights. When the program reads 0 as a weight, it interprets this as a signal that there are no more weights. The loop ends and the program displays the average weight.

A sentinel value must be distinctive enough that it will not be mistaken as a regular value in the sequence. In the example cited above, the doctor (or her medical assistant) enters 0 to signal the end of the sequence of weights. Because no patient’s weight will be 0, this is a good value to use as a sentinel.

Using a Sentinel
===============
The county tax office calculates the annual taxes on property using the following formula:

**Property tax = property value x 0.0065**

Every day, a clerk in the tax office gets a list of properties and has to calculate the tax for each property on the list. You have been asked to design a program that the clerk can use to perform these calculations.

In your interview with the tax clerk, you learn that each property is assigned a lot number, and all lot numbers are 1 or greater. You decide to write a loop that uses the number 0 as a sentinel value. During each loop iteration, the program will ask the clerk to enter either a property’s lot number, or 0 to end. 
shown down below
```
# This program displays property taxes. 
  
TAX_FACTOR = 0.0065 # Represents the tax factor. 
 
# Get the first lot number. 
print('Enter the property lot number or enter 0 to end.') 
lot = int(input('Lot number: ')) 
  
# Continue processing as long as the user 
# does not enter lot number 0. 
while lot != 0: 
    # Get the property value. 
    value = float(input('Enter the property value: ')) 
   
    # Calculate the property's tax. 
    tax = value * TAX_FACTOR 
   
    # Display the tax. 
    print(f'Property tax: ${tax:,.2f}') 
   
    # Get the next lot number. 
    print('Enter the next lot number or enter 0 to end.') 
 lot = int(input('Lot number: ')) 
```
