## Question 1:
Analyze the event with ID 4624, that took place on 8/3/2022 at 10:23:25. Conduct a similar investigation as outlined in this section and provide the name of the executable responsible for the modification of the auditing settings as your answer. Answer format: T_W_____.exe
```powershell
TiWorker.exe
```

## Question 2:
Build an XML query to determine if the previously mentioned executable modified the auditing settings of C:\Windows\Microsoft.NET\Framework64\v4.0.30319\WPF\wpfgfx_v0400.dll. Enter the time of the identified event in the format HH:MM:SS as your answer.
```powershell
10:23:50
```

## Question 3:
Replicate the DLL hijacking attack described in this section and provide the SHA256 hash of the malicious WININET.dll as your answer. "C:\Tools\Sysmon" and "C:\Tools\Reflective DLLInjection" on the spawned target contain everything you need.
```powershell
51F2305DCF385056C68F7CCF5B1B3B9304865CEF1257947D4AD6EF5FAD2E3B13
```

## Question 4:
Replicate the Unmanaged PowerShell attack described in this section and provide the SHA256 hash of clrjit.dll that spoolsv.exe will load as your answer. "C:\Tools\Sysmon" and "C:\Tools\PSInject" on the spawned target contain everything you need.
```powershell
8A3CD3CF2249E9971806B15C75A892E6A44CCA5FF5EA5CA89FDA951CD2C09AA9
```

## Question 5:
Replicate executing Seatbelt and SilkETW as described in this section and provide the ManagedInteropMethodName that starts with "G" and ends with "ion" as your answer. "c:\Tools\SilkETW_SilkService_v8\v8" and "C:\Tools\GhostPack Compiled Binaries" on the spawned target contain everything you need.
```powershell
GetTokenInformation
```

## Question 6:
Utilize the Get-WinEvent cmdlet to traverse all event logs located within the "C:\Tools\chainsaw\EVTX-ATTACK-SAMPLES\Lateral Movement" directory and determine when the \\*\PRINT share was added. Enter the time of the identified event in the format HH:MM:SS as your answer.
```powershell
12:30:30
```
