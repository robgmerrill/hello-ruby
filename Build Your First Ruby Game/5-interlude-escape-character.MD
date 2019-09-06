# Escape Sequences in strings

I thought we should pause real quick and talk about the escape character, `\`, in Ruby. 

We've seen a few times in this course already how to indicate we want a new line using `\n`. 

When we use the `\` character what follows it is an escape sequence. It means that the characters won't be represented in our code but are doing something special for us. 

Just like how `"What is under\n the car"` outputs:
```
What is under
the car
```
 Not: `What is under\n the car`

Go ahead and open a new Ruby coding playground. Let's run the following code: 
`puts "First line of code\nSecond line of code\nThird line of code`

This gives us an output of:
```
First line of code
Second line of code
Third line of code
```

We have already covered this. Let's look at another example. This is where we can build in tabs with `\n`.
`puts "First line of code\tSecond line of code\tThird line of code`

This gives us an output of: 
```
First line of code
    Second line of code
    Third line of code
```

Now, let's look at an extremely helpful use of the escape character `\`.

`print "Mary said, "Good to see you.""`

If we run this code we get an error. 
`syntax error, unexpected tCONSTANT, expecting end-of-input
print "Mary said, "Good to see you.""`

Your print function sees `"Mary said, "` between quotes indicating this is a string but then it sees the characters `Good to see you.` that are not between single or double quotes and so our code breaks.

We unintentionally ended our string when we intended to add a quote `"Good to see you."` within our string. 


There are two ways that we can fix this. We could replace the outer `""` with `''`:
`print 'Mary said, "Good to see you."'`

This works because after Ruby sees the first `'` it waits to see a second `'` and everything between those two single quotes are interpreted as text.

## Single quotes `'` and string interpolation

However, this would be a problem if we wanted to use string interpolation. Try this code in your online sandbox: 
```
name = "Mary"
print '#{name} said, "Good to see you."'
```

The output is: 
`'#{name} said, "Good to see you."'`

Our ouptut includes `#{name}` instead of the value of `name`. String interpolation does not work within single quotes. They must be double. 

So how do we fix this? If we are in a scenario where we have to use double quotes `"` to surround our text for string interpolation but we also have text with double quotes in it.

You might have guessed it. The escape character: 
```
name = "Mary"
print "#{name} said, \"Good to see you.\""
```

Success! The `\` character tells Ruby not to interpret the double quotes in `"Good to see you."` to be interpreted as the start or end of a string but to be interpreted as text.

Alright, great job! 

