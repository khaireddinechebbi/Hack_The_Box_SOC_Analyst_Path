# ARP Spoofing & Abnormality Detection
## Question 1:
Inspect the ARP_Poison.pcapng file, part of this module's resources, and submit the total count of ARP requests (opcode 1) that originated from the address 08:00:27:53:0c:ba as your answer.
* Filter
```
arp.opcode == 1 && eth.src == 08:00:27:53:0c:ba
```
* Note
```
Go to Statistics → Conversations → Ethernet
```
* Answer
```
507
```

# ARP Scanning & Denial-of-Service
## Question 1:
Inspect the ARP_Poison.pcapng file, part of this module's resources, and submit the first MAC address that was linked with the IP 192.168.10.1 as your answer.
* Filter
```
arp.opcode == 2 && arp.src.proto_ipv4 == 192.168.10.1
```
* Answer
```
2c:30:33:e2:d5:c3
```
