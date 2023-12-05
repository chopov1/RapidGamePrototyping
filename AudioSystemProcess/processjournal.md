
I began the day with the intention of implementing some audio assets I created into an fps game in unity. 
I had created an asset that I wanted to play when a projectile shot by the player explodes. 

![Alt text](<Screenshot 2023-12-04 205558.png>)

When it explodes, it destroys itself, so if it was the one to play the sound the sound would be destoryed with it. 

Two ways to go about this,  is to use AudioSource.PlaySoundAtPoint() or to spawn another gameobject to handle playing the sound.

PlaySoundAtPoint did not fit my needs as the only contorl this method offers is initial volume. I want to set attenuation settings, send audio to mixer groups, randomize pitch to create variation, etc.

Spawning an object works, but now we are left with abunch of audio sources all over the scene that have finished playing and are just sitting there. We could create a script to get the length of the audio clip from the audio source on the game object and destroy itself when its done playing, but now if we have a reverb tail that is playing it will cut off abrubtly and sound terrible. 

It is also not the most performant to keep spawning in a new object every time I want to play a sound from a projectile and cleaning them up, especially in an arena shooter where projectiles are constantly flying all over the place. 

My solution to this was to create a WorldAudioManager that uses the object pooling pattern to play audioclips using custom audio player objects.

The world audio manager creates a queue of audio player scripts and populates it with a specified number of objects, attaching that script and an audio source to them.

![Alt text](<Screenshot 2023-12-04 213631.png>)


It uses the singleton pattern so that any script can play a sound. 

When it came to implementing the audio for the player I created a playeraudio manager. This is because I needed specific functionality that I did not want to store in the world audio manager. 

I had the player audio manager use the singleton pattern as well, but instead of taking in clips it would just take in a string for an ID of the audio to play. The ID would be used to lookup an Audio Data struct to play which contained the random files to choose from, as well as other properties specific to that "audio event". This way I can specifiy properties for each event, without needing to touch the code. It also minimized code as I dont need to pass all this data arbitrarily through a function and store it in lots of places.

![Alt text](<Screenshot 2023-12-04 205340.png>)


