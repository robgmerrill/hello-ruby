As we continue building out your project feel free to continue to work with the Ruby environment you created or you can follow this link to make sure you are running the same code I am to start this lesson: https://repl.it/@robgmerrill/Game-Part-2

# `inspect` and `chomp` methods
In this lesson I want to introduce you to a little problem that is in our code. 

`name = gets`
`puts "Welcome, #{name}`

Let's add some more information to our greeting. Let's create a message that says, "Welcome [name] to the great Jelly Bean Counter Competition!"

Did you see what happened? Everything after the user's name was moved to the next line. 

```
Welcome Rob
 to the great Jelly Bean Counter Competition!
```

Why is that?

You could read those two lines of code a hundred times and not get any closer to figuring out what happened. 

Luckily, we have a tool in Ruby that lets us take a look at an object in a way that doesn't normally show up in the program output. 

## inspect method
The `inspect` method will convert any object to a string representation that is helpful for debugging.

It helps us to debug by revealing details of the object that don't normally appear in the program's output. Currently, we see the output on two different lines and don't have any indicators why this action, which is actually normal Ruby behavior, is occuring.

Let's test it out. Underneath the code where you have your `gets` method storing value to variable `name` add a line where you `inspect` this variable:
```
...
name = gets
puts name.inspect
...
```

This outputs `"Rob\n"`

That's it! We have run into this `\n` when we looked at the different between `print` and `puts`. It creates a new line. 

This is why our output is showing up on two lines. After our value for name we have a new line created so the following text moves to the next line. When the user initially submits their name it gets captured with an extra newline character.

Because using `inspect` is so common in debugging Ruby makes the process easier for us. We can simply replace `puts` with `p` and drop `inspect` to accomplish the same thing. 

Go ahead and try it out for youself and see: 
```
...
name = gets
p name
...
```

When you do the results should be the same. You should see your name with the newline character `\n`.

Now that we know the reason for this occuring let's go ahead and remove the `p name` or `puts name.inspect`.

We should be clear. This isn't a bug in Ruby. It is a way that Ruby works. Things become bugs in a developers program when they aren't clear how a language works. This `inspect` method helped us in this example to see what Ruby is doing.

So what is the solution? How do we fix our code?

## `chomp method`
The `chomp` method actually looks for the newline character and will remove it. You can think of pacman but instead of chomping on dots the `chomp` method eats the newline `\n` character if it is the last character of a string.

So let's try our code again with our new method:
```
...
name = gets.chomp
puts "Welcome, #{name} to the great Jelly Bean Counter Competition!"
```

We should successfuly see that our output is now on one line.

Great job! In this lesson we got to sharpen our debugging skills with the `inspect` method that we can shorten by just using `p` and we learned how to remove trailing newline characters `\n` with the `chomp` method.

We'll see you in the next lesson where we learn how to generate a random number!

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
name = gets.chomp

# print greeting with name
# print "Welcome " + name

# use string interpolation to print greeting with name 
# print "Welcome #{name}"

# use string interpolation to print greeting that says, "Welcome, [name] to the great Jelly Bean Counter Competition!"
print "Welcome #{name} to the great Jelly Bean Counter Competition!"
```