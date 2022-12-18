# PROJECT Report

Author: Adam Gerrish

Date: 2022-12-06

Check [readme.txt](readme.txt) for course work statement and self-evaluation. 
  

## R1 Proposal (proposal)

### R1.1 Application problem description
 

![proposal](proposal.html)
	

### R1.2 Creativity/new features

Complete? Yes

Add a few words to high light.


### R1.3 Design consideration

Complete? Yes

see proposal


### R1.4 Milestones and schedule

Complete? Yes

see proposal


### R1.5 References

Complete? (Yes/No) 

see proposal


### R1.6 Writing of the proposal

Complete? (Yes/No) 

see proposal


## R2 Design & implementation (programming)

### R2.1 Problem solving and algorithms

Complete? Yes
#### Game Board
THe game board is a 10x10 box of squares. Each square is 70px70p. We used GL_LINE_LOOP in a for loop to create each of the 100 boxes. For each inner box we use a function that we created that takes a string and turns it into a bitmap. Using this we placed a number in each of the boxes to indicate positions on the board.
[Game Board](images/gameboard.png){width=90%}

#### Pawns and pawn movement:
Pawns are created using GL_POLYGON. The function takes all verticies as parameters and uses glVertex to create the players pawn. This allows us to re use the function and re-draw the pawn whenever the player needs to move their piece.
[Pawns](images/pawns.png){width=90%}

#### Snakes and Ladders
For our snakes and ladders, we have multiple functions to aid in the drawing and logical process. We created a function for both snake and ladder takes the board space number as a parameter and returns the board space of either the end of the snake or end of the ladder. This allows us to move the pawn to the correct space if they land on either.

To draw the ladders, we used two lines GL_LINES and a function that takes all vertcies as parameters. We created a function that allows you to change the layout of ladders by pressing 'c' on the keyboard.
[Ladders](images/ladders.png){width=90%}

To draw the snakes, we created a function to draw a circle for the snakes head, using GL_LINE_LOOP and GL_POLYGON to fill in the head. This gets positioned on a square on the game board. For the body we looped glVertex2i and passed an array of integers to create a snake-like body down the board. We then used GL_TRIANGLE to draw the tail of the snake.
[Snakes](images/snakes.png){width=90%}

#### Rolling the die
We decided to use a 3D die. We used the math.h library to access rand. We gerenrated a random number 1-6 and displayed a rolling animation of the cube with dice numbers dwarn on each side. This then gives the number of spaces to move the player.
[Die](images/die.png){width=90%}

#### Moving pieces
To move the pieces, we created functions to update pixel positions based on dice roll, if they land on a snake, and if they land on a ladder. We created a loop using glut timer to animate the movement of the pieces.

### R2.2 Completion of the project

Complete? Yes

If Yes, insert a screen shot image to show the completion.

[image caption](images/gameboard.png){width=90%}

### R2.3 New features
Complete? Yes 
#### Bitmap String
We created a function that turns a string variable into a bitmap that allows us to display text on screen. This is used for the UI and numbering of the game board boxes.

[Bitmap String](images/bmp.png){width=90%}

#### glutTimerFunction
We used glutTimerFunction to create a timer that allows us to re draw the pawns and animate movemnts along different verticies

[Glut Timer](images/timer.png){width=90%}

#### In game state changes
We allow the players to change the ladders mid game. This affects both the interface and the game logic. When updated in game, the ladders still have an affect on the game board.

[Ladder Changes](ladderswap/.png){width=90%}

If No, add a short description to describe the issues encountered.

### R2.4 Program design and organization
 
Our program is designed with one main class. Inside we have scructures for snake and ladder.
We have a player class to handle all player activities. From there we have any functions that allow our game to work smoothly.

[Main Code](BoardGame/main.cpp)

## R3 Delivery (document)

### R3.1 Presentation & demonstration

Complete? Yes

Presented in class

### R3.2 Documentation
 

Complete? (Yes/No) 

Add the hyperlinks to the documents. 

![Project Report](project_report.html)
![Presentation Slides](presentation.pdf)
	
### R3.3 Submission packaging

Complete? (Yes/No) 

This package.

**References**

1. CP411 project
2. Add your references if you used any. 
