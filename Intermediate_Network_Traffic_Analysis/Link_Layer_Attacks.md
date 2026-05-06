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

