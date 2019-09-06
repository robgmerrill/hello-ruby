# Conditionals Part 2

Great job so far learning about conditionals! 

We are going to learn about two more operators that we will need in programming with Ruby. 

Go ahead and open the following link and we will look at how to use conditionals to look at a couple more scenarios: https://repl.it/@robgmerrill/Conditionals-Part-2

AND operator: `&&`
OR operator: `||`

Let's go back to our example of dressing for the weather. Instead of looking at the temperature alone we might want to look at the possibility of rain. 

We might think to ourselves that if the weather is over 70 degrees AND it is not raining then we will wear shorts and a shirt. If it is going to rain then we will wear pants and a jacket.

The keyword is AND. We need both things to be true.

Here is what that might look like with the `&&` operator:

```
no_rain = true
temperature = 75

if temperature >= 70 && no_rain 
    puts "I will wear shorts and a shirt."
else 
    puts "I will wear pants and a jacket."
end
```

The output will be: `I will wear shorts and a shirt.`

However, if it will rain: 
```
no_rain = false
temperature = 75

if temperature >= 70 && no_rain 
    puts "I will wear shorts and a shirt."
else 
    puts "I will wear pants and a jacket."
end
```

The output will be: `I will wear pants and a jacket.`

This is because while  `temperature >= 70` is `true`, `no_rain` is `false`. The `&&` operator needs both of these to be `true` to evaluate to `true`.

Ok, now let's imagine another scenario. Let's imagine that you want to exercise outside. You don't mind if it is a little cold (under 70 degrees) as long as it isn't windy (below 5mph). You also don't mind if it is windy as long as it isn't too cold. 

```
wind_below_five_mph = false
temperature = 75

if temperature >= 70 || wind_below_five_mph
    puts "Looks like a good day for a run!"
else 
    puts "Something about the weather doesn't feel right."
end
```

The ouput when we run our code is: `Looks like a good day for a run!`

The `||` looks to see if either `temperature >= 70` is `true` or `wind_below_five_mph`. If either is `true` then our condition passes. 

Look what happens when we change our variale values:
```
wind_below_five_mph = true
temperature = 55

if (temperature >= 70 || wind_below_five_mph) 
    puts "Looks like a good day for a run!"
else 
    puts "Something about the weather doesn't feel right."
end
```

The output in this scenario is the same. As long as one of our expressions are true the condition will be true.


As you can see these operator would be helpful in reflecting the complexities of human life and how we make decisions. We'll often times find in writing programs that we'll have to take advantage of these operators to help our program run as we need it to!

Let's look at one more operator to close out this lesson.

## `!=` operator
The not equal, `!=`, operator checks if the value of two operands are equal or not, if values are not equal then condition becomes `true`.

Instead of coming up with a new weather scenario let's go ahead and rewrite our previous examples with the `!=` operator.


```
is_windy = false
temperature = 55

if (temperature >= 70 || !is_windy) 
    puts "Looks like a good day for a run!"
else 
    puts "Something about the weather doesn't feel right."
end
```

So in the example above `temperature >= 70` is `false` but `is_windy` is `!false` which is actually `true`.

Let's look at one more example using the `!=` operator with `&&`:

```
rain = true
temperature = 75

if (temperature >= 70 && !rain) 
    puts "I will wear shorts and a shirt."
else 
    puts "I will wear pants and a jacket."
end
```

This will output `I will wear shorts and a shirt.` because `temperature >=70` is `true` and `rain` is `!false` which is also true.

Great! All this will really help you as a Ruby developer. Now, let's move on and continue to work on our Guess the Jelly Bean program!

Add this to examples challenges:

The `&&` operator is going to require that two statements are true to return true: 
if (5 > 4 && 3 > 2) 
    puts "These are both true"
else 
    puts "These are not both true"

if (5 > 6 && 3 > 2) 
    puts "These are not both true."



Starter Code: 
```
# Scenario 1: if the weather is over 70 degrees AND it is not raining then we will wear shorts and a shirt. If it is going to rain then we will wear pants and a jacket.
  # AND operator: `&&`
  # if 70 or more AND not raining - "I will wear shorts and a shirt."



# Scenario 2: Let's imagine that you want to exercise outside. You don't mind if it is a little cold (under 70 degrees) as long as it isn't windy (under 5mph). You also don't mind if it is windy as long as it isn't too cold. 
  # OR operator: `||`
  # if temp is 70 degrees or more OR wind is less than 5mph - "Looks like a good day for a run!"


## `!=` operator
  # The not equal, `!=`, operator checks if the value of two operands are equal or not, if values are not equal then condition becomes `true`.
  # rewrite previous examples with `!=` operator. Feel free to rewrite variables boolean values  
```