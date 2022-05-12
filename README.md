# py_firewall
A firewall built from scratch using iptables and written in python.

# Firewall from scratch
The aim of this project is to implement a basic firewall to filter the network traffic for the IITJ campus which blocks all the video streaming websites. We used the linux kernel functionality, IPTABLES, for this purpose. IPTABLES, simply monitors & applies a set of rules using tables which contain sets of rules, called chains, that will filter incoming and outgoing data packets in a local network.


Some of the most important IPTABLE codes are:-
```
# to block an ip address
$ sudo iptables -A INPUT -s <IP Address> -j DROP
```
```
# to unblock an ip address
$ sudo iptables -D INPUT -s <IP Address> -j DROP
```
```
# to list out all the rules of iptables
$ sudo iptables -L
```
```
# to flush and delete all the rules of iptables
$ sudo iptables -P INPUT ACCEPT
$ sudo iptables -P FORWARD ACCEPT
$ sudo iptables -P OUTPUT ACCEPT
$ sudo iptables -t nat -F
$ sudo iptables -t mangle -F
$ sudo iptables -F
$ sudo iptables -x
```

The overall workflow of iptables can be understood as follows:-
