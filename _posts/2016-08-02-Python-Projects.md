---
layout: post
title: Python Projects
---

Dinner and Code currently offers two programming paths: Python and web development. On this page are the Python projects.

<em>Python is a modern, interactive, object oriented programming language. Its clear 
syntax and extensive libraries make it a great choice for beginners that 
want to learn to write code without having to write absolutely everything 
on their own.</em>

# Project Listing 
<ol>
<li>Project 1: Dice Rolling Game</li>
<li>Project 2: Mad Libs Generator</li>
<li>Project 3: Hangman</li>
</ol>

<em>All of the projects are listed on this page. Keep scrolling to see more.</em>

---


# Project 1: Dice Rolling Program
Difficulty Level: Beginner

Language: Python

## Concepts Learned:
<ul>
<li>Using a text editor and console</li>
<li>Importing a module</li>
<li>Creating a WHILE loop</li>
<li>Working with Integers</li>
<li>Print</li>
</ul>

## Description:
This basic dice rolling program will let you get comfortable with coding in Python. The
program will randomly select a number (based on the number of “sides” your die
has) and print it out on the screen. 

## What you’ll need:

### Text editor such as:

1. NotePad++ ([https://notepad-plus-plus.org](https://notepad-plus-plus.org/))

2. Brackets ([http://brackets.io/](http://brackets.io/)) 

3. TextWrangler ([http://www.barebones.com/products/textwrangler/](http://www.barebones.com/products/textwrangler/)) 

### Python Download:
[Python Download Page](http://python.org/download)

### Learning Resources for this Lesson:
<ul>
<li>How to Use the Random Module in
Python[http://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python](http://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)</li>
<li>Choose Your on PyVenture: The Random
Module [The Random Module](https://en.wikibooks.org/wiki/Choose_Your_Own_Pyventure/Random_and_PRNGs)</li>
<li>Learn Python the Hard Way (Python
2.7) [Learn Python the Hard Way](http://learnpythonthehardway.org/)</li>
<li>Zed Shaw’s Command Line Crash Course [Zed Shaw's Command Line Crash Course](http://learnpythonthehardway.org/book/appendixa.html)</li>
<li>Python 2.7 Docs [https://docs.python.org/2.7/](https://docs.python.org/2.7/)</li>
</ul>

### The How-To Video for this Project
[YouTube](https://youtu.be/48n9NnK4k-M)


## The Steps

### Step 1: Get Set Up
You’ll need to install a text editor and configure it for your particular machine. Since
the steps vary, it’s best to do some Google Fu as it relates to your particular
text editor + OS combination. 

See: [Learn Python the Hard Way Lesson](http://learnpythonthehardway.org/book/ex0.html)

You’ll then need to install Python 2.7:
[Python.org Download](http://python.org/download)

### Step 2: Create a file in your Text editor

Go ahead and create a .py file in your editor. This file is what you’ll call in your command
line. Make sure you save it in the right place so Python can call it up.

### Step 3: Start writing some code

This program has several components you must include:

<ul>
<li>Call the Random Module</li>
<li>Define a function to Roll the dice</li>
<li>Define a main() function of the program</li>
<li>Print the results</li>
</ul>

### Code Example:

```
import
random

 

def
roll(sides=6): 

    num_rolled = random.randint(1,sides)

    return num_rolled

 

def main():

    sides = 6

    rolling = True

    while rolling:

        roll_again = input("Ready to roll?
ENTER=Roll. Q=Quit. ")

        if roll_again.lower() != "q":

        num_rolled = roll(sides)

        print("You rolled a",
num_rolled)

    else:

        rolled = False

        

    print("Thanks for playing.")

    

    main()

```

### Step 4: Run the program

In your command line, go ahead and run the program. If you need help, see: [http://learnpythonthehardway.org/book/ex1.html](http://learnpythonthehardway.org/book/ex1.html)

---

# Project 2:  Mad Libs Generator

Difficulty Level: Beginner

Language: Python (v3)

## Concepts Learned:
<ul>
<li>Using a text editor and console</li>
<li>Importing a module</li>
<li>Creating a WHILE loop</li>
<li>Working with Integers</li>
<li>Print</li>
</ul>

## Description:
This basic dice rolling program will let you get comfortable with coding in Python. The program will randomly select a number (based on the number of “sides” your die has) and print it out on the screen. 


## Learning Resources:
<em>See lesson 1's resources</em>

[How-To Video for this Project](https://youtu.be/Oq75BBqd2y0)

### Step 3: Start writing some code
This project is creative, so much of the code is up to you! The components required to make it work include:
<ul>
<li>Print function</li>
<li>Main function</li>	
<li>Variables</li>	
<li>Strings</li>
</ul>

#### Code Example:
See: http://anh.cs.luc.edu/python/hands-on/3.1/handsonHtml/madlib2.html

```
print("Welcome to Mad Libs - Python Edition. Follow the prompts to create your own hilarious story.")

proper_name1 = raw_input("Enter a name: ")
proper_name2 = raw_input("Enter another name: ")
noun1 = raw_input("Enter a proper title: ")
place1 = raw_input("Enter a place: ")
place2 = raw_input("Enter another place: ")
verb1 = raw_input("Enter a present-tense verb: ")
noun3 = raw_input("Enter a noun: ")
noun2 = raw_input("Enter a plural noun: ")
noun4 = raw_input("Enter another plural noun: ")
num2 = raw_input("Enter a number: ")
num1 = raw_input("Enter another number: ")
percent1 = raw_input("Enter another number: ")

print("Dear {}, It is my pleasure to {} to you today. I am {} and I'm the "
     "{} of {}. I have inherited {} {} but I need your help to get it to {}."
     "Please send me your {} and the sum of {} {} to get started, and I will"
      " give you {} percent of my inheritance. Yours truly, {}".format(
          proper_name1, verb1, proper_name2, noun1, place1, num1, noun2, 
          place2, noun3, num2, noun4, percent1, proper_name2))
```

## Step 4: Run the program
In your command line, go ahead and run the program. If you need help, see: http://learnpythonthehardway.org/book/ex1.html

---

# Project 3: Hangman

Difficulty Level: Intermediate

Language: Python (v3)

## Concepts Learned:
<ul>
<li>Using a text editor and console</li>
<li>Importing a module</li>
<li>Creating a WHILE loop</li>
<li>Working with Integers</li>
<li>Print</li>
<li>Random</li>
<li>Variables</li>
<li>Boolean</li>
<li>Input/Output</li>
<li>Char</li>
<li>Strings</li>
<li>Length</li>
</ul>

## Description:

The main goal here is to create a “guess the word” game. The user needs to be able to input letter guesses (strings). A limit should also be set on how many guesses they can use. This means you’ll need a way to grab a word to use for guessing. (This can be grabbed from a pre-made list. No need to get too fancy.) You will also need functions to check if the user has actually inputted a single letter, to check if the inputted letter is in the hidden word (and if it is, how many times it appears), to print letters, and a counter variable to limit guesses.


## Learning Resources:

[How-To Video for this Project](https://youtu.be/5aAkDVXxNhk)

### Step 3: Start writing some code
This project is creative, so much of the code is up to you! The components required to make it work include:
•	Print function
•	Main function
•	Print
•	Random
•	Variables
•	Boolean
•	Input/Output
•	Char
•	Strings
•	Length

#### Code Example:
<em>Here’s one with a timer from http://www.pythonforbeginners.com/code-snippets-source-code/game-hangman:</em>
```
#importing the time module
import time

#welcoming the user
name = raw_input("What is your name? ")

print "Hello, " + name, "Time to play hangman!"

print "
"

#wait for 1 second
time.sleep(1)

print "Start guessing..."
time.sleep(0.5)

#here we set the secret
word = "secret"

#creates an variable with an empty value
guesses = ''

#determine the number of turns
turns = 10

# Create a while loop

#check if the turns are more than zero
while turns > 0:         

    # make a counter that starts with zero
    failed = 0             

    # for every character in secret_word    
    for char in word:      

    # see if the character is in the players guess
        if char in guesses:    
    
        # print then out the character
            print char,    

        else:
    
        # if not found, print a dash
            print "_",     
       
        # and increase the failed counter with one
            failed += 1    

    # if failed is equal to zero

    # print You Won
    if failed == 0:        
        print "
You won"  

    # exit the script
        break              

    print

    # ask the user go guess a character
    guess = raw_input("guess a character:") 

    # set the players guess to guesses
    guesses += guess                    

    # if the guess is not found in the secret word
    if guess not in word:  
 
     # turns counter decreases with 1 (now 9)
        turns -= 1        
 
    # print wrong
        print "Wrong
"    
 
    # how many turns are left
        print "You have", + turns, 'more guesses' 
 
    # if the turns are equal to zero
        if turns == 0:           
    
        # print "You Loose"
            print "You Loose
"


```
### Step 4: Run the program

In your command line, go ahead and run the program. If you need help, see: [Learn Python the Hard Way Lesson](http://learnpythonthehardway.org/book/ex1.html)


