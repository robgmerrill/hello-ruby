starter code: https://repl.it/@robgmerrill/Game-Part-6

# Jelly Bean Conditionals

Let's go ahead and look at the requirements we have accomplished so far:

* We will prompt player to enter their name. We will then print their name in a greeting.
* We are going to generate a random between 1 - 500 to be the toal of jelly beans in a jar.
* We want to let the player know how many guesses they have already made before each turn. We will give them a total 10 guesses.
*  Have the player guess the total of jelly beans in the jar.

In this lesson we are going to learn how to respond when a player guesses too high, too low or runs out of guesses. To accomplish the following steps we are going to need to learn about conditionals.




Our game so far: 
```
puts "Welcome to Guess the Number of Jelly Beans!"
puts "May I ask who is playing?"
name = gets.chomp
puts "Welcome, #{name} to the Great Jelly Bean Counter Competition!"

# Store a random number of Jelly Beans for user to guess
puts "This Jelly Bean jar contains between 1 - 500 jelly beans."
puts "Do you think you can guess it?"
total_jelly_beans = rand(500) + 1

# Number of guesses player has made
number_of_guesses = 0
guesses_left = 10 - number_of_guesses
puts  "You have #{guesses_left} guesses left."

# Prompt user to make a guess
puts "Please guess how many jelly beans are in the jar!"
user_guess = gets.to_i
```

Now, we want to implement the following steps: 

*  When a player guesses a number too low we will print a message that says, "Nope. That guess is too low!" When a player guesses a number too high we will print a message that says, "Nope, that guess is too high!"
* For a correct guess we will tell them, "Great job, [name]! You guessed the right amount of jelly beans and it only took you [number of guesses] guesses, enjoy!"

We'll begin by comparing the `user_guess` to the `total_jelly_beans` and build in the logic to accomplish our program goals listed above:
```
# Compare `user_guess` to `total_jelly_beans`
if user_guess < total_jelly_beans
    puts "Nope. That guess is too low!"
elsif user_guess > total_jelly_beans
    puts "Nope, that guess is too high!"
elsif user_guess == total_jelly_beans
    puts "Great job, #{name}!" 
    puts "You guessed the right amount of jelly beans and it only took you #{number_of_guesses} guesses, enjoy!"
end
```


Let's go ahead and run our code and see if it works! Underneath the line `total_jelly_beans = rand(500) + 1` be sure to add a `puts total_jelly_beans`. That way you know the total of the random jelly bean number so you can test putting in user guess values below, equal and above to the correct number of jelly beans in the jar. 

```
puts "Welcome to Guess the Number of Jelly Beans!"
puts "May I ask who is playing?"
name = gets.chomp
puts "Welcome, #{name} to the great Jelly Bean Counter Competition!"

# Store a random number of Jelly Beans for user to guess
puts "This Jelly Bean jar contains between 1 - 500 jelly beans."
puts "Do you think you can guess it?"
total_jelly_beans = rand(500) + 1
puts total_jelly_beans

# Number of guesses player has made
number_of_guesses = 0
guesses_left = 10 - number_of_guesses
puts  "You have #{guesses_left} guesses left."

# Prompt user to make a guess
puts "Please guess how many jelly beans are in the jar!"
user_guess = gets.to_i

# Compare `user_guess` to `total_jelly_beans`
if user_guess < total_jelly_beans
    puts "Nope. That guess is too low!"
elsif user_guess > total_jelly_beans
    puts "Nope, that guess is too high!"
elsif user_guess == total_jelly_beans
    puts "Great job, #{name}!" 
    puts "You guessed the right amount of jelly beans and it only took you #{number_of_guesses} guesses, enjoy!"
end
```

Hopefully, your code is working as you would expect for one round! But you probably recognize a huge problem. The game is only one round! 

We need to change our code to achieve the following steps:
* Allow player to guess until they get it right or run out of turns.
* If a player takes more than 10 guesses we will tell them, "Sorry, you are out of guesses. The correct answer was [number of guesses] NO jelly beans for you!"


The player should get 10 guesses not one. Somehow we need the program to: 
* track how many guesses a player has made.
* run over and over again to a player has had 10 attempts and print a game over message if not successful or stop running once a player has made a correct guess. 

This sounds like a perfect example of when we want to use loops in Ruby!

