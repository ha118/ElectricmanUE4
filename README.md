# Electricman UE4
 A game similar to bomberman made using unreal engine 4 with blueprints visual scripting and starter content.
 
 The objective of the game is to make your way to the end of the level while destroying blocks blocking your way and avoiding enemies.
 
 The blocks's collision for the visibility channel was set to block. For the enemies and the player, this was set to overlap. 
 
To implement the bomb, MultiSphereTraceByChannel is used. Through this a blocking hit is detected and everything between the blocking hit and the start of the trace is destroyed. This also allows beam target location of the particle effect of the spark to be set to the blocking hit location.

The enemies start by moving to a new random location in navigable area. They either succeed or fail. In both the cases, they wait for 2 seconds and move to a new loaction. Touching the enemies leads to failure. 
