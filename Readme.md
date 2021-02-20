Javascript Graphing Calculator
==============================

# Introduction
In this exercise we will be creating a simple javascript graphing calculatormake sure the graph is erased before plotting new functions application. The end product will take a mathematical equation, along with the bounds on which to graph the equation. A series of points along the curve will be calculated, returned and plotted. in addition a delta x (dx) term will be input as well that describes how often these points will be graphed. (more on all of this later) 

This exercise will help you better understand the following topics

1. The relationship between html, Javascript, and CSS
2. Animations and graphics with html5 Canvas
3. javascript functions, loops, and math operations
4. Html form data (user inputs)
5. Using External javascript Libraries
6. Git and Github

The documentation for this exercise will not be extensive and this is on purpose. Just like in real world projects, you will be expected to use outside sources to complete certain parts of the project, but you can always contact me if needed.

# Procedure
The sections of this exercise are meant to be completed one at a time and after each section you should post your code to Github so it can be reviewed

## Step 1 - Configuring Github (1-2 hr)
1. Watch a few videos on youtube that describe what Git is and install / configure it on your machine.
2. Create a Github account so you can post your code for review (if you dont know the difference between git and GitHub then watch more videos or contact me directly)
3. To test that github is installed and working properly - create a new repository named 'myFirstGit'. 
4. Create a Readme.md (md stands for markdown - give it a google if unfamiliar). Commit and push your changes to your GitHub for review.

## Step 2 - Getting started with the exercise(10 min)
5. Fork THIS gitHub repository (see youtube to learn what forking is)
6. in the responses directory - create a response_1.txt file with your name in it. commit and push the changes for review.

## Step 3 - Simple Edits (15 min)
1. Edit the index.html and add a large title above the html canvas.
2. Edit the script.js to get not just the x1 value from the form, but all of the inputs from the form. 
3. Edit the style.css to change the background of the body of the page to a light gray color. 
4. Use css and HTML to center the new title you created in the html
5. commit all changes and push to repository for review

## Step 4 - Validating user input with if/else and math(1 hr)
Currently the input that you are using in the script.js has not been validated in any way. In this section you will make sure the input values meet the following criteria:

1. x1, x2 are rational numbers
2. x1 < x2
3. 0 < dx < |x1-x2|

Preform all of these validations in the graph function in the script.js file.

If any inputs fail to meet these criteria then alert the user using the alert() method (look it up) and break out (reurn from) the graph function

when finished, commit and push all changes to github for review.

## Step 5 - Regex practice (1 hr)
1. Watch a few youtube videos on regex and be familiar with text pattern searching
2. Create a function getEvalString in script.js
   - that takes 2 args:
      1. a string in the form "x+2" (can be any math expression with x as variable but should not contain an = sign)
      2. a number to replace x with in the expression example: 7
   - and returns a string "(7)+2" **make sure to surround your inputed number with parenthesis**
   - **USE REGEX** even though its overkill to make this function 
3. Obligatory commit and push all changes to github (will omit this step from all further section instructions - but do not forget to do this going forward)

## Step 6 - CALCULATIONS (3 hr)
1. Create a function getCalculations that accepts all of the inputs x1, x2, dx, and fx as inputs.
2. Use a for loop starting at x1, ending at x2 and stepping by dx to calculate all the fx values and return ordered pairs as an array. the getEvalString function you created and the eval() (google eval function) function will be useful here.
3. Create 2 other functions (getMin & getMax) that accept the output of getCalculations and returns the min and max fx values

## Step 7 - Coordinate Systems (3 hr)
The html 5 canvas has a coordinate system with (0,0) in the top left of the canvas and (500,500) in the bottom right corner

Create a function convertCoords that accepts the output of the getCalculations function (which will be contained within the coordinates (x1, getMax) in the top left, and (x2, getMin) in the bottom right) and scale it to match the coordinates of the html5 canvas coordinate system

convertCoords( [[-10, -10],[0, 0],[10, 10]] should return [[0, 500],[250, 250],[500, 0]]

## Step 8 - GRAPHING (1 hr)
Create a function plotCoords that takes the output of the convertCoords functsion as input and plots small squares on the html canvas arround each coordinate. 

(use a for loop to go through each coordinate and search google how to draw rectangles on html canvas for each coordinate)

## Step 9 - Clean It Up (Unlimited)

Do everything that you can to make the application look pretty. 

make sure you commit and push after making small changes that are related to single issues. You should not style the entire page and build in tons of new stuff before commiting. Smaller commits are easier for others to review and make it **MUCH** easier for you to roll back changes if you accidently break something in the furure.

here are a couple of items to get you started:
1. draw grid lines on the html 5 canvas
2. add an icon to the title bar that looks like a calculator
3. make sure the canvase is erased before plotting new expressions after the graph button is pressed