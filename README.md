## Steps to make it work:

### mumble-server
permissions for ./data/mumble-server 108:111
start the mumble-server twice, in the first run it just creates the mumble-server.ini in the second run it will start the server


### mumble-web
`openssl req -new -x509 -days 365 -nodes -out self.pem -keyout self.pem` see: https://github.com/novnc/websockify#encrypted-websocket-connections-wss
permissions for self.pem 1001:1001
connect via https://localhost:8080/
