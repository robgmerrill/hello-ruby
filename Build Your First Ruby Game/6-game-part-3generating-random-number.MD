Code for game part 3 start: https://repl.it/@robgmerrill/Game-Part-3

# Random Number Generation

Let's return to our Guess the Number of Jelly Beans program. 

We've accomplished the following: 
* We will prompt player to enter their name. We will then print their name in a greeting.

```
puts "Welcome to 'Guess the Number of Jelly Beans'"
print "May I ask who is playing?"
name = gets.chomp
puts "Welcome, #{name} to the Great Jelly Bean Counter Competition!"
```

Now we are on to our next step:
* We are going to generate a random between 1 - 500 to be the total of jelly beans in a jar.

## rand method
Generating random numbers is going to be much easier than you might image in Ruby with the `rand` method.

Go ahead and open a new Ruby sandbox so we can practice this method.

Here it is in action:
`puts rand(500)` => `127`
`puts rand(500)` => `376`

Your outputs will vary from above because of the random value that is created.

This `rand` method will consistantly generate numbers between `0` and `499`. Because we know that `0` isn't going to be a guess we can instead do the following: 
`puts rand(500) + 1`

This will give us a value between `1` and `500`.

Perfect, we have all the skills we need for our next step. Go ahead and open the link to where your program is or you can follow along with this link: https://repl.it/@robgmerrill/Game-Part-3 

Here is what we want to do next:
```
puts "Welcome to Guess the Number of Jelly Beans!"
print "May I ask who is playing?"
name = gets
puts "Welcome, #{name} to the Great Jelly Bean Counter Competition!"

# Store a random number of Jelly Beans for user to guess
```

Let's create a variable called `total_jelly_beans` and assign it the value of `rand(500) + 1`.

```
...
# Store a random number of Jelly Beans for user to guess between 1 - 500
total_jelly_beans = rand(500) + 1
```

I always like to check my code to see that it is working as expected. So I would add a `puts total_jelly_beans` so we can track the random jelly beans being created as we build out our program.

```
...
# Store a random number of Jelly Beans for user to guess between 1 - 500
total_jelly_beans = rand(500) + 1
puts total_jelly_beans
```

When you run your game you should see output similar to this but replaced with the name you provide and the random number your program generates: 

```
Welcome to 'Guess the Number of Jelly Beans'
May I ask who is playing? Rob
Welcome, Rob to the Great Jelly Bean Counter Competition!
341
```

Now, let's go ahead and print two lines above our randomly generated number:
"This Jelly Bean jar contains between 1 - 500 jelly beans."
"Do you think you can guess it?"

```
...
# Store a random number of Jelly Beans for user to guess
puts "This Jelly Bean jar contains between 1 - 500 jelly beans."
puts "Do you think you can guess it?"
total_jelly_beans = rand(500) + 1
```

Your final output for this lesson should resemble:
```
Welcome to 'Guess the Number of Jelly Beans'
May I ask who is playing? Rob
Welcome, Rob to the Great Jelly Bean Counter Competition!
This Jelly Bean jar contains between 1 - 500 jelly beans.
Do you think you can guess it?
365
```

Great job! In this lesson we added the `rand` method to our Ruby syntax toolbelt. 

See you in the next lesson!


Final Code: 
```
# Jelly Bean Counter Game
# Dev Team: Rob

# print "Welcome to Guess the Number of Jelly Beans!"
# print "May I ask who is playing?"

puts "Welcome to 'Guess the Number of Jelly Beans'"
print "May I ask who is playing?"
name = gets.chomp
puts "Welcome, #{name} to the Great Jelly Bean Counter Competition!"

# Store a random number of Jelly Beans for user to guess between 1 - 500
puts "This Jelly Bean jar contains between 1 - 500 jelly beans."
puts "Do you think you can guess it?"
total_jelly_beans = rand(500) + 1
puts total_jelly_beans
```