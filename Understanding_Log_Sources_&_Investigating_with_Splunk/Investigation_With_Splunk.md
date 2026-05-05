# Intrusion Detection With Splunk (Real-world Scenario)
## Question 1:
Navigate to http://[Target IP]:8000, open the "Search & Reporting" application, and find through an SPL search against all data the other process that dumped lsass. 
* SPL
```
index="main" sourcetype="WinEventLog:Sysmon" EventCode=10 TargetImage="*lsass.exe"  SourceUser=*waldo*
```
* Answer
```text
rundll32.exe
```

## Question 2:
Navigate to http://[Target IP]:8000, open the "Search & Reporting" application, and find through SPL searches against all data the method through which the other process dumped lsass. Enter the misused DLL's name as your answer.
* SPL
```
index=* sourcetype="WinEventLog:Sysmon" CommandLine="*.dll* *lsass*"
```
* Answer
```text
comsvcs.dll
```

## Question 3:
Navigate to http://[Target IP]:8000, open the "Search & Reporting" application, and find through an SPL search against all data any suspicious loads of clr.dll that could indicate a C# injection/execute-assembly attack. Then, again through SPL searches, find if any of the suspicious processes that were returned in the first place were used to temporarily execute code.
* SPL
```
index="main" sourcetype="WinEventLog:Sysmon" EventCode=10 TargetImage="*lsass.exe"
```
* Answer
```text
rundll32.exe
```

## Question 4:
Navigate to http://[Target IP]:8000, open the "Search & Reporting" application, and find through SPL searches against all data the two IP addresses of the C2 callback server.
* SPL
```
index="main" sourcetype="WinEventLog:Sysmon" EventCode=3 (Image="*rundll32.exe" OR Image="*cmd.exe" OR Image="*randomfile.exe" OR Image="*SharpHound.exe") | table _time, Image, DestinationIp, DestinationPort
```
* Answer
```text
10.0.0.186 and 10.0.0.91
```

## Question 5:
Navigate to http://[Target IP]:8000, open the "Search & Reporting" application, and find through SPL searches against all data the port that one of the two C2 callback server IPs used to connect to one of the compromised machines.
* SPL
```
index="main" sourcetype="WinEventLog:Sysmon" (SourceIp="10.0.0.91" OR SourceIp="10.0.0.186") | table _time, SourceIp, SourcePort, DestinationIp, DestinationPort, Image
```
* Answer
```text
3389
```
