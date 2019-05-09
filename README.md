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

Save the following code to a `gp.scpt` file. This enables and disables the 
GlobalProtect VPN application based on the Wifi network you're connected to. 
This script automatically connects to GlobalProtect when you are on the 
_DDMGuest_ network and closes GP when you are on any other network.

```
set globalProtectEnabled to false

repeat
	
	tell application "System Events" to tell process "SystemUIServer"
		set menuString to value of attribute "AXDescription" of menu bar items of menu bar 1
		set networkString to item 5 of menuString
	end tell
	
	# If the value returned contains the text "DDMGuest" then start GlobalProtect
	if networkString contains "DDMGuest" then
		if globalProtectEnabled is false then
			try
				tell application "GlobalProtect" to open
			end try
			display dialog "GlobalProtect Started"
			set globalProtectEnabled to true
		end if
	else
		tell application "GlobalProtect" to quit
		set globalProtectEnabled to false
	end if
	
	delay 15
	
end repeat
```
## Give the script assistive access

You will probably be prompted. Maybe. You'll need root access to the machine to 
do this.

## Set the script to start automatically

