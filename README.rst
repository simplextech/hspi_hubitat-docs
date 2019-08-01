HomeSeer Plugin: Hubitat Elevation
==================================

Mirror your Hubitat Elevation devices to your HomeSeer home automation server.

Features
--------

- Z-Wave Devices
- ZigBee Devices
- Lutron Radio RA2 / Caseta Pro 
- Philips Hue bridge
- LiFX
- TP-Link SmartPlugs (Limited support)
- More device support coming...

Installation
------------
Install from the Plug-in Manager:

    Plug-Ins -> Manage -> Additional Interfaces -> Lighting & Primary Technology

Configuration
-------------

- Pre-Requisites:
  Hubitat Hub setup with devices
  Hubitat Maker API app installed

- Go to Apps
- Add Built-In App
- Click Maker API in the list

  - Security - Local IP Address must be on. Cloud access is up to you
  - Select Devices (Click to Set)
  - Select the device(s) you want to be available through Maker API
  - Endpoints - Local URLS
  - Copy the "Get All Devices with Full Details" Link
  - You can come back to the Maker API app to get this link if you miss this step
  - Click Done

- Plugin Setup

  - Hubitat Maker API URL
  - Paste the URL form Step 2.4.1 above
  - Select your room/floor
  - Click Connect / Re-Scan Devices

In your HomeSeer Device page you will need to use the drop downs to make sure the 
room/floor/Device Types are checked to make the devices visible. If you suspect any problems 
go back to the plug-in setup and enable debug logging. This will output verbose details to the HS3 Log.

Support
-------
If you are having issues, please let us know.
`HomeSeer Hubitat Elevation Forum <https://forums.homeseer.com/forum/lighting-primary-technology-plug-ins/lighting-primary-technology-discussion/hubitat-elevation-simplex-technology>`_

Use Cases and Awesome Stuff
===========================

HubConnect
----------
This is an awesome Hubitat Community developed app.

`GitHub: HubConnect <https://github.com/HubitatCommunity/HubConnect>`_

`HubConnect Installation Instructions <https://github.com/HubitatCommunity/HubConnect/blob/master/HubConnect%20Installation%20Instructions.pdf>`_

`Hubitat Community Forum Thread <https://community.hubitat.com/t/release-hubconnect-share-devices-across-multiple-hubs-even-smartthings/12028>`_

HubConnect replaces the native HubLink/Link to Hub apps and includes the following enhancements:

- Support for multiple device attributes (i.e switch, power, voltage for a Zigbee Plug).
- Battery status is available for any device that supports it.
- Switches, Dimmers, RGB Bulbs, and Buttons are 2-way devices which can be controlled from the coordinator hub as well as the remote hub in which they are connected to.
- Fully bi-directional.  Connect physical devices from remote hubs to the coordinator AND devices on the coordinator to remote hubs!
- When a remote device is controlled from master, status updates (i.e. switch) are instantly sent by the remote device to ensure the device actually responded to the command.
- Full bi-directional SmartThings support including 2-way devices.
- Hub Health ensures each remote hub checks in with the coordinator every minute. If a hub fails to respond for 5 minutes it is declared offline.
- A virtual "hub presence" device is created for every linked remote hub. If the remote hub is responding, the status is "present", if it's offline the status is "not present".
- This uses the "HubConnect Beacon Sensor" and is done so rules can be created to notify when a hub is not responding.
- Flexible oAuth endpoints; Hubs do not need to be on the same LAN or even same location. 
- Remote hubs can be located anywhere with an internet connection.
- Communications between the master and remote hubs can be suspended for maintenance.  (i.e. rebooting the master hub as it prevents the remotes from logging http errors)
- Publish user-defined device drivers without modifying HubConnect source code.
- Mode changes can be pushed from the Server to Remote hubs, including SmartThings.
- Remote hub "Reboot-Recovery" checks-in with the Server hub to set the current system mode anytime a remote hub is rebooted.