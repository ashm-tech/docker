To run proxy server, install docker, add IPs that will be allowed to use proxy to file "allowed_clients.txt" (each IP on new line) and run command:

sudo docker run -d --restart=always --name squid -p 3128:3128 -v ./squid.conf:/etc/squid/squid.conf -v ./allowed_clients.txt:/etc/squid/allowed_clients.txt ubuntu/squid:latest


Proxy will be available on port 3128.

To change allowed IPs, edit file allowed_clients.txt and restart server.