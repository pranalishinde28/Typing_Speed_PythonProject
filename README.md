# Typing Speed Python Project
Background.jpg – A background image we will use in our program
Icon.png – An icon image that we will use as a reset button.
Sentences.txt – This text file will contain a list of sentences separated by a new line.
Speed typing.py – The main program file that contains all the code
Typing-speed-open.png – The image to display when starting game

Used an Object-oriented approach to build the program.
Imported the libraries along with some built-in modules of Python like time and random library.
Created the game class which will involve many functions responsible for starting the game, resetting the game and few helper functions to perform calculations that are required for this project in Python.
In the constructor, we have initialized the width and height of the window, variables that are needed for calculation and then initialized the pygame and loaded the images. The screen variable is the most important on which we will draw everything.
The draw_text() method of Game class is a helper function that will draw the text on the screen. The argument it takes is the screen, the message we want to draw, the y coordinate of the screen to position our text, the size of the font and color of the font. We will draw everything in the center of the screen. 
get_sentence() method will open up the file and return a random sentence from the list. then will split the whole string with a newline character.
The show_results() method is where we calculate the speed of the user’s typing. The time starts when the user clicks on the input box and the user hits return key “Enter” then it performs the difference and calculate time in seconds.
To calculate accuracy, we have to apply a little bit of math : The formula for accuracy is:

(correct characters)x100/ (total characters in sentence)

The WPM is the words per minute. A typical word consists of around 5 characters, so we calculate the words per minute by dividing the total number of words with five and then the result is again divided that with the total time it took in minutes. Since our total time was in seconds, we had to convert it into minutes by dividing total time with 60.

We call the reset_game() method at the starting of this method which resets all the variables. Next, run an infinite loop which will capture all the mouse and keyboard events. Then, we draw the heading and the input box on the screen.
We then use another loop that will look for the mouse and keyboard events. When the mouse button is pressed, we check the position of the mouse if it is on the input box then we start the time and set the active to True. If it is on the reset button, then we reset the game.
When the active is True and typing has not ended then we look for keyboard events. If the user presses any key then we need to update the message on our input box. The enter key will end typing and we will calculate the scores to display it. Another event of a backspace is used to trim the input text by removing the last character.

The reset_game() method resets all variables so that we can start testing our typing speed again. We also select a random sentence by calling the get_sentence() method. In the end, we have closed the class definition and created the object of Game class to run the program.

