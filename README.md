# Screensaver
## About the Screensaver
First I set the stars to a list format,I used the `randint` to randomly create the coordinates of the stars within the center of the screen， then I added some three-dimensional parameters of the stars and the color of the stars in new_star to control the stars to fly out in the center of the screen.

`def new_star() -> list:
    star = [0, 0, 0, 0]`

Then in `move_and_check`, first convert the three-dimensional coordinates of the star into two-dimensional coordinates, so that we can check whether the star flies out of the screen. If it flies out of the screen, create a new star, and then determine the distance from the screen. We increase the star's brightness,

Finally, in `draw_star`, draw a circular star based on the position of the star.
At this point, we have initially completed the plan

## Problem
At first I was going to check the brightness of the stars and use this to increase the brightness, but because the brightness of my star was 0 and there was a problem with the coordinate calculation of the star, it could not be displayed on the screen. 

The stars are displayed, but I changed the method to change the brightness of the stars by detecting their position from the screen. And changed the way the coordinates are calculated, and solved it.

## Addition
I added some slowly moving meteorites and a fixed position sun placed in the upper left corner.

For the meteorite part, since the meteorite is a two-dimensional image, I deleted the function that checks the distance relative to the stars, and did not consider the z-axis, so I added the `draw.circle` function to draw the meteorite.

For the sun part, use the `draw.circle` function to draw a yellow sun located in the upper left corner and it will not move.
