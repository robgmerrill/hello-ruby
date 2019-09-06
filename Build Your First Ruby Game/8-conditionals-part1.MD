# Conditionals

Let's go ahead and look at the requirements we have accomplished so far:

* We will prompt player to enter their name. We will then print their name in a greeting.
* We are going to generate a random between 1 - 500 to be the toal of jelly beans in a jar.
* We want to let the player know how many guesses they have already made before each turn. We will give them a total 10 guesses.
*  Have the player guess the total of jelly beans in the jar.

In the next part of our project we are going to learn how to respond when a player guesses too high, too low or runs out of guesses. To accomplish the following steps we are going to need to learn about conditionals.

*  When a player guesses a number too low we will print a message that says, "Nope. That guess is too low!" When a player guesses a number too high we will print a message that says, "Nope, that guess is too high!"
* Allow player to guess until they get it right or run out of turns.
* For a correct guess we will tell them, "Great job, [name]! You guessed the right amount of jelly beans and it only took you [number of guesses], enjoy!"
* If a player takes more than 10 guesses we will tell them, "Sorry, you are out of guesses. The correct answer was [number of guesses] NO jelly beans for you!"

The syntax we will learn is something called conditionals. We use conditionals all the time in real life. 

Open up the following link to look at two scenarios involving the weather the we can program with conditionals: https://repl.it/@robgmerrill/Conditionals-Part-1

Depending on the weather we might think to ourselves, "If the weather is nice I will wear shorts today. Or else, I will wear pants."

Notice those two key words in that sentence `if` and `else`. Here is what this might look like in code:
```
temperature = 70
if temperature >= 70
    puts "I will wear shorts today."
else
    puts "I will wear pants today."
end
```

Notice the specifics of the syntax. An `if`/`else` statement must include an `end` keyword for Ruby to run your code. If you leave out the `end` keyword you will get a syntax error.

Notice what happens when you run your code. We get the output `I will wear shorts today.`

Try changing `temperature` to `69`. When you run your code the output will now be `I will wear pants today.`

However, the temperature can vary quite a bit and you might want to build in more options than just `if`/`else`.

Go ahead and clear out or comment out all the code and let's look at another scenario:

We might think to ourselves, "If the weather is less than 70 degrees I'm wearing pants and a sweater. If the weather is 70 degrees I'll weal pants and a shirt. If it is 80 degrees I'll wear shorts and a shirt and finally if it is hotter than 90 degrees I'll put on my swimsuit and go swimming."

We have special Ruby syntax to check for multiple conditions between `if` and `else` called `elsif`. 

Clever right? It's just a combination of both words. Here is what the above situation might look like in code: 

```
temperature = 70
if temperature >= 90
    puts "I am putting on my swimsuit and going for a swim!"
elsif temperature >= 80
    puts "I will wear shorts and a shirt today."
elseif temperature >= 70
    puts "I will wear pants and a shirt today."
else 
    puts "I will wear pants and a sweater today."
end
```

Go ahead and try inputs of `67, 77, 87, 97` to make sure that you are getting the output you would expect!

## Rock, Paper, Scissors

Let's try this with the famour rock, paper and scissors game. Go ahead and clear out the code from our two scenarios or comment out the code so you can use it for reference. 

Create a `player_one_choice` variable and use the `gets.chomp` to gather a players input of rock, paper or scissors.

Create a `player_two_choice` variable and use the `gets.chomp` to gather a players input of rock, paper or scissors.

Go ahead and build a game that implements the logic of: 
* paper beats rock
* rock beats scissors
* scissors beat paper

I'll provide the answer below but this would be a great time to spend at least 10-15 minutes trying to implement this on your own.

[put in a gif/meme for passage of time]

Ok, here is what our logic might look like:
```
puts "Player 1: Please make a choice of rock, paper or scissors."
player_one_choice = gets.chomp
# puts player_one_choice
puts "Player 2: Please make a choice of rock, paper or scissors."
player_two_choice = gets.chomp
# puts player_two_choice

# if player one chooses `'rock'`
if player_one_choice == 'rock' 
  if player_two_choice == 'paper'
    puts 'Player 2 wins!'
  elsif player_two_choice == 'scissors'
    puts 'Player 1 wins!'
  else
    puts "It's a tie!"
  end
# if player one chooses `'paper'`
elsif player_one_choice == 'paper'
  if player_two_choice == 'scissors'
    puts "Player two wins!"
  elsif player_two_choice == 'rock'
    puts "Player one wins!"
  else 
    puts "It's a tie!"
  end
# if player one chooses `'scissors'`
else 
  if player_two_choice == 'rock'
    puts "Player two wins!"
  elsif player_two_choice == 'paper'
    puts "Player one wins!"
  else 
    puts "It's a tie!"
  end
end
```

Let's be clear. There is a lot that can be improved with the above code. It doesn't account for if the user has capital letters or provides an option like `'gun'`.

Also, there are other operators that we could use to make this more succint and human readable. 

I tried to write this out in the most verbose (lots of words and code) way possible to help you get a feel for the way the logic flow!

If it isn't clear that is ok! I would suggest watching the video for this lesson where I talk through this code step by step to get a more in depth explanation. I even refactor the code a few times 

I would love to see your solutions! Go ahead and click the share button and post it in this lessons Q&A. It would also be superhelpful for other students to see your solution as well and maybe even give feedback!



