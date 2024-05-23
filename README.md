# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name: GURU REVANTH KUMARAVEL RADHIKA
## Register Number: 212223230065
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Server Side
```
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```
### Client Side
```

import socket
s=socket.socket()
s.connect(('localhost',90))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## OUTPUT
## Client:
![Screenshot 2024-04-29 141459](https://github.com/23013743/3b_CHAT_USING_TCP_SOCKETS/assets/161271714/1b734ae7-d464-403d-8f52-20c870c40213)

## Server:
![Screenshot 2024-04-29 141506](https://github.com/23013743/3b_CHAT_USING_TCP_SOCKETS/assets/161271714/f2c8dd36-8f4b-4457-80f1-5eff019c2807)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
