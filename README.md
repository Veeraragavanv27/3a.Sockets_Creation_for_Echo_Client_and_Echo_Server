# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## NAME : VEERARAGAVAN V
## REGISTER NUMBER : 212223230237
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
### CLIENT 
```py
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    clientmessage=c.recv(1024).decode()
    c.send(clientmessage.encode())

```
### SERVER 
```py
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client>")
    s.send(msg.encode())
    print("server>",s.recv(1024).decode())
```
## OUTPUT
### CLIENT OUTPUT
![CLIENT (2)](https://github.com/user-attachments/assets/7af1167a-af76-4790-93cc-66bb36eb8626)

### SERVER OUTPUT
![SERVER](https://github.com/user-attachments/assets/9fc46168-1b67-4424-8236-fa58fb6d0a54)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
