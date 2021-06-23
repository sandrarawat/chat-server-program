# chat-server-program


************Design Document************

	Description
		This Server/Chat program contains two Classes; ChatClient and ChatServer.
		ChatServer waits for socket connections on the hardcoded Port 20000.
		When ChatClient is run, a new socket(client) is created, which is assigned a username as set by the user. 
		Multi-Threads are used to allow multiple Socket connections. 
		All messages are broadcast to all users. 
		ChatClient uses JScrollframe, therefore an appropriate IDE is required to run the programme.
		Each users JScrollPane (chatPanel) contains a TextArea and two buttons; Send (to send message) and Exit (exit program)
		A vector is used to store clients (users) by adding them to the vector upon each new socket created by ChatClient. When each client exits they are removed from the vector.
		If client is unable to reach server , an error message is displayed on the console, which originates from the try catch statement (ChatClient:91 run constructor)
		
	Instructions: *package name is ie.gmit.dip
		1.Run ChatServer in order to connect to the hardcoded port 20000, and listen for socket connections.
		2.Run ChatClient, where port 20000 is hardcoded.
		3.Type Username when prompted in order to start a new socket
		4.Run ChatClient additional times in order to create additional sockets for new users.
		5.Type message, press Send or press enter to broadcast message to all users
		6.Type \q or press Exit to exit chat (user is removed from the vector, message will be broadcast to all users to display user has disconnected, and a broadcast message to show remaining users.)	
			
		   
	References:
		https://stackoverflow.com/questions/16336123/display-online-users-from-server-to-all-connected-clients
		https://www.geeksforgeeks.org/multi-threaded-chat-application-set-1/
		https://www.geeksforgeeks.org/multi-threaded-chat-application-set-2/
		https://stackoverflow.com/questions/6257316/illegal-escape-character	   
		https://www.codejava.net/java-se/networking/how-to-create-a-chat-console-application-in-java-using-socket
		   
