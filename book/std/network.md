# 网络

## urllib

## socket

- PyMOTW-3 https://pymotw.com/3/socket/tcp.html

**Echo Server**

```python
import sys
import socket

sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

server_addr = ('localhost', 6666)
print('starting up on %s port %s' % server_addr)
sock.bind(server_addr)

sock.listen(1)

try:
    while True:
        print('waiting for a connection')
        conn, client_addr = sock.accept()

        try:
            print('connection from', client_addr)
            while True:
                data = conn.recv(16)
                print('received "%s"' % data)
                if data:
                    print('sending data back to the client')
                    conn.sendall(data)
                else:
                    print('no more data from', client_addr)
                    break
        finally:
            conn.close()
except KeyboardInterrupt:
    sys.exit()
```

**Echo Client**

```python
import sys
import socket

sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
server_addr = ('localhost', 6666)
print('connecting to %s port %s' % server_addr)
sock.connect(server_addr)

try:
    msg = 'This is the message. It will be repeated.'
    print('sendding "%s"' % msg)
    sock.sendall(msg.encode())

    amount_received = 0
    amount_expected = len(msg)

    while amount_received < amount_expected:
        data = sock.recv(16)
        amount_received += len(data)
        print('received "%s"' % data)
finally:
    print('closing socket')
    sock.close()
```

## http

```python
import http.client

conn = http.client.HTTPSConnection("codingcat.top")
conn.request("GET", "/")

resp = conn.getresponse()
print(resp.status, resp.reason)
data = resp.read()
print(data)
```

## asyncio
