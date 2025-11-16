# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### Server
```
import socket
s = socket.socket()
s.bind(('localhost',8001))
s.listen(5)
c,addr = s.accept()
while True:
    ClientMessage = c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
### Client :
```
import socket
s = socket.socket()
s.connect(('localhost',8001))
while True:
    msg=input("client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUPUT :

<img width="517" height="93" alt="image" src="https://github.com/user-attachments/assets/50755ef7-a679-4701-9c84-b0ddd8f53f1e" />

<img width="517" height="93" alt="image" src="https://github.com/user-attachments/assets/6c768314-6a15-404b-952f-1648de9d747b" />



## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
