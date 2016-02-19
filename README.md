# Tech_Writing1_MonsterGame
Program Description
=================================================
This is a basic game written in Python where the player fights a monster. The entire game is a written into a file that loops its intructions until the either the monster or the player reach zero or below in point count. 
Both the player and the monster fight for their points and avoid damage until the game ends (or when one of the player's scores drop below zero). 
The game depends on how well the player plays if he plays well he can receive experience points which will help him gain an advantage on the monster by winning either a dagger, shield, or sword. The experience points can be key to winning the game.

Modules 
================================================
The 'os' module was used to save the file we stored the game in. 
The 'random' module was used to randomize the numbers that we use throughout the game. The primary reason for using the random module was to initialize the game scores and to regulate the variable for dropRange which drops objects for the player to gain experience or damage from. The 'random' module was called into the program several times and even called within the main loop to maintain the game.
You can see below how both the 'random' and 'os' module's are initialized and used in the program below.

```
import random
import os 

myNumber = random.randint(1,20)                 #player's status based on random choice between 1 and 20
monsterNumber = 0 
my_health = 100
monster_health = 100
experiencePoints = 0
level = 0
itemDrop = ["dagger", "shield", "sword"]
dropRange = random.randint(1,100)               #how often the items (dagger, shield, and sword) are dropped.
damage = 0
shield = 0
weapon = 0
x = 0
y = 0

if os.path.exists("monsterSavefile.txt"):       #We use os for accessing the file system - os module
    file = open("monsterSavefile.txt", "r")     #Open file to write and save data    
    temp = [line.strip("\n") for line in file]      
    experiencePoints = int(temp[0])
    level = int(temp[1])
    file.close()
else:
    experiencePoints = 0
    level = 0
    itemDrop = ["dagger", "shield", "sword"]

choice = "notq"
```

At the end of the file I made sure to save it in the loop so that ALL the information needed was saved into the file:

```
report = open("monsterSavefile.txt", "w") #write the file inside the loop so it has ALL the information needed
report.write(str(experiencePoints)+ "\n" + str(level) + "\n" + str(itemDrop))
report.close()
```

Game Creation Challenges
------------------------
Challenges included learning basic loops such as dropping objects during the game and getting the file to save all of the game's previous progress. Both took time, but were implemented into the game so that it accomplishes both of these tasks.

Notes
-----
* There were NO FUNCTIONS defined within this game only basic module's and looping structures. 
* All of the loops and if statements in this game are essential to creating fair gameplay. The first set of if-statements control the overall player/monster scores while the second set of statments maintain the itemDrop variable with it's content.
* This is a basic program that runs the game without hands on interaction.


