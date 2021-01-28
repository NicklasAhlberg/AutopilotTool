# AutoPilot Tool – Upload HW hash with a user interface
If you have been working with Windows Autopilot you know that manual upload of the hardware hash is a repetitive and time consuming task.

**This tool will make your life easier by…**

*-Install the necessary PowerShell modules*

*-Connect to the tenant (MFA is supported)*

*-Import the hardware hash.csv-file to the tenant*

*-Initiate a sync*

…. directly from the device! 

No more need to struggle with USB-keys and import the csv-file from another device. All you need to do is run the tool (Shift+F10 when you get to pick your keyboard layout), start Autopilot Tool and sign in to Azure (when you get prompted) with an administrative user. This works well with MFA!


![alt text](https://github.com/NicklasAhlberg/AutopilotTool/blob/main/AutopilotTool.gif?raw=true)

| Windows 10 version | Supported |
| ------- | ------------------ |
| 20H2  | :white_check_mark: |
| 2004  | :white_check_mark: |
| 1909  | :white_check_mark: |
| 1903  | :white_check_mark: |

This is a UI to Nickolaj Andersens script found at: 
https://github.com/MSEndpointMgr/Intune/blob/master/Autopilot/Upload-WindowsAutopilotDeviceInfo.ps1
