# Tag
An online multiplayer game of tag.

Tag (first named "netGame") originally was a practice range for network programming as I began to develop more network-based software.
However, it has changed into something much more than that!

Tag now has server and client programs, which do the following:

Server:

  Must be ran in the command line. A pretty GUI may come in the future, but for now that focus has been put
  on the client version.
  
  The limit of players on the server is only limited by the hardware. In the code, the number of sockets can be changed before starting the server,
  and this can set the amount of people that can join.
  
  A socket-recycling algorithm that helps to clear out the closed sockets and make room for the new ones coming in (only occurs when there is one or less
  people connected to the server, so that this process does not cause network latency)
  
  You are able to put in 5 commands (so far): 1 - shutdown the server \ 2 - list all current sockets and their IP addresses \ 3 - close a specific socket \ 4 - choose a
  player at random to make the tagger and start the game \ 5 - show the command list again
  
  
Client:

  Initially you are prompted to input the IP of the server you wish to connect to, which you may type in and press ENTER to initiate a connection. If you simply wish to play
  the game without anyone else, you can leave the line blank, press ENTER and explore on your own!

  Run around as sheep \ people \ objects with WASD
  
  Meet up with friends in a very wide coordinate space, which is speckled with NPCs all generated randomly but synchronously on all clients, so you all see the same things
  
  Change your outfit with the left and right arrow keys
  
  Use each outfit's emotes by pressing 1 or 2 (more to come hopefully)
  
  Press SHIFT to end your connection to the server and properly exit the application
  
  The tagger is twice as fast as the other people, and the runners have abilites with a cooldown timer above them, so gameplay is more dynamic
