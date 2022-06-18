# Tag


An online multiplayer game of tag!


## Installation

WINDOWS x64 INSTALLER LINK FOR CLIENT VERSION 5.0:
https://drive.google.com/file/d/1KTs0Dm4LO-fyqe71uFrMmOianntrJzdg/view?usp=sharing

If you choose to run the .jar files directly, you will need the consumer version of Java installed along with Oracle's JDK (Java Development Kit) version 18

Here are the links to the downloads (as of 6/11/2022):

https://www.java.com/en/download/

https://www.oracle.com/java/technologies/downloads/

In order for these downloads to be effective, be sure to run them once they've been downloaded.


## Gameplay

Tag (first named "netGame") originally was a practice range for network programming as I began to develop more network-based software.
However, it has changed into something much more than that!

Tag now has server and client programs, which do the following:

Server:

  - Must be ran from the command line. A pretty GUI may come in the future, but for now that focus has been put
  on the client. Port-fowarding on port 44440 may be necessary depending on your network (Usually is necessary).
  
  - A socket-recycling algorithm that helps to clear out the closed sockets and make room for the new ones coming in
  
  - You are able to put in 5 commands (so far): 
  
        1: shutdown the server
        2: list all current sockets and their IP addresses
        3: close a specific socket
        4: choose a player at random to make the tagger and start the game
        5: show the command list again
  
  
Client:

  - If you press SHIFT you will be prompted to input the IP of the server you wish to connect to, which you may type in and press ENTER to initiate a connection

  - Run around as sheep \ people \ objects with WASD
  
  - Meet up with friends in a wide coordinate space, which is speckled with objects with which you can hide behind / below
  
  - Change your outfit with the left and right arrow keys
  
  - Use each outfit's emotes by pressing 1 or 2
  
  - Press 'O' to end your connection to the server
  
  - The tagger is twice as fast as the other people, and the runners have abilites with a cooldown timer above them, so gameplay is more dynamic. 
  
  - The abilities are as follows:
  
        1: extra speed
        2: invisiblity
        3: mist effect (affects tagger only)
        4: teleport to a random location


## Version Notes

NOTE: The version numbers for the server and client programs don't need to be the exact same. Only the first number for each version number has to be the same
for proper combatibility, for example a server with version number 1.0 can be used with clients that have a version number of 1.2, 1.0, or 1.5, but not 2.3. However,
it is strongly advised to always use the latest updated versions of both programs for maximum compatibility.

1.0:

- First full version of Tag, complete with three map variants and a group of characters to choose from
- Score system, if you are the tagger when the round ends, you lose a point. Each player starts with 3
- Key to press to show more information, such as rules, abilities, controls
- Much more refined server program that allows for better intake of other clients's data (helped immensely with latency)
- Abilities only reset their amounts per round, instead of (accidentally) resetting whenever you became the tagger during any given game
- A secret...

1.2:

- Fixed the game timer so that when it gets to single digits it doesn't display it weirdly (Props to TheLegitDrummer for pointing it out). Also made
the game timer 4 minutes long instead of 5, games felt a bit too long
- Added 4 player skins and changed a few skins as well
- Added a game over message for when the player runs out of lives. Also, the box that displays your score now says "Lives: #" rather than "Score: #"
- Fixed a communication problem with the socket on the client's side
- Players that are invisible can no longer be tagged (Should've had this happen in the first place, makes much more sense)
- Added a kick-up animation to the running of the player's character, as if they're running so fast that they're kicking up something
- Made it so that once you disconnect from the server, all other players that were visible disappear (Again, this should've been a feature already, sorry!)

2.0:

- Added knights and dragons as outfits
- Added a loading screen at the beginning after pressing ENTER
- Created a host system between the clients and the server, so that the first person in the match is the host. The host will have the ability to start the match
once there are enough players to play. This was a good step because before you could only start the match by doing so from the command line through the server
- Added a stunned effect once someone has become the tagger, so that the other players have a moment to get away
- Fixed some buggy movement glitches, where if you were double speed or the tagger you could break the barrier formed around the map occasionally, thus messing
up the data being sent to the server for your client
- Updated the coordinate system to be more intuitive, and players are started at the center of the map now instead of the bottom right corner
- Began negating the kick-up animation for characters that fly or levitate (right now only dragons and spacemen)
- Changed the server messages to be a little prettier when printed in the command line
- Found and fixed two small things that help tremendously with runtime speed

3.0:

- Added elves and Santa as outfits
- Added player numbers, but they are only visible if the other player is not invisible or tiny (having the number above their head when they're invisible
or tiny would give them away!)
- Fixed movement at the boundary of the map, sometimes the player would go too far if they were double speed or the tagger. The main problem of this was
fixed in version 2.0, but I have made some tweaks here to make sure it is smooth and what it should be
- Fixed the stun-tag trading problem, where the person who was just tagged is stunned, but still able to transfer the tagging ability. Caused lots of
double tagging to happen, props to XKainerX, Sentience, and Its_Jamt for helping with this and being good test rats! (just kidding, their test mice,
much more sophisticated)

3.1:

- Added a halloween killer outfit! Also very slightly changed the Santa outfit
- Added arrows that are togglable to show other runners's locations. It will only display for other runners, otherwise the tagger would have a huge leg up!
this just allows people to be able to group up more or avoid other players to avoid attention
- Added another box that shows up for the controls, showing the controls for toggling the arrow locators and for starting a game as the host

3.5:

- Added police officers as outfits. Chase down the killer! Thanks to (Lenny_Face) for the suggestion of the skin and emote #1
- Added coins and the shop! Skins are no longer all free, you have to earn coins to purchase them. The player gets coins by tagging others and
using their abilities while in-game
- With the addition of coins, a coin box was added to the top right of the screen to show you how many coins you have
- With the addition of the shop, the save feature has been added! Press V to save your information, such as your coins and the skins you have unlocked
- Added new text to the Show More menu outlining the new things the player can do, and rearranged some of the pop-ups to look smoother with the layout

3.6:

- Added 10 new outfits: trolls, chefs, and mad scientists
- Added an animation for the drop-down alert along with reshaping that alert to look more like other screen boxes
- Added an animation for when the player gets coins
- Adjusted the randomization of the map selection from the seed given by the server so that other maps can be selected more often (before it was usually 
if not always the first map)
- Another secret...

3.7:

- ATTENTION - The save file was changed in this update from "player.txt" to "tagData.txt". Please rename your file if necessary, and keep the file in the
same directory as the .jar file of Tag

- Added gnome skins
- All skins now have names in the shop, slightly changed the layout of the shop panels when characters are purchased
- The window is now resizable, shoutout to Sentience for testing

4.0:

- Now a 12-player game!
- Fixed a painting to window process that helped processing time
- Made it so that scrolling through the shop is faster, props to robotbroadcast for the tip!

5.0:

- ATTENTION - The save file was changed from "tagData.txt" to "save.tag". Please rename your save file if necessary
- General optimization of networking processes
- Changed a few skins
- Map and map objects reworked! Only one map now, however this can change... (see final bullet point)
- Collision process has been moved to the server
- Changed the GUI and key bindings
- Number boxes on players removed
- The teleportation ability is no longer based on map objects / NPCs. You will be teleported to a random location on the map rather than a random object
- The tiny ability has been changed to the mist effect! The mist effect puts a thick mist around the tagger, lowering their chances of seeing a runner
- More points are given for using abilities and for tagging. We have to buy those skins somehow!
- CUSTOM IMPORTING! I am very excited to say that there is now a custom importing process for Tag. This allows you to import custom map objects, custom skins, and a custom map if you wish. See the custom importing PDF file for more information.
