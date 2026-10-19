
# To see System Logs, add system rule in the "inputs.conf" file:
>[WinEventLog://System] <br>
disabled = 0 <br>
start_from = oldest <br>
current_only = 0
# See all Event Ids in System
>index=main sourcetype=WinEventLog:System <br>
| stats count by EventCode <br>
| sort -count
<img width="1915" height="865" alt="image" src="https://github.com/user-attachments/assets/3b5f9861-3e60-4d10-a1d7-2205d9ac1d1f" />

# Common Event Ids to search for (from security perspective)
## 1.) Service started — 7036
>index=main sourcetype=WinEventLog:System EventCode=7036
<img width="1917" height="865" alt="image" src="https://github.com/user-attachments/assets/df92bcdf-f909-4d48-b029-78824b792e61" />

## 2.) Service failed — 7031
>index=main sourcetype=WinEventLog:System EventCode=7031
## 3.) Service crashed unexpectedly — 7034
>index=main sourcetype=WinEventLog:System EventCode=7034
## 4.) Service installation — 7045 (Its very important event as attackers can create services for persistence)
>index=main sourcetype=WinEventLog:System EventCode=7045
<img width="1915" height="867" alt="image" src="https://github.com/user-attachments/assets/35bccd04-ef7b-4f85-b6dd-097ade306fdd" />

### Service installation events:
Nothing suspicious as legitimate services were installed by legitimate softwares.
## 5.) System startup — 6005
>index=main sourcetype=WinEventLog:System EventCode=6005
## 6.) System shutdown — 6006
>index=main sourcetype=WinEventLog:System EventCode=6006

