# RDP and IIS Lab - Intro to Networking

## Configure Vlan 1 for Switch 1
```
enable
config t

enable secret <password> (cde13f737e9665ecff904ba43f12f67ae995331ef2a2142f6bbee4f3b3b30f90b2162942c5dcf2f9b2d483398c82095496e90ba13d9c3850fa2cf142b70bfe53)

int vlan 1
ip addr 192.168.10.2 255.255.255.0
no shut
```
## Configure telnet
```
line vty 0 4
password <password> (cde13f737e9665ecff904ba43f12f67ae995331ef2a2142f6bbee4f3b3b30f90b2162942c5dcf2f9b2d483398c82095496e90ba13d9c3850fa2cf142b70bfe53)
login
```
## Configure Router 1 interfaces
```
enable
config t

enable secret <password> (cde13f737e9665ecff904ba43f12f67ae995331ef2a2142f6bbee4f3b3b30f90b2162942c5dcf2f9b2d483398c82095496e90ba13d9c3850fa2cf142b70bfe53)

int gig 0/0
ip addr 192.168.10.1 255.255.255.0
no shut

int gig 0/1
ip addr 10.10.10.1 255.0.0.0
no shut

line vty 0 4
password <password> (cde13f737e9665ecff904ba43f12f67ae995331ef2a2142f6bbee4f3b3b30f90b2162942c5dcf2f9b2d483398c82095496e90ba13d9c3850fa2cf142b70bfe53)
login
```
