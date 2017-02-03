---
layout: post
title: Python Projects
---

Dinner and Code currently offers two programming paths: Python and
javascript development. On this page are the Python projects.

<em>Python is a modern, interactive, object oriented programming language. Its clear
syntax and extensive libraries make it a great choice for beginners that
want to learn to write code without having to write absolutely everything
on their own.</em>

# Project Listing
<ol>
<li>Project 1: Dice Rolling Game</li>
<li>Project 2: Mad Libs Generator</li>
<li>Project 3: Hangman</li>
<li>Project 4: Nibbles</li>
</ol>

<em>All of the projects are listed on this page. Keep scrolling to see more.</em>

---


# Project 1: Dice Rolling Program
Difficulty Level: Beginner

Language: Python

## Concepts Learned:
* Using a text editor and console
* Importing a module
* Creating a WHILE loop
* Working with Integers
* Print

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
* How to Use the Random Module in Python [http://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python](http://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)</li>
* Choose Your on PyVenture: The Random Module [The Random Module](https://en.wikibooks.org/wiki/Choose_Your_Own_Pyventure/Random_and_PRNGs)</li>
* Learn Python the Hard Way (Python 2.7) [Learn Python the Hard Way](http://learnpythonthehardway.org/)</li>
* Zed Shaw’s Command Line Crash Course [Zed Shaw's Command Line Crash Course](http://learnpythonthehardway.org/book/appendixa.html)</li>
* Python 2.7 Docs [https://docs.python.org/2.7/](https://docs.python.org/2.7/)</li>


### The How-To Video for this Project
[YouTube](https://youtu.be/48n9NnK4k-M)

## The Steps

### Step 1: Get Set Up
You’ll need to install a text editor and configure it for your particular machine. Since
the steps vary, it’s best to do some Google Fu as it relates to your particular
text editor + OS combination.

See: [Learn Python the Hard Way Lesson](http://learnpythonthehardway.org/book/ex0.html)

You’ll then need to install Python 2.7: [Python.org Download](http://python.org/download)

### Step 2: Create a file in your Text editor

Go ahead and create a .py file in your editor. This file is what you’ll call in your command
line. Make sure you save it in the right place so Python can call it up.

### Step 3: Start writing some code

This program has several components you must include:

* Call the Random Module
* Define a function to Roll the dice
* Define a main() function of the program
* We should be good to go on Monday with that outline and agendaPrint the results

### Code Example:

~~~ python
# python 2: delete 'from builtins import input'

# python 2: use raw_input('') instead of input('')
# e.g. roll_again = raw_input("Ready to roll? ENTER=Roll. Q=Quit. ")

from builtins import input
import random

def roll(sides=6):
    num_rolled = random.randint(1, sides)
    return num_rolled

def main():
    sides = 6
    rolling = True
    while rolling:
        roll_again = input("Ready to roll? ENTER=Roll. Q=Quit. ")
        if roll_again.lower() != "q":
            num_rolled = roll(sides)

            print("You rolled a {}".format(num_rolled))
        else:
            rolling = False

    print("Thanks for playing.")

main()
~~~

### Step 4: Run the program

In your command line, go ahead and run the program. If you need help, see:
[http://learnpythonthehardway.org/book/ex1.html](http://learnpythonthehardway.org/book/ex1.html)

---

# Project 2:  Mad Libs Generator

Difficulty Level: Beginner

Language: Python (v3)

## Concepts Learned:
* Using a text editor and console
* Importing a module
* Creating a WHILE loop
* Working with Integers
* Print

## Description:
The mad libs generator will take a few inputs from the user and then
generate a funny story! Try it out and have some fun

## Learning Resources:
<em>See lesson 1's resources</em>

[How-To Video for this Project](https://youtu.be/Oq75BBqd2y0)

### Step 3: Start writing some code
This project is creative, so much of the code is up to you! The components required to make it work include:
* Print function
* Main function
* Variables
* Strings

#### Code Example:
See: http://anh.cs.luc.edu/python/hands-on/3.1/handsonHtml/madlib2.html

~~~ python
# python 2: remove 'from builtins import input'
from builtins import input

print("Welcome to Mad Libs - Python Edition. Follow the prompts to create your own hilarious story.")

# python 2: use raw_input('') instead of input('')
	# proper_name1 = raw_input("Enter a name: ")

proper_name1 = input("Enter a name: ")
proper_name2 = input("Enter another name: ")
noun1 = input("Enter a proper title: ")
place1 = input("Enter a place: ")
place2 = input("Enter another place: ")
verb1 = input("Enter a present-tense verb: ")
noun3 = input("Enter a noun: ")
noun2 = input("Enter a plural noun: ")
noun4 = input("Enter another plural noun: ")
num2 = input("Enter a number: ")
num1 = input("Enter another number: ")
percent1 = input("Enter another number: ")

# \n inside of a string means new line

print("\nDear {}, \n\nIt is my pleasure to {} to you today. I am {} and I'm the "
     "{} of {}. I have inherited {} {} but I need your help to get it to {}. "
     "Please send me your {} and the sum of {} {} to get started, and I will "
      "give you {} percent of my inheritance. \n\nYours truly, \n{}"
      .format(proper_name1, verb1, proper_name2, noun1, place1, num1, noun2,
        place2, noun3, num2, noun4, percent1, proper_name2))
~~~

## Step 4: Run the program
In your command line, go ahead and run the program. If you need help, see: http://learnpythonthehardway.org/book/ex1.html

---

# Project 3: Hangman

Difficulty Level: Intermediate

Language: Python (v3)

## Concepts Learned:
* Using a text editor and console
* Importing a module
* Creating a WHILE loop
* Working with Integers
* Print
* Random
* Variables
* Boolean
* Input/Output
* Char
* Strings
* Length

## Description:

The main goal here is to create a “guess the word” game. The user needs to be able to input letter guesses (strings). A limit should also be set on how many guesses they can use. This means you’ll need a way to grab a word to use for guessing. (This can be grabbed from a pre-made list. No need to get too fancy.) You will also need functions to check if the user has actually inputted a single letter, to check if the inputted letter is in the hidden word (and if it is, how many times it appears), to print letters, and a counter variable to limit guesses.

## Learning Resources:

[How-To Video for this Project](https://youtu.be/5aAkDVXxNhk)

### Step 3: Start writing some code
This project is creative, so much of the code is up to you! The components required to make it work include:
* Print function
* Main function
* Print
* Random
* Variables
* Boolean
* Input/Output
* Char
* Strings
* Length

#### Code Example:
Here’s one with a timer from http://www.pythonforbeginners.com/code-snippets-source-code/game-hangman:

~~~ python
from builtins import input
import time

#welcoming the user
name = input("What is your name? ")

print("Hello, " + name + " Time to play hangman!")

print("")

#wait for 1 second
time.sleep(1)

print("Start guessing...")
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
            print(char)
        else:
            # if not found, print a dash
            print("_")
            # and increase the failed counter with one
            failed += 1

    # if failed is equal to zero
    # print You Won
    if failed == 0:
        print("You Win")
        # exit the loop, effectively ending the script
        break

    print("")

    # ask the user go guess a character
    guess = input("guess a character:")

    # set the players guess to guesses
    guesses += guess

    # if the guess is not found in the secret word
    if guess not in word:
        # turns counter decreases with 1 (now 9)
        turns -= 1

        # print wrong
        print("Wrong")

        # how many turns are left
        print("You have", + turns, 'more guesses')

        # if the turns are equal to zero
        if turns == 0:
            # print "You Lose"
            print("You Lose")
~~~

### Step 4: Run the program

In your command line, go ahead and run the program. If you need help, see:
[Learn Python the Hard Way Lesson](http://learnpythonthehardway.org/book/ex1.html)

# Project 4: Nibbles

Difficulty Level: Intermediate

Language: Python 3 with Tkinter

## Concepts Learned:
* Importing modules
* Using Tkinter, the defacto GUI library for Python
* Basic multi-threading and concurrency
* Sprite generation
* Arrays and Dictionaries
* Object-oriented design

## Description
This project servers to intruduce you to the queue module in Python as used in conjunction with the threading module and basic introduction to concurrency and multi-threaded software. The game could have been implemented without threads and queues, but it would have been slower, longer, and a lot more complex. By using queues to manage data from multiple threads effectively, we have been able to contain the program to under 150 lines of code.

####
This project requires [Tkinter](http://tkinter.unpythonic.net/wiki/). This may have come with your python installation, if not, instructions for installing Tkinter can be found [here](http://tkinter.unpythonic.net/wiki/How_to_install_Tkinter).

#### Code Example:
~~~ python
from queue import Queue, Empty
from random import randrange
from threading import Thread
from time import sleep

# The module differs between Python 2 and 3
#from Tkinter import Tk, Button, Canvas # Uncomment for Python 2
from tkinter import Tk, Button, Canvas # Uncomment for Python 3


# colors used when drawing the game
bg_color = '#6960EC'
snake_color = '#E4ED61'
food_color = '#E4ED61'
text_color = 'white'


class GUI(Tk):
    def __init__(self, queue):
        Tk.__init__(self)                                                   # GUI class inherits the Tk class
        self.queue = queue
        self.is_game_over = False
        self.canvas = Canvas(self, width=495, height=305, bg=bg_color)      # initialize the draw canvas
        self.canvas.pack()
        self.snake = self.canvas.create_line((0, 0), (0, 0), fill=snake_color, width=10)        #initialize game objects
        self.food = self.canvas.create_rectangle(0, 0, 0, 0, fill=food_color, outline=food_color)
        self.points_earned = self.canvas.create_text(455, 15, fill=text_color, text='Score: 0')
        self.queue_handler()                                                # call the queue handler which will act as
                                                                            # our main loop, processing queued events
    def queue_handler(self):
        try:
            while True:
                task = self.queue.get(block=False)                          # get the next item in queue

                # in this block of logic, we check the conditions of the game and apply any changes
                if 'game_over' in task:
                    self.game_over()
                elif 'move' in task:
                    points = [x for point in task['move'] for x in point]
                    self.canvas.coords(self.snake, *points)
                elif 'food' in task:
                    self.canvas.coords(self.food, *task['food'])
                elif 'points_earned' in task:
                    self.canvas.itemconfigure(self.points_earned, text='Score: {}'.format(task['points_earned']))
                self.queue.task_done()
        except Empty:
            if not self.is_game_over:
                self.canvas.after(100, self.queue_handler)

    def game_over(self):
        self.is_game_over = True
        self.canvas.create_text(200, 150, fill=text_color, text='Game Over')
        quitbtn = Button(self, text='Quit', command=self.destroy)
        self.canvas.create_window(200, 180, anchor='nw', window=quitbtn)


class Food:                                             # Because we want to process all data centrally from within a
    def __init__(self, queue):                          # queue, we pass the queue as an argument to the Food class.
        self.queue = queue                              # This demonstrates how code executed in the main thread can
        self.generate_food()                            # communicate with attributes and methods from other threads!

    def generate_food(self):                            # generate_food generates a random position on the canvas.
        x = randrange(5, 480, 10)
        y = randrange(5, 295, 10)
        self.position = x, y                            # However, because this point is just a small point on the
        self.exppos = x - 5, y - 5, x + 5, y + 5        # canvas, it would be barely visible. Therefore, we generate
        self.queue.put({'food': self.exppos})           # an expanded coordinate range within five values lower and
                                                        # higher than the original coordinates. This is easily visible.


class Snake(Thread):                                    # To demonstrate multi-threading, we implement our Snake class
    def __init__(self, gui, queue):                     # to work from a separate thread.
        Thread.__init__(self)
        self.gui = gui
        self.queue = queue
        self.daemon = True
        self.points_earned = 0                          # Initialize the score points to zero.
        self.snake_points = [(495, 55), (485, 55), (475, 55), (465, 55), (455, 55)] # The initial position of our Snake
        self.food = Food(queue)
        self.direction = 'Left'                         # Set our Snake's initial direction to left.
        self.start()                                    # Start our new Worker Thread

    def run(self):                                      # This method overrides the Thread's run() method and was set
        while not self.gui.is_game_over:                # in motion when we called start() in Snake. It begins an
            self.queue.put({'move': self.snake_points}) # infinite loop to call the move() method at small intervals.
            sleep(0.1)                                  # During every loop cycle, the method populates the queue with
            self.move()                                 # a 'move' value equal to our Snake's updated position.

    def move(self):
        new_snake_point = self.calculate_new_coordinates() # move() obtains the latest coordinates of the snake
        if self.food.position == new_snake_point:          # check if the new snake point is the same as Food's position
            self.points_earned += 1                        # if so, increment the score and add an item to queue to
            self.queue.put({'points_earned': self.points_earned})  #update the GUI on the main thread.
            self.food.generate_food()                      # Generate a new Food object.
        else:
            self.snake_points.pop(0)                       # If not, pop() removes the last the last item from the snake
        self.check_game_over(new_snake_point)              # coordinates.
        self.snake_points.append(new_snake_point)

    def key_pressed(self, e):
        self.direction = e.keysym

    def calculate_new_coordinates(self):
        last_x, last_y = self.snake_points[-1]
        if self.direction == 'Up':
            new_snake_point = last_x, (last_y - 10)
        elif self.direction == 'Down':
            new_snake_point = last_x, (last_y + 10)
        elif self.direction == 'Left':
            new_snake_point = (last_x - 10), last_y
        elif self.direction == 'Right':
            new_snake_point = (last_x + 10), last_y
        return new_snake_point

    def check_game_over(self, snake_point):
        x, y = snake_point[0], snake_point[1]
        if not -5 < x < 505 or not -5 < y < 315 or snake_point in self.snake_points:
            self.queue.put({'game_over': True})


def main():
    queue = Queue()
    gui = GUI(queue)
    snake = Snake(gui, queue)
    gui.bind('<Key-Left>', snake.key_pressed)
    gui.bind('<Key-Right>', snake.key_pressed)
    gui.bind('<Key-Up>', snake.key_pressed)
    gui.bind('<Key-Down>', snake.key_pressed)
    gui.mainloop()


if __name__ == '__main__':
    main()
~~~
