An attempt at creating an Indie Horror Game

https://ookii-tsuki.itch.io/teke-teke-moonlit-dread

With the timeframe of two weeks, and 4 college students having lots of other work, we knew we needed small scope for the Chicaghoul game jam. 

The idea is to make a small indie horror experience that doesnt have much code and is bassicly a walking simulator. The challenge then is to emulate this retro style that has become common with indie hits like Janitor Bleeds or Teke Teke which is the screenshot below.
![Alt text](<Screenshot 2023-10-15 194927-1.png>)

These games emulate ps1 style graphics in a 3d space, and are bassicly a walking simulator with jump scares.

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
The model I used in the video was the same free asset used by Teke Teke and many other indie horror games.

## Thursday October 12, 2023

I put on my c# boots and coded a quick trigger system for our game, the idea was to creare a modular system to allow the player to trigger things like openeing doors, jumpscares, and audio files.
