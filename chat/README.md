Hi, this is the readme file of the chatbot project i have done:
this chatbot is designed to let you chat by going to the chatrooms, and this is how it works:
  
  
  ***How this project works:
1. Login: user enters the site, writes their name and then has two options:
    Create a room: a new room is created, and system will specifically give a random 4-number code to that room.
    Entering the created room: by entering the room's code, you can join to the chatroom.

2. Connection:
    Just as you enter the chatroom, the client(javascript browser) starts a websocket permanent connection with the server(python).

3. Exchanging messages:
    Every written message by the users are sent to the server, and the server sends the message to everyone  who is present in that room.

4. Exit:
   By closing the room page or the user leaving the chatroom, system will reduce that user's presence and notifies everyone about it.

*** Special Features:
    Real-time comuunication: doesn't need to refresh everytime, or continouos HTTP requests(with the help of Websocket technology)

    Multi-room support: users of different rooms cannot see other rooms' messages. Rooms are completely separated fro each other.

    Unique code geneation: By using a special mechanism, it is guaranteed that no two chatrooms will have the same 4-number code.

    In-memory history: As long as the server in on, chat history of the chatroom is visible even to the user who joined the chatroom after those messages were sent.

    Active members tracker: server knows the number of members in the chatroom.

    Auto cleanup and garbage: if the last member of chatroo leaves, system will automatically wipe out that room and all it's messages so that the resources of RAM won't be wasted.

    Status Notifications: Automatically notifies when a user enters or leaves ta chatroon.

***Technical Details:
   1. Data store: This program does not use databases such as MySQL or MongoDB, but it uses the dictonary date structure in python.it helps the program to have an incredible speed due to the direct access to RAM.But there are disadvantages, as an example, by restarting the server, all the rooms and messages will be deleted.

   2. Session management: For remembering user's name and the code they have entered, flask.session has been used. This is why the server knows who the user is and to which rom they are going when they are guided to /room route.

   3. Socket.io Events:There are some events that are managed in the program:
   connection event, disconnection event, and messaging event.

   4. FrontEnd:By the usage of Socket.io library, the connection establishes. and with help of 'createMessage'function, with change in DOM, it automatically creates new tags and adds them to the end of messages list.


This was the summary of my project, and I hope it was useful.
my university code:404497007
