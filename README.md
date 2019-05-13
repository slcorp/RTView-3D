# RTView-3D

This repository provides information and examples that show how to render and implement data-driven animation of 3D graphical models within RTView displays.   

**RTView** is a real-time data management, visualization and analytics engine provided by SL Corporation (www.sl.com). It is used by organizations worldwide as a key component of mission-critical monitoring and control systems built around various middleware, infrastructure, telemetry and IoT data sources.

In such applications, it is often most effective to present real-time dynamic data in a 3-dimensional representation. For example, a satellite telemetry feed containing information about the orientation of its solar panels might best be visualized using a 3D rendering of the solar panels rotated in real-time as the data change. This and many other similar displays can readily be created and published to users using the tools available with RTView.

![](assets/images/sample-car-3d.png)

**[Three.js](https://threejs.org/)** is widely used 3D Javascript rendering library, specifically designed for use in HTML browser applcations. With it one can create and render complex dynamic 3D models, as well as import models created with tools such as AutoCAD, Blender, Maya, and others. This repository shows how to use Three.js to render models within the context of RTView and manipulate them with real-time data accessed from datasources provided by RTView.

In addition, displays containing 3D representations can be combined with other real-time displays such as charts, tables, diagrams, and more, to create complete dashboard applications for monitoring and controlling complex applications or processes.

By following the steps described below you will:

* Create an account on RTView Cloud.
* Upload a set of sample 3D model files to your RTView Cloud account.
* Create, deploy, and publish displays that drive these sample models with real-time data.
* Learn how to create your own 3D models and extend RTView in new ways.

## Create an RTView Cloud account
An RTView Cloud account provides the tools for creating, viewing and publishing rich graphical displays connected to real-time data sources.

* In a browser, go to [RTView Cloud](http://rtviewcloud.sl.com/).
* Click on Start Free Trial to create your account (skip if you have an account already).
* Login to your RTView Cloud account.

Note that you are automatically placed into your own private organization (e.g. JohnSPrivateOrg).

## Upload the sample 3D HTML snippets to RTView Cloud

* In a browser, go to [RTView Cloud](http://rtviewcloud.sl.com/).

* Upload the sample 3D models to an RTView Cloud Assets folder: 
```
On the RTView Cloud top menu bar, open the Settings menu (select the 'gear' icon).
Choose the Assets option.
Select 'Create Directory' and enter 'html' to create a folder to hold your HTML assets (skip if it exists).
Select the 'html' folder.
Choose 'Add File', navigate to the 'assets/html' folder in this github repo,
    and select one or all of the html snippets to upload.
Select 'Open' to initiate the upload process. 
```

## Import and view the sample displays

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
