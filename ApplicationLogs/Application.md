#  To see System Logs, add system rule in the "inputs.conf" file:
>[WinEventLog://Application] <br>
disabled = 0 <br>
start_from = oldest <br>
current_only = 0
# To see all event IDs in Application Logs:
>index=main sourcetype=WinEventLog:Application <br>
| stats count by EventCode <br>
| sort -count
# To investigate errors:
>index=main sourcetype=WinEventLog:Application (Type=Error OR Level=Error) 

One of the error I found:
<img width="1465" height="597" alt="image" src="https://github.com/user-attachments/assets/ef7ec7b3-e307-4f4b-a305-56285211f738" />
Generally, its not malicious as there is no other suspicous event related to it.
# To investigate warnings:
>index=main sourcetype=WinEventLog:Application (Type=Warning OR Level=Warning)

