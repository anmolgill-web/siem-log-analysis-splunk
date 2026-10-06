# Splunk Search to view all the logs
>index=* (to view logs of all indexes) <br>
index=main (by default index container is "main")
<img width="1912" height="862" alt="image" src="https://github.com/user-attachments/assets/0fda9b31-8ec0-43f6-acd7-ff4f41812d1f" />

## Authentication Logs
I will analyse these logs for Brute-force or suspicious logon attempts.
### 1.) Failed Logons
>index=main EventCode=4625
<img width="1915" height="862" alt="image" src="https://github.com/user-attachments/assets/eb16cab2-6905-4ac7-9948-cd4e55835ee1" />

### 2.) Successfull Logons
>index=main EventCode=4624
<img width="1912" height="865" alt="image" src="https://github.com/user-attachments/assets/eb216250-3289-4f98-afb5-4632d4b90f2b" />

### Analysis:
1.) There is no brute-force attack as there are 4 failed login attempts. <br>
2.) The login is attempted from a legitimate account from the system only( Logontype=2). <br>
3.) I have checked Computer Name, Workstation, Source network address, nothing suspicious. 
## Further Investigation if found suspicious
### 1.) Special Privileges Assigned
>index=main EventCode=4672
### 2.) User/group enumeration
>index=main EventCode=4798
### 3.) Failed login count
>index=main  EventCode=4625 <br>
| stats count
<img width="1907" height="861" alt="image" src="https://github.com/user-attachments/assets/34eac2f6-59fc-4c24-b85b-aec4f5e92e5c" />

### 4.) Failed logins by username
>index=main  EventCode=4625 <br>
| stats count by user <br>
| sort - count
### 5.) Failed logins by source IP
>index=main  EventCode=4625 <br>
| stats count by Source_Network_Address <br>
| sort - count


