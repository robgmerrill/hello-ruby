# Ruby Loops

## `while` loop
Let's imagine a scenario in which a person has to go on a run. In this ficticious example let's give the person an energy level of 100 when they start their run. Next, let's imagine every mile takes 10 units of energy. After all of their energy is spent we want to print a message that the person is out of energy and share how many miles they ran. 

Let's imagine what this might look like in code. We would need a variable that contains the starting energy level, `starting_energy`. We would also want a variable that tracks the miles that are ran. We then need a loop, what we are going to learn in this lesson, that will remove `10` energy points from the starting energy level then add `1` to the variable that tracks miles, `miles_ran`. Then we want to print a final message that the run is completed and the total of miles ran. Let's take a look at how we might do that with Ruby loops:

```
starting_energy = 100
energy_per_mile = 10
miles_ran = 0
print_total = false 

while starting_energy > 0
    starting_energy = starting_energy - energy_per_mile
    miles_ran = miles_ran + 1
end

puts "Good job! You ran a total of #{miles_ran} mile(s)."
```

We used a `while` loop to accomplish this. Notice the syntax is the `while` keyword followed by a condition `starting_energy > 0`. As long as this is true we run the following code between the `while` keyword and condition and the `end` keyword:
```
starting_energy = starting_energy - energy_per_mile
miles_ran = miles_ran + 1
```

## `for` loop
In the situation above the `while` loop was a perfect fit when we didn't know how many times we wanted to run our code. 

However, there are times where we know how many times we want our code to run. This is a great time to use a `for` loop.

Take a look at this code and try to guess what it does. After you have done that go ahead and run it in a sandbox so see if the results match what you expected:
```
for number in 1...20
    puts num
end
```

Did you get what you expected? Let's look at the syntax `for number in 1...20`

This says to Ruby: For the variable `number` in the range `1` to `20`, run the following code: `puts num`.

Did you wonder why the program printed `19` and not `20`?
That is because `for number in 1...20` means "go up to but don't include `19`. If you wanted to include `20` then you would use two dots `..` which would look like `for number in 1..20`.

There are many more ways to repeatedly run a block of code. These are just two ways. We'll cover more as this course goes on but we now have enough for the next steps in our program! 

Let's go!



