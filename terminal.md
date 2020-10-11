Find the process listening on the port:
```
lsof -i tcp:3080 (or with sudo if it might have a different owner)
```

Check port is listening on the remote machine
```
nc -zv localhost 2181
echo stat | nc localhost 2181
```

block outgoing connection to the IP address
```
iptables -A OUTPUT -d 1.2.3.4 -j DROP
```

allow access to the port for 1.2.3.4 IP but deny for everyone else
```
iptables -A INPUT -p tcp --dport 8000 -s 1.2.3.4 -j ACCEPT
iptables -A INPUT -p tcp --dport 8000 -j DROP
```

run in the background so that it wouldn't stop after terminating the session:
```
nohup commandname &
```
