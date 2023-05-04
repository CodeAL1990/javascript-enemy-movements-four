# javascript-enemy-movements-four

As usual, copy from the previous movement file(three in this case) and paste the html,css and js to start editting
Change the source image to fourth image type and the spriteWidth and height accordingly
To start off, Remove angle, angleSpeed and curve from the constructor
Set xy to 0 and remove angle in update
Comment out xy in update
Add a newX and newY properties in the constructor and randomise them from 0 to canvas.width and height respectively
Add an if condition in update using the modulus where it will invoke whenever every 30 gameFrames has passed, set newX and newY to a different random position
Initialize variables dx and dy after the gameFrame if condition where dx is the distance between x and newX and vice versa for y
To make your sprites move towards the new position, you can decrement x and y by dx and dy respectively
Every 30 gameFrames seems too fast, you can change it to a higher value to make it slower
By dividing the assignment of dx and dy by lets say 20, your sprites will move 1/20 of the full distance in dx and dy respectively
With the current setup, all sprites reset at the exact same time where in a game you want them to be independent of each other
Add a property called interval in constructor and randomise it between lets say 50 to 250
Replace the hardcoded number in the gameFrame calculation to interval
Since the modulus operator requires a whole number and randomised numbers gives you decimal, wrap the calculation of interval in Math.floor to get whole numbers
And it is done! (for now)
