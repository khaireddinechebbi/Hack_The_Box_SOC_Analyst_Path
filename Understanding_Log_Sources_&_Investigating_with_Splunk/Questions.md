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

## Question 3:
Navigate to http://[Target IP]:8000, open the "Search & Reporting" application, and run a SPL search against all 4624 events. Identify the accounts whose total login activity occurred within a time range of less than 10 minutes. As your answer, enter the name of the account having highest login attempts.
* SPL
```
index=* EventCode=4624 
| stats count min(_time) as firstTime max(_time) as lastTime by Account_Name
| eval duration=lastTime - firstTime
| where duration < 600
| sort - count
```
* Answer
```text
aparsa
```


