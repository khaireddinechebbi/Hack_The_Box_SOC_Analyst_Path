## Question 1
Download the Wazuh exported logs file (i.e., wazuh_export.zip), and identify all events that indicate potential credential compromise. Check the event ID 4688 and verify the full path of the parent process name that executed a credential dumping tool. Answer format is C:\\Pr........
```bash
C:\\Program Files\\Mozilla Firefox\\firefox.exe
```

## Question 2:
Identify events that show persistence mechanisms. Type the value of imagePath for a persistence mechanism that took place on the host DB01.
```bash
C:\\Windows\\PSEXESVC.exe
```

## Question 3:
Identify exfiltration activity — file(s) uploaded or outbound traffic. What is the external IP address to which the file diagnostics_data.zip was uploaded?
```bash
93.184.216.34
```

## Question 4:
Which user tried to connect to the file share \\fs01\projects?
```bash
svc_admin
```
