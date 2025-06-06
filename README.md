# PeerToPeerArchitecture
This project is a simple peer-to-peer (P2P) chat application developed in Java using socket programming. It fulfills all the requirements provided in the lab instructions.

#Lab Tasks Covered
The project runs a basic P2P communication model using socket programming.

The code is modified to allow a client to send as many messages as they want until the word "exit" is entered.

The code is split into two separate classes, one acting as a peer (sender) and the other as a receiver (listener), which enables testing on the same machine.

The application allows communication between two machines using IP address and port number, enabling chatting with classmates.

#Project Files
Peer.java: This class is responsible for sending messages to another peer. It acts as the client.

Receiver.java: This class listens for incoming messages and prints them on the console. It acts as the server.

⚙️ How to Run
First, compile both Java files using the following commands:

nginx
Copy
Edit
javac Peer.java
javac Receiver.java
In the first terminal, run the receiver by executing:

nginx
Copy
Edit
java Receiver
In a second terminal (or on a different machine), run the peer by executing:

nginx
Copy
Edit
java Peer
The Peer program will ask for:

The IP address of the receiver (e.g., localhost or your classmate’s IP)

The port number (e.g., 5000)

You can then start chatting by typing messages. Typing "exit" will stop the chat session and close the connection.
#Example Run
On Receiver terminal:

vbnet
Copy
Edit
Receiver is listening on port 5000
Received: Hello
Received: exit
On Peer terminal:

pgsql
Copy
Edit
Enter receiver IP: localhost
Enter receiver port: 5000
Enter message (type 'exit' to quit): Hello
Enter message (type 'exit' to quit): exit
#Chatting Across Machines
To use this application for chatting with your classmates over a network:

Enter the correct IP address of the other machine instead of localhost.

Make sure both sender and receiver use the same port number.

Add inbound and outbound firewall rules for the port being used (e.g., 5000) to allow network communication.

Both machines must be on the same local network, or port forwarding should be configured if on separate networks.

#Exit Condition
Typing "exit" in the Peer program will:

Send an "exit" message to the Receiver

Terminate the Peer program gracefully
