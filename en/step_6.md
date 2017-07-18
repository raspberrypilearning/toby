## Add more bounce

But the problem is: nothing happens when Toby touches the ball. Let's fix this! 



+ Modify your script so that when the ball touches Toby, it bounces off as well:

	```blocks
		when FLAG clicked  
		show
		go to x:(pick random (-220) to (220)) y:(160)
		point in direction (135 v)
		forever
		move (4) steps
		if on edge, bounce
		if <touching [Toby v]?> then
		turn right (pick random (90) to (270)) degrees
		move (100) steps
	   	end
	 	end
	```

+ We also need to add some code to detect when the ball touches the floor. The ball seems to be touching the floor when its `y position`{:class="blockmotion"} is less than  140. This is an approximate number, and you may need to adjust it, especially if you have chosen a different background. 
We are going to modify the script so that the ball moves back to the top (and changes colour) as soon as it is dropped. Import the **water drop** sound, and modify your script again:

	```blocks
		when FLAG clicked  
		show
 		go to x:(pick random (-220) to (220)) y:(160)
	 	point in direction (135 v)
	 	forever
	   	move (4) steps
	   	if on edge, bounce
	   	if <touching [Toby v]?> then
		turn right (pick random (90) to (270)) degrees
		move (100) steps
	   	end
 	   	if <(y position) < (-140)> then
		change [color v] effect by (25)
		go to x:(pick random (-220) to (220)) y:(160)
		play sound [water drop v]
	   	end
	 	end
	```

## Test Your Project

__Click the green flag__, what happens when the ball is dropped ?
Can you see a new ball falling from the top? Is it a different colour?





