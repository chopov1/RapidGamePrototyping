An attempt at creating an Indie Horror Game

https://ookii-tsuki.itch.io/teke-teke-moonlit-dread

With the timeframe of two weeks, and 4 college students having lots of other work, we knew we needed small scope for the Chicaghoul game jam. 

The idea is to make a small indie horror experience that doesnt have much code and is bassicly a walking simulator. The challenge then is to emulate this retro style that has become common with indie hits like Janitor Bleeds or Teke Teke which is the screenshot below.
![Alt text](<Screenshot 2023-10-15 194927-1.png>)

These games emulate ps1 style graphics in a 3d space, and are bassicly a walking simulator with jump scares.

The game was for a chicago game jam and the idea we came up with was a spooky trip on the cta. You would wait in the station for a bit, interact with some npc's, then get on the train as you try to go home. The train would end up stopping and you would need to make your way through the train cars in order to get to the front car, where you find the conductor possessed and theres a final jumpscare. 

## Thursday October 5th, 2023

The first step was to find a way to emulate that pixelated feel in 3D within the unity engine. 

A quick way to do this was with a render texture. It bassicly just downsamples the rendering of the scene at the final step of drawing to thescreen. 
The resolution of the texture can be set to desired value.
![Alt text](<Screenshot 2023-10-15 195442-1.png>)

The camera is set to display the render texture rather then the game. So the camera feeds what it sees to the texture, then displayes it to the viewport.
![Alt text](<Screenshot 2023-10-15 195432-1.png>)

So instead of this
![Alt text](<Screenshot 2023-10-15 195401-1.png>)

we get this
![Alt text](<Screenshot 2023-10-15 195341-1.png>)


[Video On How To Do Render Texture Pixel Effect](https://www.youtube.com/watch?v=Sru8XDwxC3I)

I also spent alot of time looking at interesting VHS camera shaders.

[Video that showed me camera shaders](https://www.youtube.com/watch?v=YYNMGq50d5g)

https://github.com/IAMColumbia/ApocolypseTrain/assets/76492881/ad835c0c-751e-4173-b961-4721e68f978e

I was able to achieve this effect with the VHS tape which I found to be informative and a nice introduction to application of shaders, but didnt fit with the theme of our game.

## Thursday October 12, 2023

I put on my c# boots and coded a quick trigger system for our game, the idea was to creare a modular system to allow the designer to setup triggers to allow the player to do things like open doors, trigger an object to move accross the screen for a jumpscares and play spooky audio files. 

https://github.com/IAMColumbia/ApocolypseTrain/assets/76492881/b5ed5f4a-94a0-46b7-9798-c818f620307d

I also started looking deeper into how shaders are made and I tried my hand at writing my own. [I Followed this Tutorial series to make my own](https://www.youtube.com/watch?v=1mWrX0YRtRM)

This really opened my eyes to how much of game polish uses shaders. Alot of things I didnt even know how developers did, I now realize they probobly did through shaders. It is an area of game development I am pretty novice with but I have started to get super excited about. I managed to create this from the tutorial

https://github.com/IAMColumbia/ApocolypseTrain/assets/76492881/6126ea83-0859-4461-9c54-bf501db2f09e

Next step I think is to look into camera shaders, as my end goal for this game is to create a fog effect using camera shaders. Not sure if ill reach that skill level but I will try.

Another thing to note is that coding shaders in Unity using visual studio sucks. You either get grey text or a ton of red squigglies. From reading forums I discovered this is because unitys shaders use a combination of languages from hlsl to unitys own shader methods. The best solution is to use VSCode, which doesnt have intellisense specific to unity shaders but it has basic type highlighting, spell checking and auto fill which I deffinitly take for granted as a programmer.

![Alt text](<Screenshot 2023-10-15 202245-1.png>)

