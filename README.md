# Disable GlobalProtect by Network

This is an application, written in AppleScript, that enables and disables the 
GlobalProtect VPN based on the WiFi network that your Mac is connected to. The 
network name, _DDMGuest_ is hard coded into the script.

## Installation Overview

* Disable GlobalProtect automatic restart
* Download the application
* Set the script to start automatically
* Log out and then back in to Mac OS
* Give the app accessibility access

## Disable GlobalProtect automatic restart

* Follow instructions at https://richddean.com/post/147155656349/stopautostartglobalprotectvpn

## Download the application

Clone this project or save the `GlobalProtectSwitcher.app` file somewhere on 
your Mac. The app opens or closes the GlobalProtect VPN application based 
on the WiFi network you're connected to. It's currently written to open 
GlobalProtect when you're on the _DDMGuest_ network and close it when you're 
on any other network. You'll have to edit the `.scpt` file and then export it as 
an application to change the network name. You must edit the `.scpt` file with 
the Mac OS Script Editor.

## Set the script to start automatically

* Open _System Preferences_
* Select _Users & Groups_
* Select _Login Items_ (for your user account)
* Click the plus (_+_) button
* Find and select the _GlobalProtectSwitcher.app_ file
* Optionally, check the _hide_ checkbox

## Give the app accessibility access

When you log back in you'll be prompted to give the application Accessibility 
permissions. These are necessary in order for the application to automatically 
open and close GlobalProtect.

## Log out and then back in to Mac OS

You should log out of Mac OS and then log back in to make sure that the 
application starts and is working.

## The Files

* `README.md` is this readme file
* `GlobalProtectSwitcher.scrp` is the AppleScript source code
* `GlobalProtectSwitcher.app` is the compiled application
