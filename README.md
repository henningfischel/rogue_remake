# rogue_remake

  Rogue is a 1980 game for unix systems that spawned an entire genre. Traditional rouge-likes are defined by random generation, permanent death, a high level of difficulty, and grid/turn -based exploration and combat. Dungeons and Dragons inspired many early fantasy computer games in the late 70s and 80s. Many titles such as Adventure (1980) had players adventuring through a dungeon in search of a magical object. The Dungeon (1976) was an early example of a grid and turn based dungeon crawler. Beneath Apple Manor (1978) did random dungeon generation before Rouge in 1980. Rouge’s main innovation was the use of ascii characters as graphics which allowed more display room and faster processing then graphical tiles. Rouge’s popularity can also be attributed to originally released in version 4.2 of the Berkley Software Distribution and being open source for all to modify.
 
 ![alt text](https://github.com/StumpyTheLemming/rogue_remake/blob/main/4.PNG)

  I attempted to make a basic copy of Rogue but due to time constraints was only able to make a simpler reproduction. My version has similar aesthetics to later versions of the original. It procedurally generates floors of rooms connected by hallways. It has monsters to fight with turn-based combat.
 
![alt text](https://github.com/StumpyTheLemming/rogue_remake/blob/main/myrogue.PNG)
 
  There are many things that I had to leave out of my version. It is missing: varieties of monsters, items and an inventory, scaling difficulty, player statistics, fog of war, and a win state. Besides that there are several major ways the parts of Rouge the I did implement differ from the original. The screen size of TIC-80 is much smaller than that of most unix machines in 1980 so there is a smaller space to explore in each floor. 
  
  ![alt text](https://github.com/StumpyTheLemming/rogue_remake/blob/main/myrogueboxes.PNG)
  
  My dungeon generation is also different. I could not find the algorithm that Michael Toy and Glenn Wichman used in the original so I used Binary Space Partitioning (http://www.roguebasin.com/index.php?title=Basic_BSP_Dungeon_generation). This method uses binary trees to randomly split the space in half repeatedly to draw rooms and then connects them by drawing a path between the center of the spaces defined by sister nodes. This method ensures that all the rooms are connected but produces a very different result than is seen in the original rogue. 
  
The game can be played at https://stumpythelemming.github.io/rogue_remake/
Use the vi keys to move:


y k u

h _ l

b j n

and . to move down when on the stairs
