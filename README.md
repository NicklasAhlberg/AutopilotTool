# AutopilotTool
If you have been working with Windows Autopilot you know that manual upload of the hardware hash is a repetitive and time consuming task.

This tool will make your life easier by….

Install the necessary PowerShell modules
Connect to the tenant (MFA is supported)
Import the hardware hash.csv-file to the tenant
Run a sync
…. directly from the device! No more need to struggle with USB-keys and import the csv-file from another device. All you need to do is run the tool (Shift+F10 when you get to pick your keyboard layout) and sign in with an administrative user.

This is a UI to Nickolaj Andersens script found at: https://github.com/MSEndpointMgr/Intune/blob/master/Autopilot/Upload-WindowsAutopilotDeviceInfo.ps1

![alt text](https://github.com/NicklasAhlberg/AutopilotTool/blob/main/AutopilotTool.gif?raw=true)
