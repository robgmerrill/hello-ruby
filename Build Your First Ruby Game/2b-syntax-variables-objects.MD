Before we start our project we are going to spend one more lesson looking at Ruby syntax. Go ahead and open up this repl.it: https://repl.it/@robgmerrill/variablesobjects


## Variables
Variables are simply names that refer to values. Variables don't have types in Ruby. They can hold any value that you want! 

Remember our Hello Ruby lesson?
`message = "Hello Ruby"`
`message` is our variable, or name, that refers to the value `"Hello Ruby"`.

In some programming langauges you would have to declare variables. In JavaScript for example this would look like `var message = "Hello Ruby"` However, in Ruby, just the act of assigning a value creates them.

### Rules
There are some rules and best practices. A best practice in Ruby is that your variables will start with a lowercase letter and it may contain numbers and underscores `_`. 

While you may use numbers, they are rarely used and you should probably have a very good reason for using them.

Imagine you wanted to name a variable for pet type. While the name choice is up to you in Ruby I would do that as `pet_type = "cat"`. It is all lowercase letters and the two words are made human readable by adding the `_`. This naming style is often called "snake case".

Here is an exercise. Create a variable for the color of your house and assign it a value. 

As long as you don't break the rules for naming variables we discussed before there are a lot of ways you could choose to name variable. Here are a few examples: 

`house_color = "blue"`
`home_color = "blue"`
`color_of_home = "blue"`

There are some more nuances to naming variables but if you keep with all lowercase letters and `_` then you have all the tools you need for our project!

While variables may appear simple they are actually a superpower! We'll see how in our next lesson.

## Ruby's Most Well Known Secret
It won't take us long to discover that everything in Ruby is an object. There is an exception to that we will address later in the course. But for now you can assume that everything you run across strings, numbers booleans are actually objects.

What does that mean? It means that you are a more powerful Ruby developer than you even imagined.

Let's take a look at an example. Imagine we have a variable with a greeting of "Hi, neighbor."
`greeting = "Hi, neighbor."`

The object, in this case our variable `greeting` that refers the the string `Hi, neighbor."` is what we call the receiver. This is the object that we are going to call the method on. Method is just another word for function when attached to an object. 

Remember, a function is just a word for code that does something for you. `print` is a Ruby function that ouputs a value we provide.

To call our method we need to use a dot operator `.` and then name our method. Let's take a look at the `upcase` method.
`print greeting = "Hi, neighbor."` => `Hi, neighbor.`
`print greeting.upcase` => `HI, NEIGHBOR.`

Powerful, right?

Here is another demonstration of a built in method you can use on numbers: `even?`
`number = 42`
`print number.even?` => `true`
`print number.even?` => `false`

Remember, we have our object which is the receiver of the method and we attach the two with the dot operator.

You might be thinking that it isn't helpful that the teacher knows the methods available on and object and you don't! You are right, I shouldn't keep that to myself. You could look up the documentation but you can also do this little trick. 
```
print 42.methods
print "hi".methods
```

This will allow you to see all the methods available on a number, such as `42` and the methods available on a string, such as `"hi"`.

Those are a lot of methods, right?!!

Some will be really helpful while some you may find yourself never using. 

Don't worry about knowing them all right now :)  

Finished Code: 
```
# `message = "Hello Ruby"`

# rules for Ruby variable names
  # start with lowercase letter
  # may contain letters, underscores and numbers

# best practice
  # all lowercase letters and separate words with underscores: snake_case 
  # while numbers are acceptable they are not commonly used 

# example - suppose we want to create a variable that tracks whether a value is a dog, cat
  # pet_type 

# exercise 
  # Create a variable for the color of your house and assign it a value


# Ruby objects
# greeting = "Hi, neighbor."
# call `.upcase` on `greeting` and print `greeting`

# number = 42
# call `.even?` on `number` and print 

# uncomment out the following line to see methods available to strings
# print "hi".methods

# uncomment out the following line to see methods available to numbers
# print 42.methods
```



