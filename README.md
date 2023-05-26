### EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

DATE:3-5-2023

### AIM :

To write a python program for creating Chat using TCP Sockets Links.

### ALGORITHM :

1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in server
4. Send and receive the message using the send function in socket.

### PROGRAM :

### CLIENT :
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### SERVER :
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
### OUTPUT :

### CLIENT :

![image](https://github.com/Anandanaruvi/EX-9/assets/120443233/92929ad6-8135-461d-b4d1-6c58f4e014ba)

### SERVER :

![image](https://github.com/Anandanaruvi/EX-9/assets/120443233/c61118e8-737f-4f51-b2a7-008cffb94a03)

### RESULT :

Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
