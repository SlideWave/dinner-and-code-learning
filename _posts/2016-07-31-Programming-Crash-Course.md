---
layout: post
title: Programming crash course
---

Coding is super fun and can be very rewarding, but in order to be able 
to complete any projects, you must first have a basic understanding of 
programing constructs.

Programming languages are designed as a bridge for humans to be able to 
give computer a series of instructions to follow in order to complete a 
task.  They have evolved from punch cards, to machine language, to 
systems programming languages, and finally high level object oriented 
and functional programming languages. Language evolution is driven by
our desire to get more done in less time and with less effort.

Ultimately, no matter which language you choose to code in, the
objective is to translate an idea inside your head into a program running 
on a computer. 

# Language Similarities

Almost all programming languages share a few common features:

- They provide a way to store the value of an intermediate calculation. 
These storage locations are called **variables**.
- They provide a way to encapsulate blocks of code into reusable pieces. 
The most primitive of these is normally in the form of a **function**.
- They provide a way to run a block of code N times. This functionality 
is provided either as a loop construct or a way for a function to call 
itself the requisite number of times (this is called recursion). We’ll 
cover **for and while loops**.
- Further, most programming languages provide a way to evaluate the 
conditions under which a block of code is run. This is called a 
conditional construct. 

Understanding these basic similarities is essential to writing any 
computer program. For the remainder of this document, we’ll provide some 
examples of how these features are used to build a functioning computer 
program.

# Getting started

At dinner and code, we concentrate on two languages to start off new 
programmers with: Python, and/or javascript.

### Python
A modern, interactive, object oriented programming language. Its clear 
syntax and extensive libraries make it a great choice for beginners that 
want to learn to write code without having to write absolutely everything 
on their own.

### Javascript
A prototype based programming language. Javascript has quickly become a 
requirement for any serious front end web development. Its ubiquity 
makes it a great language to learn to accomplish a variety of projects.

No matter which language you choose to begin learning about, examples 
are provided in this guide to help explain the basic concepts.

### Getting started in Python

You’ll need to download the python programming language to get started. 
To do this, head over to https://www.python.org/downloads/ and choose 
the latest version of Python 3.0 that is available on the page. Make 
sure you download the correct version for your operating system. Once 
python is installed, you can click on the IDLE editor that comes with 
the package and start typing in code right away.

### Getting started in Javascript
The easiest way to get started in Javascript is simply to navigate to 
jsfiddle.net where you can to type in HTML, JS, and CSS and see 
the results immediately.

---

# Variables
Variables allow you to store the result of some work that has been done 
for later use. Let’s say, for example, you’re writing a program that adds 
two numbers together and does something later on with the result. We can 
use variables to store the result and print it out. 

### Python Variables Example
Open up the IDLE editor and type in a = 5 and then press enter. The 
screen should look something like this below.

```
Python 3.5.1 (v3.5.1:37a07cee5969, Dec  6 2015, 01:54:25) [MSC v.1900 64 bit (AMD64)] on win32
Type "copyright", "credits" or "license()" for more information.
>>> a = 5
>>> 
```

This has assigned the value of 5 to the variable _a_. We can now use _a_ 
later on in the program whenever we need the value again. We can see 
this by telling python to print out the value of a by typing _print(a)_ 
as shown below.

```
Python 3.5.1 (v3.5.1:37a07cee5969, Dec  6 2015, 01:54:25) [MSC v.1900 64 bit (AMD64)] on win32
Type "copyright", "credits" or "license()" for more information.
>>> a = 5
>>> print(a)
5
>>>
```

Note that using _print(a)_ has printed the value of 5. So now if 
we wanted to add two numbers together, we can simply create a new 
variable _b_, give it a different value and add them together using 
the + sign. See below:

```
Python 3.5.1 (v3.5.1:37a07cee5969, Dec  6 2015, 01:54:25) [MSC v.1900 64 bit (AMD64)] on win32
Type "copyright", "credits" or "license()" for more information.
>>> a = 5
>>> print(a)
5
>>> b = 6
>>> print(a + b)
11
>>>
```
5+6 = 11, just as expected. 

We can also store the result of adding the numbers together in another 
variable _c_

```
Python 3.5.1 (v3.5.1:37a07cee5969, Dec  6 2015, 01:54:25) [MSC v.1900 64 bit (AMD64)] on win32
Type "copyright", "credits" or "license()" for more information.
>>> a = 5
>>> print(a)
5
>>> b = 6
>>> print(a + b)
11
>>> c = a + b
>>> print(c)
11
```

We can see that _c_ now has the value 11 from the result of _a + b_

### Javascript Variables Example
Navigate to jsfiddle.net

In the HTML pane to the top left, type the following code:
&lt;p id="output"&gt;&lt;/p&gt;

We'll use this for the rest of the examples as it provides a place for
us to see the output of the code that is written.

From now on, we'll be concentrating on the javascript pane to the bottom
left

Your browser should now look like the following:

![_config.yml]({{ site.baseurl }}/images/jsfiddle.png)

In the javascript pane, type the following code:

    function print(message) {
        var output = document.getElementById('output');
        output.innerHTML = output.innerHTML + "<br>" + message;
    }
    
    var a = 5;
    
    print(a);

Then press the run button at the top left, and you should see output 
like the image below:

![_config.yml]({{ site.baseurl }}/images/jsfiddle2.png)

Notice that the output pane on the bottom right now contains the value 
of the variable _a_ that we set.

```
var a = 5;
```

Tells javascript to assign the value of 5 to the variable named _a_. 
We can now use _a_ later on in the program whenever we need the value 
again. We can see this when we call _print(a)_ which is a simple 
function we have defined to display the value of a variable. Each time 
we use _print(a)_ or _print(something)_ a new line will be appended to
the right panel. We'll talk more about functions later. Just keep in 
mind for now that _print(something)_ is magic that makes a new line
of text appear in the righthand bottom pane.

Now if we wanted to add two numbers together, we can simply create a new
variable _b_, give it a different value, and add them together using
the + sign. See below:


    function print(message) {
	    var output = document.getElementById('output');
        output.innerHTML = output.innerHTML + "<br>" + message;
    }
    
    var a = 5;
    print(a);
    
    var b = 6;
    print(a + b);


Then press the run button at the top left, and you should see output 
like the image below:

![_config.yml]({{ site.baseurl }}/images/jsfiddle3.png)

Note that, in the output pane to the right, we see the initial value of 
_a_ as 5, and then right below it the value of _a + b_ printed. 

5 + 6 is 11, as expected.

We can also store the result of adding the numbers together in another
variable c. Type the following into jsfiddle:

    function print(message) {
	    var output = document.getElementById('output');
        output.innerHTML = output.innerHTML + "<br>" + message;
    }
    
    var a = 5;
    print(a);
    
    var b = 6;
    print(a + b);
    
    var c = a + b;
    print(c);

Then press the run button at the top left, and you should see output 
like the image below:

![_config.yml]({{ site.baseurl }}/images/jsfiddle4.png)

As you can see, the output on the right is now
    
    5
    11
    11

Demonstrating that _c_ holds the result of _a + b_

---

# Functions
Functions allow you to package up multiple commands that you may 
want to reuse more than once in a project. This allows you to write
utilities that can be used anywhere in a program as well as avoiding 
copying and pasting duplicate code all over which leads to bugs 
and having to fix the same problems in multiple places.

### Python function example
In python, we define a function with the **def** keyword. Each function 
has a name, and a set of **parameters** that can be sent to it each time 
we call it. You can think of a function as telling someone what to do, 
and then adding some more specific instructions. A request such as 
"I would like a grilled cheese with tomato" could be represented in 
Python as a function defined like so:

~~~ python
def make_grilled_cheese(include_tomato): #include_tomato is a parameter 
    if include_tomato:
        #do something special to include tomato
    else:
        #make the grilled cheese, but no tomato
~~~

We can call the make_grilled_cheese function in two different ways.
The first includes the tomato, and the second omits it:

~~~ python
make_grilled_cheese(False) #makes a grilled cheese without tomato
make_grilled_cheese(True) #makes a grilled cheese with tomato
~~~

When the make_grilled_cheese function is called as above, the value we
pass in sets the value of the _include_tomato_ parameter inside the
function, and we can then test if the caller would like tomato or not.

In our previous python examples, _print()_ was a function that we called
to see the values of our variables. This function is defined by the
python language, so we didn't actually have to **def** it.

~~~ python
a = 5
print(a)
~~~

In the code above, _a_ is the parameter passed to the print function.
print(X) takes whatever we pass in for X and prints it to the screen

Functions can also return values to be used later. We use the 
**return** keyword to accomplish this.

Lets define our own function and call it. Open IDLE and fill out a 
function called double_a_number. It should look like the following:

    Python 2.7.10 (default, May 23 2015, 09:40:32) [MSC v.1500 32 bit (Intel)] on win32
    Type "copyright", "credits" or "license()" for more information.
    >>> def double_a_number(number):
        return number * 2
    
    >>> 

The function we have defined is called double_a_number, and it takes a
single number as a parameter. **return** sends a value back to the
caller, and in this case, the value it sends is whatever the caller
passed to the _number_ parameter multiplied by 2 as in the above 
_return number * 2_

Now that we have a function to call, lets call it and see if it does
what we expect

    Python 2.7.10 (default, May 23 2015, 09:40:32) [MSC v.1500 32 bit (Intel)] on win32
    Type "copyright", "credits" or "license()" for more information.
    >>> def double_a_number(number):
        return number * 2
    
    >>> a = 5
    >>> double_a_number(a)
    10
    >>> 

As in the previous example, we set the value of _a_ to 5 using _a = 5_
but now instead of just printing it out, we pass it to our 
double_a_number function. We then see that _double_a_number(a)_ returns
10 as expected, since we passed 5 in as the number parameter and it was
doubled.

We can also store the return value of a function for later use. Just 
like an assignment of _a = 5_, we do this like so:

    Python 2.7.10 (default, May 23 2015, 09:40:32) [MSC v.1500 32 bit (Intel)] on win32
    Type "copyright", "credits" or "license()" for more information.
    >>> def double_a_number(number):
        return number * 2
    
    >>> a = 5
    >>> double_a_number(a)
    10
    >>> b = 10
    >>> result = double_a_number(10)
    >>> print(result)
    20
    >>> 

Note that we're assigning the result of _double_a_number(10)_ to the
variable result by typing _result = double_a_number(10)_ 

After that we can print out the result of _double_a_number(10)_ by calling the 
print function on _result_ as shown above in _print(result)_

### Javascript function example
In javascript, we define a function with the **function** keyword. Each 
function has a name, and a set of **parameters** that can be sent to it 
each time we call it. You can think of a function as telling someone 
what to do, and then adding some more specific instructions. A request 
such as "I would like a grilled cheese with tomato" could be represented 
in Javascript as a function defined like so:

~~~ javascript
function makeGrilledCheese(includeTomato) {
    if (includeTomato) {
        //do something special to include tomato
    } else {
        //make the grilled cheese, but no tomato
    }
}
~~~

We can call the makeGrilledCheese function in two different ways.
The first includes the tomato, and the second omits it:

~~~ javascript
makeGrilledCheese(false); //makes a grilled cheese without tomato
makeGrilledCheese(true); //makes a grilled cheese with tomato
~~~

When the makeGrilledCheese function is called as above, the value we
pass in sets the value of the _includeTomato_ parameter inside the
function, and we can then test if the caller would like tomato or not.

Let's take a look at another function we defined earlier.

Make sure you have jsfiddle open as in the previous example and lets 
take a look at our starting point print function:

    function print(message) {
        var output = document.getElementById('output');
        output.innerHTML = output.innerHTML + "<br>" + message;
    }

Here, we are interacting with the web browser in order to print messages 
The name of the function is _print_, and it takes a single parameter
called _message_. We then find the output p tag we added to the HTML in
the top left window, and add the content contained in the _message_
parameter to it.

Functions can also return values to be used later. We use the 
**return** keyword to accomplish this.

Lets define our own function and call it. Add a new function below
the _print_ function called _doubleTheNumber_. It should take a 
parameter called _number_, and **return** that number multiplied by 2. 

Your jsfiddle should now look like this:

![_config.yml]({{ site.baseurl }}/images/jsfiddle5.png)

Let's look at the function in depth

~~~ javascript
function doubleTheNumber(number) { // number here is the parameter
		return number * 2; //return the parameter multiplied by 2
}
~~~

We would call the function like so:

~~~ javascript
var a = 5;
print(doubleTheNumber(a));
~~~

Lets add this below the functions in our jsfiddle and then press play 
to see the result which should now look like this:

![_config.yml]({{ site.baseurl }}/images/jsfiddle6.png)

Note that the output of the function has been printed directly via
_print(doubleTheNumber(a));_. We can also store the result in a variable
and then print it out later, like so:

~~~ javascript
var result = doubleTheNumber(a);
print(result);
~~~

Add these lines to the program and you should see the following results:

![_config.yml]({{ site.baseurl }}/images/jsfiddle7.png)

---

# Loops
Loops give us a way to perform some task more than once. This task 
can be anything from counting from 1 to 10 to iterating all the 
elements in a list.

### Python looping examples
Let's say we want to print out numbers from 1 - 10 in python. There are
actually a few ways to do this. Let's explore a couple:

Open up IDLE and type in the following code:

    Python 2.7.10 (default, May 23 2015, 09:40:32) [MSC v.1500 32 bit (Intel)] on win32
    Type "copyright", "credits" or "license()" for more information.
    >>> number = 0
    >>> while number < 5:
    	number = number + 1
    	print(number)

When you press enter after the last line, you should see the following 
appear:

    Python 2.7.10 (default, May 23 2015, 09:40:32) [MSC v.1500 32 bit (Intel)] on win32
    Type "copyright", "credits" or "license()" for more information.
    >>> number = 0
    >>> while number < 5:
            number = number + 1
            print(number)
    
        
    1
    2
    3
    4
    5
    >>> 

Note that python listed all numbers between 1 and 5 and then brought us
back to the prompt. Lets take a closer look:

~~~ python
while number < 5:
~~~

This tells python that everything indented underneath this statement
will be repeated over and over again in top down order while the 
_number_ variable is less than 5.

~~~ python
number = number + 1
~~~

This takes whatever the current value of the _number_ variable is,
adds 1 to it, and then assigns the new value back to _number_ creating
a counter.

~~~ python
print(number)
~~~

We've done this before. Prints out the number to the screen.

If you imagine this running over and over again in your head:

~~~ python
number = number + 1
print(number)
~~~

You can start to understand why we have to put limits on the while loop.
_number < 5_ makes it so that we don't continue the loop forever (a 
bug known as an infinite loop). We can intentionally create a loop that
goes on forever by replacing _while number < 5_ with _while True_, but 
I dont recommend this as you'll have to force kill IDLE to be able to
work again.

In python we can also use a builtin function called _range_ to more easily 
create loops that iterate through a range of numbers.

Below is an easier way to do what we did above:

    Python 2.7.10 (default, May 23 2015, 09:40:32) [MSC v.1500 32 bit (Intel)] on win32
    Type "copyright", "credits" or "license()" for more information.
    >>> number = 0
    >>> while number < 5:
    	number = number + 1
    	print(number)
    
    	
    1
    2
    3
    4
    5
    >>> for number in range(1, 6):
    	print(number)
    
    	
    1
    2
    3
    4
    5
    >>> 
    
Note that the two loops have the exact same output, but the bottom one
is less code. The _range_ function returns numbers between the two 
parameters given, up to but not including the second number.

_range(start, end)_

This means:

~~~ python
for number in range(1, 6): #first parameter is the start so 1 is included
    print(number) #prints the numbers 1 through 5. 6 is excluded
    
for number in range(3, 9): #first parameter is the start so 3 is included
    print(number) #prints the numbers 3 through 8. 9 is excluded
~~~

### Javascript looping examples
Let's say we want to print out numbers from 1 - 10 in Javascript. There 
are actually a few ways to do this. Let's explore a couple. We'll start
off with our print function and add to it.

    function print(message) {
        var output = document.getElementById('output');
        output.innerHTML = output.innerHTML + "<br>" + message;
    }
    
    var number = 0;
    while (number < 5) {
        number = number + 1;
        print(number);
    }

Typing that into the javascript panel of our jsfiddle and pressing the
Run button will yield the following:

![_config.yml]({{ site.baseurl }}/images/jsfiddle8.png)

Note that javascript listed all numbers between 1 and 5 and then brought us
back to the prompt. Lets take a closer look:

~~~ javascript
while (number < 5) {
    
}
~~~

This tells javascript that everything contained between the curly 
brackets of this statement will be repeated over and over again in top 
down order while the _number_ variable is less than 5.

~~~ javascript
number = number + 1;
~~~

This takes whatever the current value of the _number_ variable is,
adds 1 to it, and then assigns the new value back to _number_ creating
a counter.

~~~ javascript
print(number);
~~~

We've done this before. Prints out the number to the screen.

If you imagine this running over and over again in your head:

~~~ javascript
number = number + 1;
print(number);
~~~

You can start to understand why we have to put limits on the while loop.
_number < 5_ makes it so that we don't continue the loop forever (a 
bug known as an infinite loop). We can intentionally create a loop that
goes on forever by replacing _while number < 5_ with _while true_, but 
I don't recommend this as you'll have to force kill the browser or script
to be able to work again.

An even easier way to count in Javascript is the **for** loop:

        function print(message) {
            var output = document.getElementById('output');
            output.innerHTML = output.innerHTML + "<br>" + message;
        }
        
        var number = 0;
        while (number < 5) {
            number = number + 1;
            print(number);
        }
            
        for (number = 1; number < 6; number++) {
            print(number);
        }

Typing that into the javascript panel of our jsfiddle and pressing the
Run button will yield the following:

![_config.yml]({{ site.baseurl }}/images/jsfiddle9.png)

_for (number = 1; number < 6; number++) {_

This means:

~~~ javascript   
for (number = 1; //start our counter variable, number at 1
number < 6; //continue while number is less than 6 
number++) { //shorthand for number = number + 1
    
}
~~~

Note that the two loops have the exact same output, but the bottom one
is less lines, and less prone to mistakes

# Conditionals
Programming gets really interesting when you can test conditions and change
the program's behavior depending on the outcome of the tests. Conditionals 
allow you to do this. You have already seen conditionals at work earlier in 
the make_grilled_cheese(include_tomato) function. Let's take a look more in 
depth:

## Boolean expressions

A boolean expression is one that evaluates to produce a result which is of
a boolean type (that is, either true or false.) Boolean expressions are the 
basis for all modern computer logic. For example, in python, the operator ==
tests that two variables or values are equal. It produces (or yields) a 
boolean value:

~~~ python
>>> 3 == (1 + 2)
True
>>> 3 == 4
False
>>> j = "cod"
>>> j == "code"
False
>>> j + "e" == "code"
True
~~~

## Conditional execution
In order to code useful and interesting programs, we almost always need the
ability to evaluate conditions and change the program behavior accordingly.
The simplest form is the if statement:

~~~ python
if x % 2 == 0:
    print(x, " is even.")
    print("Did you know that two is the only even number that is also prime?")
else:
    print(x, "is odd.")
    print("Did you know that multiplying two odd numbers always yields " +
        "an odd result?")
~~~

The boolean expression after an if statement is called a condition. If true, 
then all indented statements get executed. If false, then all the statements
indented under the else clause get executed. An else clause is optional. You
may write conditionals that only evaluate whether a condition is true and do 
nothing when false.

## Chained conditionals
Sometimes there are more than two possibilities and we need more than two 
paths the code may take. One way to express this is with a chained conditional.
An example:

~~~ python
if x < y:
    print(x, " is less than ", y)
elif x > y:
    print(x, " is greater than ", y)
else:
    print("If ", x, " is neither greater nor lesser than ", y,
       " it must be equal to it.")
~~~
