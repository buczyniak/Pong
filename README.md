# Pong
![pong](https://github.com/buczyniak/Pong/assets/78871310/f0948ef3-3d3e-489e-8f01-9f81a39a9d64)

## Introduction
Pong is an early and iconic video game developed by Atari in 1972. It simulates a table tennis match, where 
players control paddles moving vertically to hit a ball back and forth. The objective is to score points by 
preventing the ball from passing behind the paddles. Pong's simple and minimalist gameplay, along with its 
monochromatic graphics, made it a commercial success and a symbol of the gaming industry's beginnings. Despite 
its basic design, Pong's enduring legacy has influenced countless games and continues to remind us of the timeless 
appeal of classic video gaming.

The code is a classic example of an Object-Oriented Programming (OOP) implementation, where the game entities 
(ball, paddles, and scoreboard) are represented as classes with attributes and methods. OOP allows for better 
organization, reusability, and modularity of code, making the Pong game easy to maintain and extend. Players can 
control the paddles using keyboard inputs, and the game continues until one player wins by reaching a set score. 
The game's graphical elements are handled using the Turtle library, which provides a simple and interactive way 
to build 2D graphics and games in Python.

The Pong was created while taking a [Udemy course](https://www.udemy.com/course/100-days-of-code/).

## Explanation of the Code

1. main.py
   
    This is the main script that runs the Pong game and sets up the game environment.
    
    * Screen Setup: It initializes the game screen using the Turtle's Screen class. The screen has a width of 800
      pixels and a height of 600 pixels. The background color is set to black, and tracer(0) is used to turn off
      animation updates.
    * Paddles and Ball: Two paddles and a ball are created using the classes defined in paddle.py and ball.py.
    * Moving the Paddles: The script listens for user keyboard inputs to move the paddles up and down.
    * Game Loop: The game loop (while game_is_on) keeps the game running. It controls the ball movement and checks
      for collisions with walls, paddles, and score updates.

2. ball.py
   
    This file contains the Ball class, which represents the ball object in the Pong game.
    
    * Attributes: The ball has attributes for its shape (a circle), color (white), and initial movement speed in 
    the x and y directions.
    * Methods:
      * move(): Updates the ball's position based on its current x and y movement values.
      * bounce_y(): Changes the ball's y movement direction to simulate bouncing off the top or bottom wall.
      * bounce_x(): Changes the ball's x movement direction to simulate bouncing off the paddles and increases its speed 
        slightly with each bounce.
      * reset_position(): Resets the ball to the center of the screen after a player scores.

3. paddle.py
   
    This file contains the Paddle class, which represents the paddles used by players in the Pong game.
    
    * Attributes: Each paddle has a shape (a square), color (white), and size (5 times taller than wide).
    * Methods:
      * go_up(): Moves the paddle up by adjusting its y-coordinate.
      * go_down(): Moves the paddle down by adjusting its y-coordinate.

4. scoreboard.py
   
    This file contains the Scoreboard class, which represents the scoreboard in the Pong game.
    
    * Attributes: The scoreboard has a yellow color and uses the "Courier" font with a size of 50.
    * Methods:
      * update_scoreboard(): Clears the scoreboard and updates the scores for both players.
      * l_point(): Increases the left player's score and updates the scoreboard.
      * r_point(): Increases the right player's score and updates the scoreboard.
