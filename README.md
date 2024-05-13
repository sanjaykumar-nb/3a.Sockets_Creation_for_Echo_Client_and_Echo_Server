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
## client
```
import socket
s=socket.socket()
s.connect(('localhost',8080))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## server
```
import socket
s=socket.socket()
s.bind(('localhost',8080))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUPUT
## client
![Screenshot 2024-04-29 141309](https://github.com/sanjaykumar-nb/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/154039979/ce46024e-8206-4088-9242-6a9d8df413ae)
## server
![Screenshot 2024-04-29 141309](https://github.com/sanjaykumar-nb/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/154039979/be04111a-fe3c-4f92-94de-788d6aedba7e)

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
