## Adding a bouncing ball

Let's make the game a bit more exciting by adding a bouncing ball!
Toby has to catch the ball. If Toby drops 3 balls before he has time to collect his 5 bowls of cheese-puffs, the game is over!



+ Add a new sprite: select the **Beachball** from the Scratch library.

+ Shrink the **Beachball**. Make sure that the centre of the costume is set correctly, i.e. at the centre of the ball. You can check this by clicking on the **Set costume centre** icon, located at the top right corner in the **Costumes** tab. It is important to set the centre correctly, as it will affect the way the ball moves.

+ Now we need this ball to fall from the sky, and bounce everywhere. Add the following script to your ball:

	```blocks
		when FLAG clicked  
		show
		go to x:(pick random (-220) to (220)) y:(160)
		point in direction (135 v)
		forever
		move (4) steps
		if on edge, bounce
		end
	```

## Test Your Project

__Click the green flag__, your ball should fall from the sky and bounce off the edges of the background. Which number do you need to modify to make the ball bounce faster or slower?



