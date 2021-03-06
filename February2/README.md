# Assignment 2: Computer Graphics and Art

<p float="left">
  <img src="Images/mouseLeft.png" width="320">
  <img src="Images/mouseMid.png" width="320">
  <img src="Images/mouseRight.png" width="320">
</p>
From left to right: mouseX on the left most, mouseX in the middle, mouseX on the right most.

## Description
For this assignment, I decided to create an interactive grid of squares with various shades of grey that varies in size based on the X position of the mouse. The greater the X position, the more range the size may vary over, increasing the "noise" in the image. My initial idea involved drawing overlapping rectangles of different sizes at random locations. However, I wanted to make better use of the whole canvas so I thought about how I could organize the rectangles in a way such that they would be relatively evenly-spaced. I then wanted to introduce some disorder so I added a random() component to the rectangle width and height. In order to make the piece interactive, I decided to make it so that the user can control the degree of randomness.

## Process
1. Created the grid using nested for() loops to set the X and Y position of each rectangle
2. Randomized the grey color in each square and decreased the opacity so any overlapping can be seen
3. Added a random() range in the rectangle width and height to create some disorder in the grid
4. Made the degree of disorder controllable by mapping the mouseX position

## Challenges
My main challenge was in figuring out the rectMode(), the rectangle position translation, and the random() values together as I wanted to make sure that the background will not be seen through the rectangles at all. In my first attempt I was used rectMode(CORNER) which meant that varying the width and height would make the rectangles overlap to the right and bottom and I felt that it still looked too ordered. I also set the bottom range of the random() function to a negative  number which ended up revealing the background when the shape would shrink. I played around with these components a little and ended up changing the rectMode() to "CENTER", translating it by the half the size of the default square size, and keeping the lower range of random() at 0.
