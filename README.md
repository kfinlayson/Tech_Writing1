# Tech_Writing1_MonsterGame
Description
=================================================
This is a basic game written in Python where the player fights a monster. The entire game is a written into a file that loops it's intructions until the either the monster or the player reach zero or below in point count. 
Both the player and the monster fight for their points and avoid damage until the game ends (when the score for one or the other drops below zero). Depending on how well the player plays he can receive experience points which will help him gain an advantage on the monster by winning either a dagger, shield, or sword. 

Game Creation Challenges included learning basic loops such as dropping objects during the game and getting the file to save all of the game's previous progress.

Module 
================================================
I imported the 'os' module to save the file we stored the game in. 
The random module was used to randomize the numbers that we use throughout the game. The primary reason for using the random module was to initialize the game and to regulate variable for dropRange which is in charge of dropping objects for the player to get damage from. 

```
import random
import os 

myNumber = random.randint(1,20) #set variables and create menu to store the game in
monsterNumber = 0 
my_health = 100
monster_health = 100
experiencePoints = 0
level = 0
itemDrop = ["dagger", "shield", "sword"]
dropRange = random.randint(1,100)
damage = 0
shield = 0
weapon = 0
x = 0
y = 0
```

Notes:
---------
* There were NO FUNCTIONS used in this game only basic module's and looping structures. 
* This is a basic program that runs the game without hands on interaction.


