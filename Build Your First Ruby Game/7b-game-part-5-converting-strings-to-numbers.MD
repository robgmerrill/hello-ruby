Game 5 starter code: https://repl.it/@robgmerrill/Game-Part-5

# Stings to Numbers
This should be a quick lesson before we move onto a more lengthy topic of conditionals. 

Let's take a look at our next step:

*  Have the player guess the total of jelly beans in the jar.

Let's begin by prompting a user to make a guess. 

```
...
# Number of guesses player has made
number_of_guesses = 0
guesses_left = 10 - number_of_guesses
puts  "You have #{guesses_left} guesses left."

# Prompt user to make a guess
puts "Please guess how many jelly beans are in the jar!"
```

Do you remember how we can capture user input? The `gets` method. We need to store the user input to a variable.

In this case we want that value to have a type of number. How do we do that?

Let's inspect the value type that we get when we get user input with the `gets` method.

We might try this:
```
...
# Prompt user to make a guess
puts "Please guess how many jelly beans are in the jar!"

user_guess = gets.chomp
p user_guess
```

However, if we look at the type of value if a player hits for example, `4`, on the keyboard we would see the following: `"4"`

This is a string of `"4"`. That may not seem like a problem now but we are going to build out our program in such a way that we want our logic to be based on number values and not string values. 

Our randomly generated jelly bean count will be between `1` and `500` so we need the `user_guess` to be a number as well for compaison.

## convert numbers to strings.
Fortunately, Ruby gives us a method, `to_i`, to make this happen.

Here is a quick glance to `to_i` in action:

```
"12345".to_i             #=> 12345
"99 red balloons".to_i   #=> 99
"0a".to_i                #=> 0
"0a".to_i(16)            #=> 10
"hello".to_i             #=> 0
"1100101".to_i(2)        #=> 101
"1100101".to_i(8)        #=> 294977
"1100101".to_i(10)       #=> 1100101
"1100101".to_i(16)       #=> 17826049
```

It looks like this is just the method we need to convert our user guess to an integer.

Let's rewrite our code using the `to_i` method: 

```
...
puts "You have #{10 - number_of_guesses} guesses left."

user_guess = gets.to_i
p user_guess
```

Now, if we hit `4` on the keyboard we will see that the output is `4` as well. This is all we need to compare it to the number of randomly generated jelly beans!


Alright, great job in this lesson. We've learned how to implement the `to_i` method to convert any string to a number!


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

user_guess = gets.to_i
p user_guess
```
