# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME : NITHIYANERANJAN S
## REGISTER NUMBER : 212223040136
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT
```py
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### SERVER 
```py
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())

```
## OUTPUT
### CLIENT OUTPUT
![Screenshot 2024-05-05 224151](https://github.com/NITHIYANERANJAN/3b_CHAT_USING_TCP_SOCKETS/assets/144979351/479c7709-37f0-490d-9c85-cd9c37796ed5)


### SERVER OUTPUT
![Screenshot 2024-05-05 224110](https://github.com/NITHIYANERANJAN/3b_CHAT_USING_TCP_SOCKETS/assets/144979351/20dbfadc-d1a7-4a23-8e9c-f8362e23a216)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
