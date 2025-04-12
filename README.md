# 2a_Stop_and_Wait_Protocol

## NAME: HARISH S

## REG NO: 212224040105
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program

## PROGRAM
## CLIENT 

```
import socket 
s=socket. socket()
s.bind(('localhost', 8000))
s.listen(5)
c,addr=s.accept()
while True:
    i=input("Enter a data: ")
    c.send (i.encode())
    ack=c.recv(1024).decode()
    if ack:
        print(ack) 
            1``
        continue 
    else:
        c.close()
        break
```

## SERVER

```
import socket 
s=socket.socket()
s.connect(('localhost',8000))
while True:
    print(s.recv(1024).decode())
    s.send ("Acknowledgement Recived".encode())
```
## OUTPUT

CLIENT

![client 2a output](https://github.com/user-attachments/assets/a7874b2c-f173-4c69-83a5-3ec6f01fd54a)

SERVER

![server 2a output](https://github.com/user-attachments/assets/6e7f7990-3784-4a6a-993f-2841db43bc29)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
