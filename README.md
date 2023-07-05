# Autopilot Tool – Upload HW hash with a user interface

<P> <Strong> ✅Download: </Strong> Click on a (preferably the latest) release to the right ---> </p> <br>

Download from GitHub:
https://github.com/NicklasAhlberg/AutoPilotTool 

.Version 1.0.3.0 (2023-07-05)
- The tool has been updated to reflect the changes done to MS Graph.
- Changes to the UI
 - No need to pre-define the tenant/domain name, just sign on and you are good to go
- A registered app is needed

.Version 1.0.2.6 (2022-12-14)
- It is now possible to add multiple domains to the config-file. 

.Version 1.0.2.5
- It is now possible to add a default tag to the config file

.Version 1.0.2.4
- Slightly new graphical interface
- Optional: It is now possible to add a group tag!
- Use the gather logs button to get autopilot logs as a CAB file

.Version 1.0.2.3 (2021-08-17)
It is now possible to set a default domain name. Get the latest version (1.0.2.3) from GitHub and you will find "config.txt" - edit as per your need. Thanks Dylan Brown for the idea!

.Version 1.0.2.2
It is now possible to use a custom logo. Place "logo.png" in the same directory as the .exe
Recommended logo size: 210x110 px

If you have been working with Windows Autopilot you know that manual upload of the hardware hash is a repetitive and time consuming task. 

This tool will make your life easier by...

Install the necessary PowerShell modules

Connect to the tenant (MFA is supported)

Automatically uploading the autopilot hash to the Windows Autopilot service

Let you know when the upload has completed (success or error)

.... directly from the device! 

No more need to struggle to manually get, move and import the csv-file from another device. All you need to do is run the tool (Shift+F10 when you get to pick your keyboard layout), start Autopilot Tool and sign in to Azure with an administrative user. This works well with MFA!

Instructions

The Autopilot Tool will require a registered app in your tenant to be allowed to run the MS Graph calls. Follow the prerequisites at the end of this blog post for guidance on how to set that up.

Open: Config.txt and add your tenant and client (application) ids and a group tag (save and close)

Place: "Autopilot Tool.exe" and "config.txt" in same directory on either a USB-stick or on a network location

Press: Shift+F10 when you are at the "pick your keyboard layout" screen

Write: PowerShell + hit enter to start PowerShell

Run: Install-Module MSAL.PS to install the needed PowerShell module (more info: AzureAD/MSAL.PS (github.com) )

Navigate to "Autopilot Tool.exe", press enter to start the tool

Optional: add a group tag

Click: Upload and sign in with a user with sufficient privileges

The hash will be uploaded to the Windows Autopilot service automatically after 2-3 minutes (the tool will query the service and let you know as soon as it is ready).

Download the tool from Github:
https://github.com/NicklasAhlberg/AutoPilotTool

Windows 10 versionSupported21H1OK20H2OK2004OK1909OK1903OKAll Windows 11OK

Prerequisites: Register the app

We will use an Azure registered app with delegated permissions to execute our MS Graph calls against. Please note that the app itself cannot do changes beyond these permissions even if the user running the tool has more permissions, and the other way around. The next steps cover how to create the app and delegate the appropriate permissions.

You will need either Global Administrator or Application Administrator to register the app in Azure

Navigate to: https://portal.azure.com

Click: Azure Active Directory

Click: App registrations

Click: New registration

Name: I will use ‘Demo-Graph‘, but you may name the app differently (What about “Autopilot Tool”?)

Supported account types: Accounts in this organizational directory only

Redirect URI (Select a platform): Public client/native (mobile and desktop)

Redirect URI (URL): https://login.microsoftonline.com/common/oauth2/nativeclient

Click: Register

Save the Application (client) ID in notepad, we will need it later

Click: API Permissions

Click: Microsoft Graph

Click: Delegated permissions

Search for and mark:

DeviceManagementServiceConfig.ReadWrite.All

Click: Add permissions ❗below printscreens have been reused from another post and includes more permissions than needed by the Autopilot Tool. DeviceManagementServiceConfig.ReadWrite.All is enough in our case.

Click: Grant admin consent for…

Click: Yes

Make sure that the permissions have been granted accordingly

Now navigate to https://portal.azure.com/

Click: Azure Active Directory

Save the Tenant ID in notepad, we will need it later.
