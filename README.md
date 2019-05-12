# RTView-3D

This repository provides information and examples that show how to render and implement data-driven animation of 3D graphical models within RTView displays.   

RTView is a real-time data management, visualization and analytics engine provided by SL Corporation (www.sl.com). It is used by organizations worldwide as a key component of mission-critical monitoring and control systems built around various middleware, infrastructure, telemetry and IoT data sources.


## Create an RTView Cloud account
An RTView Cloud account provides the tools for creating, viewing and publishing rich graphical displays connected to real-time data sources.

* In a browser, go to [RTView Cloud](http://rtviewcloud.sl.com/).
* Click on Start Free Trial to create your account (skip if you have an account already).
* Login to your RTView Cloud account.

Note that you are automatically placed into your own private organization (e.g. JohnSPrivateOrg).

## Upload the sample 3D HTML snippets to RTView Cloud

* In a browser, go to [RTView Cloud](http://rtviewcloud.sl.com/).

* Upload the sample 3D models to an RTView Cloud Assets folder. 
```
On the RTView Cloud top menu bar, open the Settings menu (select the 'gear' icon).
Choose the Aseets option.
Select 'Create Directory' and enter 'html' to make a directory to hold your HTML assets (skip if it exists).
Select the 'html' directory.
Choose 'Add File', navigate to the 'html' folder in this repo and select the assets you'd like to upload.
Select 'Open' to start the opload process. 
```

## Import and view the sample display

* In a browser, go to [RTView Cloud](http://rtviewcloud.sl.com/).

* Define a connection to the RTView DataServer running on your local system:
```
On the RTView Cloud top menu bar, select Data.
Select the Add RTView Server button.
In the Add RTView Server dialog enter:

	Name:       SIMPLE-EXAMPLE-SERVER
	Host/URL:   http://localhost:3270/rtvquery

Click on Save Added Servers.
```
* Test that the connection is successful:
```
Click on the green magnifying glass icon next to the SIMPLE-EXAMPLE-SERVER entry.
This will invoke the RTView DataServer - Cache Tables dialog.
Verify that you see "Connected" under Connection Status. 
Verify that you see SensorData in the CacheTable.
Close the dialog.
```
* Import the sample display:
```
On the RTView Cloud top menu bar, click on Design to invoke the RTDraw visual editing tool.
Select the File dropdown menu and click on Import.
Select "as Private". 
In the file browser, navigate to the RTView-JavaSccript directory within this project on your computer.
Select the SimpleExample.json and click Open.
```
* View or edit the sample display:
```
Select the File dropdown menu and click on Open...
Double click the name of the display you just imported, to open and view it in real-time.
```
This sample display is configured to connect to your local RTView data server and present data changing in real-time.
You can experiment with the editing features of RTDraw to make changes to these displays or create your own.

## Achieved Goals
In this RTView JavaScript you will have achieved the following: 
* Seen how easy it is to display user data in graphical and highly configurable displays in the Cloud.
* Launched the simple node program used to create and send data to RTView.
* Seen how users are able to view or enhance a sample RTView display or create new displays.

**Feel free to experiment with, modify or enhance this project, and share your experience, comments and suggestions with us. Please fork this repo and submit a pull request for any changes you would like to suggest.**
