# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

## DATE : 03-05-2023

## AIM :
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM :
```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the Socket module in server
4.Send and receive the message using the send function in socket.
```

## PROGRAM :
DEVELOPED BY : SAKTHI PRIYA D
REG NO:212222040139
## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## SERVER:
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

## OUTPUT :
## CLIENT:
![image](https://github.com/sakthipriyadhanusu/EX-9/assets/119393194/f4a2f275-41f3-450b-981b-4a39164fe4b7)
 
## SERVER:
![image](https://github.com/sakthipriyadhanusu/EX-9/assets/119393194/d9d0b822-ceb1-49ff-85df-e5d7866a6a27)

## RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
