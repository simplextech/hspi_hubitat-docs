HomeSeer Plugin: Hubitat Elevation
========

Mirror your Hubitat Elevation devices to your HomeSeer 3 home automation server.

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
