# Tag
An online multiplayer game of tag.

Tag (first named "netGame") originally was a practice range for network programming as I began to develop more network-based software.
However, it has changed into something much more than that!

Tag now has server and client programs, which do the following:

Server:

  - Must be ran in the command line. A pretty GUI may come in the future, but for now that focus has been put
  on the client.
  
  - The limit of players on the server is only limited by the hardware. In the code, the number of sockets can be changed before starting the server,
  and this can set the amount of people that can join.
  
  - A socket-recycling algorithm that helps to clear out the closed sockets and make room for the new ones coming in (only occurs when there is one or less
  people connected to the server, so that this process does not cause network latency)
  
  - You are able to put in 5 commands (so far): 
  
        1: shutdown the server
        2: list all current sockets and their IP addresses
        3: close a specific socket
        4: choose a player at random to make the tagger and start the game
        5: show the command list again
  
  
Client:

  - Initially you are prompted to input the IP of the server you wish to connect to, which you may type in and press ENTER to initiate a connection. If you simply wish to play
  the game without anyone else, you can leave the line blank, press ENTER and explore on your own!

  - Run around as sheep \ people \ objects with WASD
  
  - Meet up with friends in a very wide coordinate space, which is speckled with NPCs all generated randomly but synchronously on all clients, so you all see the same things
  
  - Change your outfit with the left and right arrow keys
  
  - Use each outfit's emotes by pressing 1 or 2 (more to come hopefully)
  
  - Press SHIFT to end your connection to the server and properly exit the application
  
  - The tagger is twice as fast as the other people, and the runners have abilites with a cooldown timer above them, so gameplay is more dynamic. 
  
  - The abilities are as follows:
  
        1: extra speed
        2: invisiblity
        3: tiny-ness
        4: teleport to a random NPC on the map




We now have version numbers! Here are the notes on what has happened for each version put out:

NOTE: The version numbers for the server and client programs don't need to be the exact same. Only the first number for each version number has to be the same
for proper combatibility, for example a server with version number 1.0 can be used with clients that have a version number of 1.2, 1.0, or 1.5, but not 2.3.

1.0:

- First full version of Tag, complete with three map variants and a group of characters to choose from
- Score system, if you are the tagger when the round ends, you lose a point. Each player starts with 3
- Key to press to show more information, such as rules, abilities, controls
- Much more refined server program that allows for better intake of other clients's data (helped immensely with latency)
- Abilities only reset their amounts per round, instead of (accidentally) resetting whenever you became the tagger during any given game
- A secret...

1.2:

- Fixed the game timer so that when it gets to single digits it doesn't display it weirdly (Props to TheLegitDrummer for pointing it out)
- Added 4 player skins and changed a few skins as well
- Added a game over message for when the player runs out of lives. Also, the box that displays your score now says "Lives: #" rather than "Score: #"
- Fixed a communication problem with the socket on the client's side
- Players that are invisible can no longer be tagged (Should've had this happen in the first place, makes much more sense)
- Added a kick-up animation to the running of the player's character, as if they're running so fast that they're kicking up something
- Made it so that once you disconnect from the server, all other players that were visible disappear (Again, this should've been a feature already, sorry!)
