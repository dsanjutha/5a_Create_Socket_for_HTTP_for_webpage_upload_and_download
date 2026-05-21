# 5a_Create_Socket_for_HTTP_for_webpage_upload_and_download
## AIM :
To write a PYTHON program for socket for HTTP for web page upload and download
## Algorithm

1.Start the program.
<BR>
2.Get the frame size from the user
<BR>
3.To create the frame based on the user request.
<BR>
4.To send frames to server from the client side.
<BR>
5.If your frames reach the server it will send ACK signal to client otherwise it will send NACK signal to client.
<BR>
6.Stop the program
<BR>
## Program 
```
import socket

def send_request(host, port, request):
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    s.connect((host, port))

    s.sendall(request.encode())

    response = s.recv(4096).decode()
    s.close()

    return response

host = "example.com"
port = 80

request = "GET / HTTP/1.1\r\nHost: example.com\r\n\r\n"

response = send_request(host, port, request)

print(response)
```

## OUTPUT
<img width="358" height="814" alt="Screenshot 2026-05-21 185701" src="https://github.com/user-attachments/assets/512e70dc-401f-4fbe-b754-057080ddbac4" />

## Result
Thus the socket for HTTP for web page upload and download created and Executed
