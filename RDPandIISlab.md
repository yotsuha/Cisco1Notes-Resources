# RDP and ISS Lab - Intro to Networking

## Configure Vlan 1 for Switch 1
```
enable
config t
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
$
