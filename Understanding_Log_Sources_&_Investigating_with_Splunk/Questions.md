# Introduction To Splunk & SPL
## Question 1:
Navigate to http://[Target IP]:8000, open the "Search & Reporting" application, and find through an SPL search against all data the account name with the highest amount of Kerberos authentication ticket requests. Enter it as your answer.
* SPL
```
index=* krbtgt 
| stats count by Account_Name 
| sort - count
```
* Answer
```text
waldo
```

## Question 2:
Navigate to http://[Target IP]:8000, open the "Search & Reporting" application, and find through an SPL search against all 4624 events the count of distinct computers accessed by the account name SYSTEM. Enter it as your answer.
* SPL
```
index=* EventCode=4624 Account_Name=SYSTEM 
| stats dc(ComputerName) as distinct_computers
```
* Answer
```text
10
```

