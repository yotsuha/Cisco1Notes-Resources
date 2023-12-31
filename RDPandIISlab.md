# RDP (Remote Desktop Protocol) and IIS (Web Server) Lab - Intro to Networking

## Configure Vlan 1 for Switch 1
```
enable
config t

enable secret ajyuvraj

int vlan 1
ip addr 192.168.10.2 255.255.255.0
no shut
```
## Configure telnet on Switch 1
```
line vty 0 4
password ajyuvraj
login
```
## Configure Router 1 interfaces & SSH
```
enable
config t

enable secret ajyuvraj

int gig 0/0
ip addr 192.168.10.1 255.255.255.0
no shut

int gig 0/1
ip addr 10.10.10.1 255.0.0.0
no shut
exit

ip route 0.0.0.0 0.0.0.0 10.10.10.2

ip domain name AJyuvrajR1SSH
crypto key generate rsa
enable password ajyuvraj1
username yuyuR1 password yuyuR1
ip ssh version 2
line vty 0 5
transport input ssh
login local
```

## Disable Firewall RDP PC
```
Control Panel > System and Security > Windows Defender Firewall > On the left, click 'Turn Windows Defender Firewall on or off' > Turn on 'Turn off Windows Defender Firewall (not recommended)' under both Public and Private Network Settings > Press 'OK'
```


## Configure Vlan 1 for Switch 2
```
enable
config t

enable secret ajyuvraj

int vlan 1
ip addr 172.16.10.2 255.255.255.0
no shut
```
## Configure telnet on Switch 2
```
line vty 0 4
password ajyuvraj
login
```
## Configure Router 2 interfaces & SSH
```
enable
config t

enable secret ajyuvraj

int fa 0/0
ip addr 172.16.10.1 255.255.255.0
no shut

int fa 0/1
ip addr 10.10.10.2 255.0.0.0
no shut
exit

ip route 0.0.0.0 0.0.0.0 10.10.10.1

ip domain name AJyuvrajR2SSH
crypto key generate rsa
enable password ajyuvraj1
username ajR2 password ajR2
ip ssh version 2
line vty 0 5
transport input ssh
login local
```

## Disable Firewall IIS PC
```
Control Panel > System and Security > Windows Defender Firewall > On the left, click 'Turn Windows Defender Firewall on or off' > Turn on 'Turn off Windows Defender Firewall (not recommended)' under both Public and Private Network Settings > Press 'OK'
```
