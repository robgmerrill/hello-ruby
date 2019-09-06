Great job making it this far!

So far we have learned: 
* who this course is for
* the format of this course
* our development environment

Let's now print "Hello Ruby"!

Let's head to this link: https://repl.it/@robgmerrill/helloruby 

When you do you will see prepopulated content in the text editor. Each line begins with a <code>#</code>. 

You probably recognize this as the "hash" or "pound" sign. It's also known as an "octothorpe" which I particularly like :) 

I'll usually refer to this as the "pound" or "hash" for brevity. 

Any line that starts with the <code>#</code> is a comment. A comment is just text that we don't want our Ruby interpreter to do anything with. 

It isn't for the computer. It is for YOU! It is also for those who are reading or working on your code with you. 

While we will always try to make our code easy to understand for humans sometimes as your codebase grows you may have a reason for writing some code that isn't clear days, weeks or months later when you or someone else is working on that code to add features or fix a bug. 

Comments help a human to quickly understand the code in a program. 

As you can see these comments are full of text such as <code># create a variable called `message` and give it a value of a string `"Hello Ruby"`</code>

You might be wandering what the <code>``</code> mean that are surrounding message and "Hello Ruby" in the comment?

They have a bigger purpose when not in comments but when I use them within a comment they are meant to communicate actual code I want you to write. 

So under this comment I want you to literally write `message` and give it a value of the string `"Hello Ruby"`.

Make sense? If not, that's ok, we'll work this out together. 

So under the first comment let's write out <code>message = "Hello Ruby"</code>

Perfect. That <code>=</code> is an assignment operator. Don't worry about memorizing key words such as `operator` for now. While it is good to take not of words that you may not be familiar with we will be using them over and over again to give time for them to sink in. <code>message</code> is a variable and <code>"Hello Ruby"</code> is a string. 

Again, we will explain these terms in depth in a few lessons so dont' worry if that just sounds like technical jargon right now. 

Let's look at our next comment:
<code># use the `print` function to print the value of `message`</code>

Let's try this together:
<code>print message</code>

Great! We just used a Ruby function!

You probably didn't know it but `print` is a built in Ruby function that we can pass a value to, such as <code>message</code>, and it prints or outputs the value as you should should see on the right hand side of the screen. 

Go ahead and press the run button and you should get an output of `"Hello Ruby"`. 

We'll talk about functions in depth in the future. We will look at the built in ones that are available like `print` and functions that we can create on our own :) 


Code solution:
```
# create a variable called `message` and give it a value of a string `"Hello Ruby"`
message = "Hello Ruby"

# use the `print` function to print the value of `message`
print message
```