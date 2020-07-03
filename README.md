# netGame
A new online game!

NetGame originally was the expansion of my knowledge on networking as I began to develop more network-based software.
However, it has changed into something much more than that now!

NetGame now has server and client programs, which do the following:

Server:

  Must be ran in the command line. A pretty GUI may come in the future, but for now that focus has been put
  on the client version.
  
  The limit of players on the server is only limited by the hardware. In the code, the number of sockets can be changed before starting the server,
  and this can set the amount of people that can join.
  
  A socket-recycling algorithm that helps to clear out the closed sockets and make room for the new ones coming in (only occurs when there is one or less
  people connected to the server, so that this process does not cause network latency)
  
  You are able to put in 3 commands (so far): 0 - accept a new connection \ 1 - shutdown the server \ 2 - list current socket information
  
  
Client:

  Initially you are prompted to input the IP of the server you wish to connect to, which you may type in and press ENTER to initiate a connection

  Run around as sheep!
  
  meet up with friends in a very wide (65536x65536, may be expanded later) coordinate space, which is (soon to be) filled with like objects all generated randomly
  
  change your skin (right now just the color of your wool) with the left and right arrow keys
  
  press SHIFT to end your connection to the server and properly exit the application
