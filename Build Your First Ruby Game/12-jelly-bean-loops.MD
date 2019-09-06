starter code: https://repl.it/@robgmerrill/Game-Part-7

# Jelly Bean Jar Loops
Alright, we are close to wrapping up our program. We just have a couple more closing steps:
Remaining Steps:
* Allow player to guess until they get it right or run out of turns.
* If a player takes more than 10 guesses we will tell them, "Sorry, you are out of guesses. The correct answer was [number of guesses] NO jelly beans for you!"

Somehow we need the program to: 
* update how many guesses a player has made for each guess attempt.
* create a variable that records whether the player has guessed a number set to boolean `false` then change to `true` if player has successfully guessed number. 
* run over and over again to a player has had 10 attempts and print a game over message if not successful or stop running once a player has made a correct guess. 

Here is the code we'll add to our already existing code base: 
```
# Track if player has guessed correctly
correct_guess = false
```
Put our logic within while loop if `number_of_guesses` is `true` and `correct_guess` is `!false` making it `true`:
```
while number_of_guesses < 10 && !correct_guess
    ...
    number_of_guesses = number_of_guesses + 1
    ...
end
```

Finally, after our while loop has been completed, if `!correct_guess` is `true we will print helpful player feedback:
```
if !correct_guess
    puts "Sorry, you didn't guess the number of Jelly Beans. It was #{total_jelly_beans}"
end
```

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

# Track if player has guessed correctly
correct_guess = false

while number_of_guesses < 10 && !correct_guess

    puts  "You have #{10 - number_of_guesses} guesses left."

    # Prompt user to make a guess
    puts "Please guess how many jelly beans are in the jar!"
    user_guess = gets.to_i

    number_of_guesses = number_of_guesses + 1

    # Compare `user_guess` to `total_jelly_beans`
    if user_guess < total_jelly_beans
        puts "Nope. That guess is too low!"
    elsif user_guess > total_jelly_beans
        puts "Nope, that guess is too high!"
    elsif user_guess == total_jelly_beans
        puts "Great job, #{name}!" 
        puts "You guessed the right amount of jelly beans and it only took you #{number_of_guesses} guesses, enjoy!"
        correct_guess = true
    end
end
if !correct_guess
    puts "Sorry, you didn't guess the number of Jelly Beans. It was #{total_jelly_beans}"
end
```



