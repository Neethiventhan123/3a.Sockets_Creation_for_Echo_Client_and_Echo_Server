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
## PROGRAM:
### CLIENT: 
``` 
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())  
``` 
### SERVER: 
``` 
import socket 
s=socket.socket() 
s.bind(('localhost',8000)) 
s.listen(5) 
c,addr=s.accept() 
while True: 
    ClientMessage=c.recv(1024).decode() 
    c.send(ClientMessage.encode())
```
## OUTPUT
### client:
![3 a cl cn](https://github.com/Neethiventhan123/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148514848/a6352359-0e58-4399-aa23-9693d7c94cf1)
### server:
![3b s](https://github.com/Neethiventhan123/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/148514848/feb4fd95-14b8-4258-b47d-4af5bb4bb277)






## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
