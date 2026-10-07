# Main Powershell search:
>index=main sourcetype=WinEventLog:PowerShell
<img width="1908" height="862" alt="image" src="https://github.com/user-attachments/assets/3c36d328-740f-4f85-a8cd-af13fcb0cefc" />

# Most Importants events:
##  Script Block Logging - 4104
>index=main sourcetype=WinEventLog:PowerShell EventCode=4104

This event needs to be enabled to see its logs otherwise logs will not be generated.
<img width="1912" height="868" alt="image" src="https://github.com/user-attachments/assets/46f5e002-39c1-458f-b8fb-0fadab81b319" />

##  Module Logging - 4103
>index=main sourcetype=WinEventLog:PowerShell EventCode=4103

## PowerShell engine started - 400
>index=main sourcetype=WinEventLog:PowerShell EventCode=400



