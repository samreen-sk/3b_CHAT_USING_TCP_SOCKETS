# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### client:
```
s=socket.socket() 
s.connect(('localhost',8080)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
### server:
```
import socket 
s=socket.socket() 
s.bind(('localhost',8080)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
            ClientMessage=c.recv(1024).decode() 
            print("Client > ",ClientMessage) 
            msg=input("Server > ") 
            c.send(msg.encode())
```
## OUPUT
### client:
![Screenshot 2024-10-18 090055](https://github.com/user-attachments/assets/2d167d18-6775-42f7-bf15-e73c27aeda26)

### server:
![Screenshot 2024-10-18 090114](https://github.com/user-attachments/assets/43a8f7a6-17c8-4cde-a8a5-9c97c5f91613)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
