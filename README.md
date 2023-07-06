# DungeonOfDoom

My implementation of Dungeon of Doom uses 6 classes. Main class creates an instance of GameLogic that runs the game. The GameLogic class contains the map and players needed to play. It also lets players execute commands since it is the central class that has access to both the map and the players with their properties. 
I then created an abstract class Player from which HumanPlayer and BotPlayer are extended. I made it abstract instead of using inheritance because I would never create an instance of Player. Player class holds information common to both the human and the bot such as coordinates, the gold required, and a method to make a move.
HumanPlayer has methods that allow humans to input their map choice and the command they wish to execute.
BotPlayer holds methods that allow the bot to make decisions on which commands to execute to chase a player or loot the gold.
Both HumanPlayer and BotPlayer return commands to GameLogic since this is where commands are executed which keeps a nice level of encapsulation.
The final class is Map. It holds the map grid, its name, and the amount of gold needed to win. Its function load map from files generates a 5x5 map. The main map the game is being played on is accessed through GameLogic, however, BotPlayer also creates a 5x5 map in its own class.
