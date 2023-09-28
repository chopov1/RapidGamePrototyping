//ctrl + shift + v to view MD from vscode

### Top Down Shooter




I took alot of inspiration from dead ops arcade 2 when looking at fps mechanics. 
In dead ops arcade it feels like they use raycast shooting, and upon research I found all the call of duty games use hitscan for most weapons, aside from rockets or snipers which use projectiles as they can be slower and or have bullet drop.
I also played and looked at fortnite which is not top down but is a shooter made in unreal engine, and I found similar information about the shooting mechanics. 

![Alt text](jB1dTwR.png)

My hitscan system
* when player holds the shoot button
* start a looping timer, that repeats every X seconds (x = fire rate)
* every time the timer completes, cast a ray
* if the ray hits an enemy actor, call that actors TakeDamage method

![Alt text](ezgif.com-optimize.gif)

(If the red line looks constant that is due to low frames of gif)

The next problem to overcome was how to visualize this ray.

<video src="New%20Project.mp4" controls title="Title"></video>

In dead ops arcade, I figured they spawn a particle effect along the ray. I took the same approach and got something similar. I didnt like how the bullets in dead ops arcade stayed in the same place so it was hard to tell if they were moving. I made sure that wasnt present in mine. 

<video src="Untitled%20video%20-%20Made%20with%20Clipchamp%20(3).mp4" controls title="Title"></video>
