# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUTPUT:
### Client:
![image](https://github.com/Monishofficial/3b_CHAT_USING_TCP_SOCKETS/assets/149455421/d0beafe6-c584-452b-b8d3-5c20b0e28e74)


### Server:
![image](https://github.com/Monishofficial/3b_CHAT_USING_TCP_SOCKETS/assets/149455421/957ac40a-e4e1-454e-b42f-fd18357540f1)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
