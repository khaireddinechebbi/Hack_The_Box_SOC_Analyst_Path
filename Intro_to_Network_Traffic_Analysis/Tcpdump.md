# Tcpdump Fundamentals
## Question 1:
Utilizing the output shown in question-1.png, who is the server in this communication? (IP Address)
```bash
174.143.213.184
```

## Question 2:
Were absolute or relative sequence numbers used during the capture?
```bash
Relative
```

## Question 3:
If I wish to start a capture without hostname resolution, verbose output, showing contents in ASCII and hex, and grab the first 100 packets; what are the switches used? please answer in the order the switches are asked for in the question.
```bash
-nvXc 100
```

## Question 4:
Given the capture file at /tmp/capture.pcap, what tcpdump command will enable you to read from the capture and show the output contents in Hex and ASCII?
```bash
sudo tcpdump -Xr /tmp/capture.pcap
```

## Question 5:
What TCPDump switch will increase the verbosity of our output?
```bash
-v
```

## Question 6:
What built in terminal help reference can tell us more about TCPDump?
```bash
man
```

## Question 7:
What TCPDump switch will let me write my output to a file?
```bash
-w
```

# Fundamentals Lab
## Question 1:
What TCPDump switch will allow us to pipe the contents of a pcap file out to another function such as 'grep'?
```bash
-l
```

## Question 2:
True or False: The filter "port" looks at source and destination traffic.
```bash
True
```

## Question 3:
If we wished to filter out ICMP traffic from our capture, what filter could we use?
```bash
not icmp
```

## Question 4:
What command will show you where / if TCPDump is installed?
```bash
which tcpdump
```

## Question 5:
How do you start a capture with TCPDump to capture on eth0?
```bash
tcpdump -i eth0
```

## Question 6:
What switch will provide more verbosity in your output?
```bash
-v
```

## Question 7:
What switch will write your capture output to a .pcap file?
```bash
-w
```

## Question 8:
What switch will read a capture from a .pcap file?
```bash
-r
```

## Question 9:
What switch will show the contents of a capture in Hex and ASCII?
```bash
-X
```

# Tcpdump Packet Filtering
## Question 1:
What filter will allow me to see traffic coming from or destined to the host with an ip of 10.10.20.1?
```bash
host 10.10.20.1
```

## Question 2:
What filter will allow me to capture based on either of two options?
```bash
OR
```

## Question 3:
True or False: TCPDump will resolve IPs to hostnames by default.
```
True
```

# Interrogating Network Traffic With Capture and Display Filters
## Question 1:
What are the client and server port numbers used in first full TCP three-way handshake?
```bash
80 43806
```

## Question 2:
Based on the traffic seen in the pcap file, who is the DNS server in this network segment? (ip address)
```bash
172.16.146.1
```
