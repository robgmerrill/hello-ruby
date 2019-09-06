We are going to build out the first part of our game. Let's refresh ourselves on what our goal is: 

* We will prompt player to enter their name. We will then print their name in a greeting.

To pull this off we are going to have to learn a few new things: The `puts` method, `gets` method and string interpolation.

Let's go ahead and open up a new Ruby playground. This is where we can start to build out our game. I'll provide the lesson's finished code at the bottom of this lesson if you need any assistance.

The first thing I would do is add some comments:
`# Jelly Bean Counter Game`
`# Dev Team: [your name]!`

Remember, Ruby is not going to interpret any code on the line after the `#`.

Here is a little mini-challenge. Try to print on two lines: 
`Welcome to 'Guess the Number of Jelly Beans'`
`May I ask who is playing?`

How'd it go?

Chances are you printed both of those sentences on one line instead of two by trying:
`print "Welcome to Guess the Number of Jelly Beans!"`
`print "May I ask who is playing?"`

We could fix that with the following:
`print "Welcome to 'Guess the Number of Jelly Beans'\n"`
`print "May I ask who is playing?"`

The `\n` is a special character that indicates a new line should occur after the print. However, there is another way that you may find more helpful: 

### puts method
The `puts` method will automatically create a new line. Go ahead and give this a shot: 
`puts "Welcome to 'Guess the Number of Jelly Beans'"`
`print "May I ask who is playing?"`

Great! Now we have to somehow collect the name that the user provides. We will create a variable called `name` to hold this value. 

### gets method
To accomplish this we will use the `gets` method. The `gets` method captures and stores a user's input to the terminal in our Ruby program. Calling the `gets` method captures the last thing the user typed into the terminal. Whevener your program makes a call to `gets`, it will freeze and wait for user input
`name = gets`

The return value of `gets` is the text typed into the terminal. So, setting a variable, `name`, euql to invoking the `gets` method sets that variable equal to the return value of `gets`.

One we store the return value of `gets` in a variable, we can treat the variable as we would any variable pointing to a string--interpolate with it, convert it to an integer, add it to an array...etc. 

If you want to see this in action you can now print `name` and see if it stored your name correctly.

`name = gets`
`print name`

Awesome! We next want to print out the users name in a greeting. Not just simply repeat it back to the user as we just did. 

Here is one way that we can do it:
`name = gets`
`puts "Welcome " + name`

This is a little bit clunky. We have to put an extra space in our `"welcome "` string then use the addition, `+`, operator to add the value of the variable `name`.

There is a smoother way! It takes a little more brain power at first but makes writing your code and reading your code much easier!

## String interpolation
Interpolation is a big word but don't let it confuse you. Just think of it as the substituting of a value. 

Whenever you include `#{}` inside of a double quoted string Ruby will use the value inside the curly braces. 

Remember when I mentioned there are differences between string with single and double quotes? This is a significant example of that:
`name = "Rob"`
`print 'Hello, #{name}` => `Hello, #{name}`
`print "Hello, #{name}` => `Hello, Rob`

Now that we equipped with this information we can finsih the first part of our project:
`name = gets`
`puts "Welcome, #{name}`

Go ahead and run the code and make sure it is working as you would expect!

Anything confusing? Take a look at the diagram below. I've written out the code and added comments to explain what everything is doing :) 

Finished Code:
```
# Jelly Bean Counter Game
# Dev Team: Rob

# print "Welcome to Guess the Number of Jelly Beans!"
# print "May I ask who is playing?"

# `puts` method will automatically create a new line at end of string
puts "Welcome to Guess the Number of Jelly Beans!"
puts "May I ask who is playing?"

# `gets` method 
name = gets

# print greeting with name
print "Welcome " + name

# use string interpolation to print greeting with name 
print "Welcome #{name}"
```


