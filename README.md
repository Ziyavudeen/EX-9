# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

### DATE : 02-05-2023

# AIM :
To write a python program for creating Chat using TCP Sockets Links.

# ALGORITHM :
1. Start the program.
2. Get the frame size from the user.
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server, it will send ACK signal to client otherwise it
will sendNACK signal to client.
6. Stop the program

# PROGRAM :
## CLIENT
~~~
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
~~~
## SERVER
~~~
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while Tru![client_9](https://github.com/Javith-farkhan/EX-9/assets/94296805/5a72931b-5781-458c-9d01-7a7d133e685b)e:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
~~~

# OUTPUT :
## CLIENT
![client_9](https://github.com/Javith-farkhan/EX-9/assets/94296805/814b2b72-0484-4c45-9927-8d68f0d276e5)

## SERVER
![server_9](https://github.com/Javith-farkhan/EX-9/assets/94296805/8250b010-cbe9-4165-a941-89c5222692cf)



# RESULT :
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
