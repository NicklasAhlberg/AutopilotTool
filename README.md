# AutoPilot Tool – Upload HW hash with a user interface

<P> <Strong> Download: </Strong> Click on a (preferably the latest) release to the right ---> </p> <br>

If you have been working with Windows Autopilot you know that manual upload of the hardware hash is a repetitive and time consuming task.

**This tool will make your life easier by…**<br>
*- Install the necessary PowerShell modules*<br>
*- Connect to the tenant (MFA is supported)*<br>
*- Import the hardware hash.csv-file to the tenant*<br>
*- Initiate a sync*

…. directly from the autopilot device! 

No more need to struggle to manually get, move and import the csv-file from another device. All you need to do is run the tool (Shift+F10 when you get to pick your keyboard layout), start Autopilot Tool and sign in to Azure (when you get prompted) with an administrative user. This works well with MFA!

<p><strong>.Version 1.0.2.4</strong><br>
– Slightly new graphical interface<br>
– Optional: It is now possible to add a group tag!<br>
– Use the gather logs button to get autopilot logs as a CAB-file<br>
</p>

<!-- wp:paragraph -->
<p><strong>.Version 1.0.2.3</strong><br>It is now possible to set a default domain name. Get the latest version (1.0.2.3) from GitHub and you will find "<strong>config.txt</strong>" - edit as per your need. Thanks <strong>Dylan Brown</strong> for the idea!</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Example: <br></strong><img class="wp-image-552" style="width: 244px;" src="https://usercontent.one/wp/www.nicklasahlberg.se/wp-content/uploads/2020/11/Snag_915c09.png" alt=""><br></p>
<!-- /wp:paragraph -->

.Version 1.0.2.2<br>
It is now possible to use a custom logo. Place "logo.png" in the same directory as the .exe<br>
Recommended logo size: 210x110 px

**Instructions**<br>
1. Download latest release and extract the .ZIP-file. Make sure "Autopilot Tool.exe", "Logo.png" and "config.txt" are in the same directory on either a USB-stick or on a network location<br>
2. Press Shift+F10 when you are at the "pick your keyboard layout" screen<br>
3. Navigate to "Autopilot Tool.exe", press Enter to start the tool<br>
4. Change yourDomain.onmicrosoft.com to your specific need<br>
5. Update: it is now possible to edit config.txt to add a default domain
6. Optional: add a group tag
7. Press the OK-button<br>
8. Sign-on with an Intune Administrator account (or similar) when prompted<br>
9. The HW hash has now been uploaded and will be visible in the Windows Autopilot service
10. Update: press "Gather Logs" to create a CAB-file with all autopilot logs. Use this to troubleshoot the autopilot deployment

![alt text](https://www.nicklasahlberg.se/wp-content/uploads/2021/08/Autopilot_GIF_new.gif)

| Windows 10 version | Supported |
| ------- | ------------------ |
| 21H1  | :white_check_mark: |
| 20H2  | :white_check_mark: |
| 2004  | :white_check_mark: |
| 1909  | :white_check_mark: |
| 1903  | :white_check_mark: |
