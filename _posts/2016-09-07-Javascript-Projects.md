---
layout: post
title: Javascript Projects
---

Dinner and Code currently offers two programming paths: Python and
javascript development. On this page are the Javascript projects.

<em>Javascript is an object-oriented computer programming language commonly used to bring interaction to websites</em>

# Project Listing
<ol>
<li>Project 1: Dice Rolling Game</li>
<li>Project 2: Tip Calculator</li>
</ol>

<em>All of the projects are listed on this page. Keep scrolling to see more.</em>

---


# Project 1: Dice Rolling Program
Difficulty Level: Beginner

Language: Javascript

## Description:
This basic dice rolling program will let you get comfortable with coding in Javascript. Two dice are created and a button to roll them. An event listener is created in our script to "watch" for the button to be clicked. When clicked, two random numbers are generated, and the dice are updated.

## The Steps

* You will need three text files for this game, one for the HTML, one for CSS, and one for the actual Javascript. If using [jsfiddle](http://jsfiddle.net), three boxes are available to enter in.

### HTML:

~~~ html
<div class="wrapper">
		<div class="column">
				<div id="dice-side-1" class="dice">0</div>
				<div id="dice-side-2" class="dice">0</div>
		</div>
		<div class="column">
				<button type="button" class="dice-roll">roll dice</button>
				<h2 id="status"></h2>
		</div>
</div>
~~~

### CSS:

~~~ css
body {
    position: relative;
}

.wrapper {
    width: 400px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
}

.column {
    display: flex;
    align-items: center;
}

#status {
    position: absolute;
    top: 5rem;
		left: 50%;
		transform: translateX(-50%);
    min-width: 400px;
    margin: 0;
		text-align: center;
}

.dice {
    width: 32px;
    float: left;
    background-color: lightcoral;
    border: 1px solid black;
    padding: 10px;
    font-size: 24px;
    text-align: center;
    margin: 5px;
    border-radius: 5px;
}

.dice-roll {
    cursor: pointer;
    text-transform: capitalize;
}
~~~

### Javascript:

If using [jsfiddle](http://jsfiddle.net), choose LOAD TYPE No wrap - in \<body\> under the gear menu.

~~~ javascript
window.addEventListener('DOMContentLoaded', function () {
    function rollDice () {
        var diceSide1 = document.getElementById('dice-side-1');
        var diceSide2 = document.getElementById('dice-side-2');
        var status = document.getElementById('status');

        var side1 = Math.floor( Math.random() * 6 ) + 1;
        var side2 = Math.floor( Math.random() * 6 ) + 1;
        var diceTotal = side1 + side2;

        diceSide1.innerHTML = side1;
        diceSide2.innerHTML = side2;

        status.innerHTML = 'You rolled ' + diceTotal + '.';

        if ( side1 === side2 ) {
            status.innerHTML += ' Doubles! You get a free turn!';
        }
    }

    var buttonRoolDice = document.querySelector('.dice-roll');
    buttonRoolDice.addEventListener('click', rollDice, false);
}, false);
~~~



---

# Project 2:  Tip Calculator

Difficulty Level: Beginner

Language: Javascript/jQuery

## Description:
Tip calculator for wait staff. This project will teach you basics in creating functions and using variables.

## The Steps

- You will need three text files for this game, one for the HTML, one for CSS, and one for the actual Javascript. If using [jsfiddle](http://jsfiddle.net), three boxes are available to enter in.
- You will also need to include [JQuery](https://jquery.com) for this project. In [jsfiddle](http://jsfiddle.net) under External Resources, enter https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js under JavaScript/CSS URI and click the + icon.

### HTML:

~~~ html
<div class="wrapper">
		<h1 class="wrapper__title">Javascript Tip Calculator</h1>
		<form class="calculator">
				<div class="calculator__row">
						<label for="bill">Enter the bill amount for your meal: $</label>
						<input type="text" id="bill" class="calculator__bill" value="5" required/>
				</div>
				<div class="calculator__row">
						<label for="tip">Tip amount: <span class="tip-amount"></span></label>
						<input type="range" min="0" max="100" value="0" step="1" class="calculator__tip" id="tip" required/>
				</div>
				<div class="calculator__row">
						<h2 class="calculator__info">Tip to leave: <span class="calculator__result"></span></h2>
				</div>
		</form>
</div>
~~~

### CSS:

~~~ css
.wrapper {
    width: 800px;
    margin: 50px auto 0;
    padding: 60px 30px;
    border: 1px solid #000;
}

.wrapper__title {
    text-transform: capitalize;
    margin: 0 0 40px;
}

.calculator__row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0 0 30px;
}

.calculator__row:last-child {
    margin-bottom: 0;
}

.calculator__row label {
    text-transform: capitalize;
    font-weight: 700;
}

.calculator__bill {
    width: 50%;
}

.calculator__tip {
    width: 60%;
}

.calculator__info {
    text-transform: capitalize;
    margin: 0;
}
~~~

### Javascript:

If using [jsfiddle](http://jsfiddle.net), choose LOAD TYPE No wrap - in \<body\> under the gear menu.

~~~ javascript
$(document).ready( function () {
    var amount, percent, result;
    var calculator = $('.calculator');
    var calculatorBill = calculator.find('.calculator__bill');
    var calculatorTip = calculator.find('.calculator__tip');
    var calculatorResult = calculator.find('.calculator__result');
    var tipAmount = calculator.find('.tip-amount');

    // Initialize bill
    $(window).on('DOMContentLoaded', function () {
        tipAmount.text( calculatorTip.val() + '%' );
        amount = calculatorBill.val() * 1;
        percent = calculatorTip.val() * 1;
        result = amount + amount * ( percent / 100 );
        calculatorResult.text( result.toFixed(2) + '$' );
    });

    calculatorTip.on('change', function () {
        if ( calculatorBill.val() === '' || isNaN( calculatorBill.val() ) ) {
            alert('Enter bill amount, please!')
        } else {
            amount = calculatorBill.val() * 1;
        }

        tipAmount.text( calculatorTip.val() + '%' );
        percent = calculatorTip.val() * 1;
        result = amount + amount * ( percent / 100 );
        calculatorResult.text( result.toFixed(2) + '$' );
    });
});
~~~

