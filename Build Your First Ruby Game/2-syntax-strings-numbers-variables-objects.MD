# Lesson Objectives: Strings, Debugging and Numbers

To complete this lesson head to: https://repl.it/@robgmerrill/stringsdebuggingnumbers


## Strings
Remember our "Hello Ruby" lesson?

We had the line `message = "Hello Ruby".

`"Hello Ruby"` is a string. As you could probably guess, a string represents text characters. 


Strings are great for holding information like emails, addresses, blog posts and a host of other possibilities! 

Looking at the lesson's sandbox. It is pre-poluted with the code `print "Rob Merrill"`

If we uncomment out that line (by removing the `#`) then run the code it prints out my name. That's not good! We want to print out your name. Go ahead and change the string `"Rob Merrill"` to your name. 

You might have guessed it already but the way to create a string is to add `""` quotes around text. These can be double quotes such as `"Rob Merrill"` or single quotes such as `'Rob Merrill'`.

There is a difference in single `''` and double `""` quotes we'll touch on later but for now they are both acceptable ways to create strings. 

The following code will provide the same output: 
```
# print "This string is the same."
# print 'This string is the same.'
```

Output: `This string is the same.`

<b>There is one thing to note as EXTREMELY important.</b> 

You can't mix `'` and `"` double quotes. 

Try printing out your name with mis-matching quotes:
`print 'Rob Merrill"`

When you do you will quickly discover that you get an error. 

`unterminated string meets end of file
print 'Rob Merrill"
                   ^`

The art of understanding why your code isn't working and fixing it is called debugging. It is probably one of the most valuable skills in programming. Sometimes you will receive helpful error messages that allow you to pinpoint the problem quickly. Sometimes error messages aren't as clear.

Our error message tells us that we have an `unterminated string...`

We can see what is happening. The Ruby interpreter sees an opening `'` single quote but doesn't see a closing `'` so it thinks we haven't terminated our string.

We'll run across plenty of errors in this course and practice solving these together. In the video's for each lesson I'll freaquently make mistakes that will provide error codes that we can debug together.


## Math

Let's look at doing math with Ruby. While some areas of the programming field involve you being a math wizard you can be assured that you can be a great Ruby developer without being an expert in math. We will want to make sure that we understand basic operations and comparisons. 

Addition, subtraction, division, multiplication and exponents should be very similar to what you learned through grade school. 

### Addition
Addition is accomplished as you might expect with the `+` operator
`print 2 + 3` => `5`

### Subtraction
Subtraction is accomplished as you might expect with the `-` operator
`print 2 - 1` => `1`

### Division
Division is accomplished with the `/` operator
`print 16 / 4` => `4`

### Multiplication
Multiplication is accomplished with the `*` operator
`print 10 * 10` => `100`

### Exponents
Exponents are accomplished with `**` operator. These might look a little unusual.
Here is an example of 10 squared:
`print 10**2` => `100`
Here is an example of 10 cubed (to the power of 3)
`print 10**3` => `1000`

Now, let take a look at some of the Ruby Comparison Operators for comparing values. A common term for a value that is being compared is an `operand`:

### Equal to
`==` checks if the value of two operands (the values we are comparing) are equal or not, if yes then the condition becomes `true`. If no then the condition becomes `false`.
`print 1 == 1` => `true`
`print 1 == 2` => `false`

### Not Equal to
`!=` checks if the value of two operands are equal or not, if values are not equal then condition becomes `true`. If the values are equal then the condition becomes `false`.
`print 1 != 1` => `false`
`print 1 != 2` => `true`

### Greater than
`>` checks if the value of the left operand is greater than the value of the right operand, if yes then the condition becomes true. If no then then the condition becomes false.
`print 1 > 1` => `false`
`print 1 > 0` => `true`

### Greater than or equal to
`>=`checks if the value of left operand is greater than or equal to the value of right operand, if yes then condition becomes true.
`print 1 > 1` => `false`
`print 1 >= 1` => `true`

### Less than
`<` checks if the value of left operand is less than the value of right operand, if yes then condition becomes true.
`print 1 < 1` => `false`
`print 1 < 2` => `true`

### Less than or equal to
`<=` checks if the value of left operand is less than or equal to the value of right operand, if yes then condition becomes true.
`print 1 < 1` => `false`
`print 1 <= 1` => `true`

Great work on the basics of handling math in Ruby. There is quite a bit more for us to learn in this area but this gives us all the tools we need for our first program!

