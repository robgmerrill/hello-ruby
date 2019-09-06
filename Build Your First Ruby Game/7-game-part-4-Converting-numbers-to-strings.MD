starter code: https://repl.it/@robgmerrill/Game-Part-4

# How to Convert Numbers to Strings

If Ruby is your first programming language you have probably never thought to yourself, "How do I convert a number I am thinking of to a string in this paper I am writing?"

As a Ruby developer this is a question that we will need to figure out. Fortunately, Ruby has a built in message to help us with this!

First, let's look at what we have accomplished so far:

* We will prompt player to enter their name. We will then print their name in a greeting.
* We are going to generate a random between 1 - 500 to be the toal of jelly beans in a jar.

We have accomplished this with the following code: 

```
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

In this lesson we are going to accomplish this next step:

* We want to let the player know how many guesses they have already made before each turn. We will give them a total 10 guesses.

First, we want to create a variable that tracks the number of user guesses, `number_of_guesses`. We will initially set it to a value of `0`.

We will then create a variable `guesses_left` set to the value of `10` - `number_of_guesses`:
```
...
# Store a random number of Jelly Beans for user to guess between 1 - 500
puts "This Jelly Bean jar contains between 1 - 500 jelly beans."
puts "Do you think you can guess it?"
total_jelly_beans = rand(500) + 1
puts total_jelly_beans

# number of guesses player has made
number_of_guesses = 0
# number of guesses a player has left
```

Now, let's go ahead and give the player some feedback. We want to communicate the message that "You have [number of guesses] guesses left."

Now, there are a couple of ways that we can accomplish this. The first would require converting the `guesses_left` to a string value. 

Let's look at what happens if we don't convert our number to a string:

```
...
# Number of guesses player has made
number_of_guesses = 0
guesses_left = 10 - number_of_guesses
puts "You have  + guesses_left + " guesses left."
```

We get an error message: 
`syntax error, unexpected tIDENTIFIER, expecting end-of-input
puts "You have " + guesses_left + " guesses left."`

The reason for this is because the `+` operator is used to add numbers as well as to concatenate strings, and since `guesses_left` contains a number, this `+` looks like an attempt to add numbers.

## to_s method
To solve this we will need to convert our number assigned to `guesses_left` to a string. We can do this with the `to_s` method.

So let's give this a shot again: 
```
...
# Number of guesses player has made
number_of_guesses = 0
guesses_left = 10 - number_of_guesses
puts "You have "  + guesses_left.to_s + " guesses left."
```

Great! Your output should be similar to mine except for the name you provided:
```
Welcome to Guess the Number of Jelly Beans!
May I ask who is playing?
Welcome, Rob to the great Jelly Bean Counter Competition!
This Jelly Bean jar contains between 1 - 500 jelly beans.
Do you think you can guess it?
10 guesses left.
```

Using the `to_s` method is a great way to accomplish this. There is another straightforward way that we've already learned. Can you remember it?

<b>String interpolation!</b>

In fact, if we use string interpolation we dont need to have `guesses_left = 10 - number_of_guesses`. We can just subtract `number_of_guesses` from `10` while doing string interpolation. Take a look below: 

```
# Number of guesses player has made
number_of_guesses = 0
puts  "You have #{10 - guesses_left} guesses left."
```

Remember, when we use `#{...}` Ruby will interpret the values between the `{}` and display it within a string. It saves us the hassle of worrying what type of value is saved to a variable so the `to_s` method isn't needed. 

Great job! In this lesson we have learned why and how to convert a number to a string. 

We've also seen another great opportunity to use string interpolation.

Ok, that wraps up this lesson. In our next lesson we are going to learn what to do if our player guesses too low or too high!


Finished Code:
```
# our game so far
puts "Welcome to 'Guess the Number of Jelly Beans'"
print "May I ask who is playing?"
name = gets.chomp
puts "Welcome, #{name} to the Great Jelly Bean Counter Competition!"

# Store a random number of Jelly Beans for user to guess between 1 - 500
puts "This Jelly Bean jar contains between 1 - 500 jelly beans."
puts "Do you think you can guess it?"
total_jelly_beans = rand(500) + 1
puts total_jelly_beans

# number of guesses player has made
number_of_guesses = 0
# number of guesses a player has left
# guesses_left = 10 - number_of_guesses

puts "You have #{10 - number_of_guesses} guesses left."
```