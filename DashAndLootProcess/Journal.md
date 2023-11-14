## Wensday November 8th 

Difficulty scaling was an important feature that needed to be in the game to make it hard. I took the classic zombies appraoch, so as players get farther the zombies health increases.

I created loot crates that players can interact with to get stat upgrades. 

https://github.com/IAMColumbia/ApocolypseTrain/assets/76492881/18c5e08e-8080-4148-b377-58e687125e70

The problem with the way the difficulty scales, is that if you dont get a damage upgrade the game gets very hard. I think one way to solve this would be to give the players more choice when it comes to these upgrades. 

I think these loot boxes start to solve two problems the game has which are it needs more choices for the players, and it needs rewards to motivate the player. As of right now though and through various playtests it seems the loot boxes dont provide that much motivation, as they dont drastically change the game. The only choice they really give is who gets to get the loot box, which does encourage player interaction. It creates competition or communication about who gets it.

## Saturday November 11th

I wanted to add a dodge mechanic, as in terms of actions the player had there was only one choice so far. I felt this would give more choices to the player which makes the game more interesting. Ideally I would mimic overcooked for this. 

![Alt text](overcooked-chef.gif)

Originally I had the dodge based on the aiming direction of the player. This worked well in overcooked as movement and aim are linked. However, with the twin stick control fo the current game, linking dodge to aim felt awkward. Being able to shoot one direction and dash in another felt much more powerful and like I had more control over the character. This also felt more intutive as having left stick handles all movement related inputs.

![Alt text](UnrealEditor_U0MXTrI3yv.gif)

I felt the dodge was not very fun on its own. It needed some interactions. The player would always get trapped in between lots of zombies, so using the dodge to knock zombies back felt like it would afford more control and make the player feel more powerful, and it gave the players more options on how to interact with the enemies. 

https://github.com/IAMColumbia/ApocolypseTrain/assets/76492881/619361cc-37f5-407d-ae2a-5c7ac2928356


I added a spiked barrel(white egg shaped thing) to act as a trap you can push zombies into using the dodge. It is still pretty buggy but I think it has potential. I got inspired by dying light as you can kick zombies into spike traps. 

https://github.com/IAMColumbia/ApocolypseTrain/assets/76492881/d9f13398-9f1b-436e-af81-095bbd5d6c4f

I am still debating wheather to have the knockback direction of the zombie linked to the players dash direction, or the direction vector from the player to the zombies current location. it makes more sense to have the zombie pushed away from the player, but it is a bit harder to control. Either way it needs to be tweaked as the spikes dont feel very useful or responsive.


## Monday November 13th

I got alot of playtesting feedback from some successful chicago indie devs. They gave alot of great ideas on where to take the project. I told them my main goal was encouraging communication between players.

Some key things I think they touched on were

Encourage players to create a plan
*  have traps attatched to the train so players can kite zombies into them and be more strategic about movement around the space
*  have a big enemy that takes more work then just shooting to kill (maybe you can only damage it from the back) so one player needs to distract it and another can go around back and kill it
* place more collectables around the map, maybe survivors to rescue to force players to make decisions about what to do 

More ways to kill zombies
* grenades, swords
* use fuel for other things besides making the train go. Power turrets around the map (maybe there is a turret on the train and you need to choose weather to fuel the train or the turret)

Make other tasks that take time to force players to help eachother. 
* one shoots zombies while the other repairs the train

## Tuesday, November 14

I decided to approach the design problem of "The spiked traps dont feel useful" by making them feel over powered first. 

I realized making the zombies anymore easy to control (Like having them knocked back based on the direction) felt too janky and didnt feel intuitive as thats not how the real world behaves. 

I thought if I cant make the player have more control over the zombies, why not make the target they need to hit bigger. So I decided to go from the spiked barrel idea to a spiked wall, with a much larger surface area and therefor a much larger target to smash zombies into.

![Alt text](<Screenshot 2023-11-14 113116.png>)

https://github.com/IAMColumbia/ApocolypseTrain/assets/76492881/120ccf4a-d8e3-49be-ac0c-02df8c20ae56
