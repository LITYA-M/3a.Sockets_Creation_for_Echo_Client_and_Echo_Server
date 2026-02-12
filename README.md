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
server
```
import socket
s=socket.socket()
s.bind(('localhost',8001))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
client
```
import socket
s=socket.socket()
s.connect(('localhost',8001))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
    
## OUPUT

server

<img width="751" height="61" alt="image" src="https://github.com/user-attachments/assets/8399edf5-0a2b-4f1c-8929-9ae76907624c" />

client

<img width="705" height="255" alt="Screenshot 2026-02-12 112025" src="https://github.com/user-attachments/assets/bc664cec-dbd5-4464-a026-351239de7787" />


## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
