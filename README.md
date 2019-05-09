# Disable GlobalProtect by Network

These are instructions on how to enable and disable the GlobalProtect VPN based 
on the network connection that your Mac is connected to. The network name is 
hard coded into the script. That is currently `DDMGuest` for this script.

Here are the installation steps.

* Disable GlobalProtect automatic restart
* Install the script
* Give the script (or ScriptEditor) assistive access
* Set the script to start automatically

## Disable GlobalProtect automatic restart

* Follow instructions at https://richddean.com/post/147155656349/stopautostartglobalprotectvpn

## Install the script

Clone this project or save the GlobalProtectSwitcher.scpt file somewhere on 
your Mac. The script opens or closes the GlobalProtect VPN application based 
on the Wifi network you're connected to. It's currently written to open 
GlobalProtect when you're on the _DDMGuest_ network and close it when you're 
on any other network.

## Give the script assistive access

You will probably be prompted. Maybe. You'll need root access to the machine to 
do this.

## Set the script to start automatically

... TODO ...