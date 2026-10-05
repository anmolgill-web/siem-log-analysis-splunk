# splunk-security-log-analysis
 Security log analysis and threat detection of a local system (Windows) using Splunk.
##  Install and Configure Splunk Enterprise
### Step-1: Downloaded Splunk Enterprise and then launched it to install the download.
### Step-2: When you install Splunk Enterprise on Windows, the software lets you select the Windows user that it should run as.
 The user that Splunk Enterprise runs as determines what Splunk Enterprise can monitor. The Local System user has access to all data on the local machine by default.
### Step-3: You can decide which logs to collect from the system like security logs, system logs, firewall logs, etc.
For this, Go to Splunk's location (by default: C:\Program Files\Splunk) : "C:\Program Files\Splunk\etc\system\local". <br>
In local Folder, search for "inputs.conf" file. If its not there create it. 
### Step-4: I created this file and then added rule to collect security logs from the system.
## Troubleshooting
### When I open the Splunk instance and went to "Search & Reporting" App, it was showing 0 events. <br>
It was because when I installed splunk, it was not using local user by default. So, I performed these steps: <br>
1.) Through "Win+R" opened "services.msc" tool( used to view and manage system services). <br>
2.) Find "Splunkd" service -> go to its properties -> go to "Log On" section -> select "Local System Account". <br>
3.) Restart the splunk.
