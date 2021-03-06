# Chat-Room-and-File-Transfer Messenger
Distributed Systems Assignment 1

Submitted By:
		Pratik Mandlecha
		20161172

<b> Running Server </b>

goto directory from the root folder
compile Server java file :
```javac TheMajesticServer.java``` <br>
start Server :
```java TheMajesticServer <max number of users>```

OR Bash Script:

```./server <max number of users>```

Error Handling: Displays error when maximum users are not provided. 

<b> Running Client </b>

goto directory from the root folder
compile Client java file:
```javac People.java``` <br>
start Client :
```java People <username>```

OR Bash Script:

```./client <username>```

Error Handling: Displays error when username is not provided. 

Whenever a user is logged in, server shows: ```User <username> is logged in```

<b> Chatroom </b>

Input: ```create chatroom <chatroom_name>```
Output: Chatroom <chatroom_name> created
	You are in chatroom <chatroom_name>

(Creating a chat room automatically joins the client to that chat room.)

Input: ```list users``` <br>
Output: <users_of_the_chatgroup_you_are_currently_in>
Error Handling: You are not part of any chatroom (If the user is not present in any chatgroup right now)

Input: ```list chatrooms``` <br>
Output: command to list all chat rooms
Error Handling: No chatrooms are available (If there are no chatrooms present)

Input: ```join chatRoom1``` <br>
Error Handling: chatroom doesn't exist (If the specified chatroom doesnt exist)

Input: ```add <username>``` <br>
Output: Adds the user to the current chatroom

Input: ```leave``` <br>
Output: <username> left the chatroom
(The chatroom gets deleted when all users leave it)

Input: ```LOGOUT``` <br>
Output: Deletes the socket for that user

Input: ```reply “message”``` <br>
Output: Send a message in the chatroom as Username: <message>

Input: ```reply <username>/<filename> <tcp/udp>``` <br>
Output: Send file to all the users in the current chatroom
Example: ```reply me/f2.png tcp```

Error Handling:
• Maximum number of users on Server reached. <br>
• Maximum number of users allowed for the server not given at the time of exection. <br>
• User tried to connect to create/join a chatroom when part of another chatroom. <br>
• User not in any chatroom but tries to print Members of the chatroom/leave. <br>
chatroom/add another user/reply. <br>
• Unrecognised command – When the command is not among the above defined commands. <br>
• User tried to join a chatroom that doesn’t exist. <br>
• User tried to add another user to a chatroom when the other user is already a part of another chatroom/doesn’t exist/part of same chatroom. <br>
• User tries to send a file that doesn’t exist. <br>
