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
<li>Project 3: Maze Generator</li>
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

---

# Project 3:  Maze generator

Difficulty Level: Moderate

Language: Javascript

## Description: 
Javascript Maze generator. Introduction to canvas and multi-dimensional arrays


## The Steps

- You will need three text files for this game, one for the HTML, one for CSS, and one for the actual Javascript. If using [jsfiddle](http://jsfiddle.net), three boxes are available to enter in.

### HTML:

~~~ html
<div>
  <canvas></canvas>
  <ul>
    <li><label>Width:</label><input id=width type="text"/></li>
    <li><label>Height:</label><input id=height type="text"/></li>
    <li><label>Path Width:</label><input id=pathwidth type="text"/></li>
    <li><label>Wall Width:</label><input id=wallwidth type="text"/></li>
    <li><label>Outer Width:</label><input id=outerwidth type="text"/></li>
    <li><label>Path Color:</label><input id=pathcolor type="text"/></li>
    <li><label>Wall Color:</label><input id=wallcolor type="text"/></li>
    <li><label>Seed:</label><input id=seed type="text"/></li>
    <li><input id=randomseed type="button" value="Random Seed"/></li>
  </ul>
</div>
~~~

### CSS:

~~~ CSS
body{
  margin: 0;
  background: blue;
  text-align: center;
}
div{
  display: inline-block;
  margin: 20px auto 0 auto;
  position: relative;
}
ul{
  position: absolute;
  right: 0;
  width: 220px;
  height: 100%;
  float: left;
  list-style: none;
  padding: 0;
  margin: 0;
  text-align: left;
  color: #eee;
}
li{
  padding: 5px 5px 5px 5px;
}
label{
  width: 50%;
  display: inline-block;
  box-sizing: border-box;
  text-align: right;
  padding-right: 5px;
  text-shadow: 2px 2px 0px rgba(0,0,0,0.2);
}
input{
  width: 50%;
  height: 24px;
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  border: none;
  background: #ccc;
  color: #333;
  font-weight: bold;
  text-align: center;
  border-radius: 2px;
  transition: background 200ms;
  box-shadow: 2px 2px 0px rgba(0,0,0,0.2);
}
input:focus{
  outline: none;
  background: #fff;
  color: #222;
}
input[type=button]{
  background: #111;
  color: #eee;
  margin-left: 50%;
  font-weight: normal;
  cursor: pointer;
}
input[type=button]:active{
  transform: translate(2px,2px);
  box-shadow: 0px 0px 0px rgba(0,0,0,0.2);
}
canvas{
  margin-right: 220px;
  display: block;
  float: left;
}
~~~

### Javascript:

If using [jsfiddle](http://jsfiddle.net), choose LOAD TYPE No wrap - in \<body\> under the gear menu.

~~~ javascript
pathWidth = 10       //Width of the Maze Path
wall = 2             //Width of the Walls between Paths
outerWall = 2        //Width of the Outer most wall
width = 25           //Number paths fitted horisontally
height = 25          //Number paths fitted vertically
delay = 1            //Delay between algorithm cycles
x = width/2|0        //Horisontal starting position
y = height/2|0       //Vertical starting position
seed = Math.random()*100000|0//Seed for random numbers
wallColor = 'black'  //Color of the walls
pathColor = 'purple'  //Color of the path

randomGen = function(seed){
	if(seed===undefined)var seed=performance.now()
	return function(){
    seed = (seed * 9301 + 49297) % 233280
		return seed/233280
	}
}

init = function(){
  offset = pathWidth/2+outerWall
  map = []
  canvas = document.querySelector('canvas')
  ctx = canvas.getContext('2d')
  canvas.width = outerWall*2+width*(pathWidth+wall)-wall
  canvas.height = outerWall*2+height*(pathWidth+wall)-wall
  ctx.fillStyle = wallColor
  ctx.fillRect(0,0,canvas.width,canvas.height)
  random = randomGen(seed)
  ctx.strokeStyle = pathColor
  ctx.lineCap = 'square'
  ctx.lineWidth = pathWidth
  ctx.beginPath()
  for(var i=0;i<height*2;i++){
    map[i] = []
    for(var j=0;j<width*2;j++){
      map[i][j] = false
    }
  }
  map[y*2][x*2] = true
  route = [[x,y]]
  ctx.moveTo(x*(pathWidth+wall)+offset,
             y*(pathWidth+wall)+offset)
}
init()

inputWidth = document.getElementById('width')
inputHeight = document.getElementById('height')
inputPathWidth = document.getElementById('pathwidth')
inputWallWidth = document.getElementById('wallwidth')
inputOuterWidth = document.getElementById('outerwidth')
inputPathColor = document.getElementById('pathcolor')
inputWallColor = document.getElementById('wallcolor')
inputSeed = document.getElementById('seed')
buttonRandomSeed = document.getElementById('randomseed')

settings = {
  display: function(){
    inputWidth.value = width
    inputHeight.value = height
    inputPathWidth.value = pathWidth
    inputWallWidth.value = wall
    inputOuterWidth.value = outerWall
    inputPathColor.value = pathColor
    inputWallColor.value = wallColor
    inputSeed.value = seed
  },
  check: function(){
    if(inputWidth.value != width||
       inputHeight.value != height||
       inputPathWidth.value != pathWidth||
       inputWallWidth.value != wall||
       inputOuterWidth.value != outerWall||
       inputPathColor.value != pathColor||
       inputWallColor.value != wallColor||
       inputSeed.value != seed){
      settings.update()
    }
  },
  update: function(){
    clearTimeout(timer)
    width = parseFloat(inputWidth.value)
    height = parseFloat(inputHeight.value)
    pathWidth = parseFloat(inputPathWidth.value)
    wall = parseFloat(inputWallWidth.value)
    outerWall = parseFloat(inputOuterWidth.value)
    pathColor = inputPathColor.value
    wallColor = inputWallColor.value
    seed = parseFloat(inputSeed.value)
    x = width/2|0
    y = height/2|0
    init()
    loop()
  }
}

buttonRandomSeed.addEventListener('click',function(){
  inputSeed.value = Math.random()*100000|0
})

loop = function(){
  x = route[route.length-1][0]|0
  y = route[route.length-1][1]|0
  
  var directions = [[1,0],[-1,0],[0,1],[0,-1]],
      alternatives = []
  
  for(var i=0;i<directions.length;i++){
    if(map[(directions[i][1]+y)*2]!=undefined&&
       map[(directions[i][1]+y)*2][(directions[i][0]+x)*2]===false){
      alternatives.push(directions[i])
    }
  }
  
  if(alternatives.length===0){
    route.pop()
    if(route.length>0){
      ctx.moveTo(route[route.length-1][0]*(pathWidth+wall)+offset,
                 route[route.length-1][1]*(pathWidth+wall)+offset)
      timer = setTimeout(loop,delay)
    }
    return;
  }
  direction = alternatives[random()*alternatives.length|0]
  route.push([direction[0]+x,direction[1]+y])
  ctx.lineTo((direction[0]+x)*(pathWidth+wall)+offset,
             (direction[1]+y)*(pathWidth+wall)+offset)
  map[(direction[1]+y)*2][(direction[0]+x)*2] = true
  map[direction[1]+y*2][direction[0]+x*2] = true
  ctx.stroke()
  timer = setTimeout(loop,delay)
}
settings.display()
loop()
setInterval(settings.check,300)
~~~
