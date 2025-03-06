## Name   : SANJAY M
## Reg No : 212223230187

# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:

```python
Client.py
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'Name :SANJAY M - Reg No:212223230187-Date: 06/03/2025')
    print(f'Received: {s.recv(1024)!r}')
```

```python
Server.py
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```

## OUTPUT:
### Client.py:
![image](https://github.com/user-attachments/assets/43558a9b-c230-4952-831e-ed2a13618117)

### Server.py:
![image](https://github.com/user-attachments/assets/d6ac9149-f1ea-4806-8ac4-c1ad7fe471b5)



## RESULT:
The program is executed successfully
