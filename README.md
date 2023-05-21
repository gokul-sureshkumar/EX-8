# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

DATE :

AIM :
```
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.
```

ALGORITHM :
```
1.Get the frame size from the user
2.To create the frame based on the user request.
3.To send frames to server from the client side.
4.If your frames reach the server, it will send ACK signal to client otherwise it will send NACKsignal to client.
5.Stop the program.
```

PROGRAM :
## Client Program:
``` python 
## Developed By : Kavinraja D
## Reg no : 212222240047
import socket

s = socket.socket()
s.connect(('localhost', 8000))

while True:
    msg = input("Client > ")
    s.send(msg.encode())
    print("Server > ", s.recv(1024).decode())
```
## Server Program:
``` python
import socket

s = socket.socket()
s.bind(('localhost', 8000))
s.listen(5)
c, addr = s.accept()

while True:
    ClientMessage = c.recv(1024).decode()
    c.send(ClientMessage.encode())
```

OUTPUT :
## Server Output:
![image](https://github.com/gokul-sureshkumar/EX-8/assets/121148715/1a84f0dd-2ad2-401a-8c46-7b5f4f9814a0)
## Client Output:
![image](https://github.com/gokul-sureshkumar/EX-8/assets/121148715/087e9da9-ef87-4d10-8faa-982ead8cf9a0)



RESULT :
```
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
```
