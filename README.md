## Steps to make it work:

### mumble-server
We are using this image: https://github.com/sudoforge/docker-images/tree/master/mumble-server


### mumble-web
`openssl req -new -x509 -days 365 -nodes -out self.pem -keyout self.pem` see: https://github.com/novnc/websockify#encrypted-websocket-connections-wss
permissions for self.pem 1001:1001

Alternatively start a container, install Let's encrypt certbot and move `fullchain.pem` and `privkey.pem` to the `pem` folder/volume.

### Connection
Open the mumble-web in your browser: via https://localhost:8080/
if it warns you about an insecure certificate accept it, if it is the one you have created in the previous step
in the connection window set:
- adress: localhost
- port: 8080
- user: as you like

connect
