# tasmota-slimmelezer
Run the tasmota firmware on the SlimmeLezer+ device

In order to use tasmota on the SlimmerLezer+ device two pieces of information is required:
* a tasmota firmware binary that includes support for tasmota scripting
* a tasmota script that provides settings related to the specific metering device 

My metering device is a Landis+Gyr E360 device and its setup script is found in the file scripts/landisgyre360.txt.

In order to use some other metering device, additional scripts or updates to existing scripts would be required. The process is roughly as follows:
* Find out the format and scope of the information coming from the metering device. This is most easily done by first removing all Smart Meter definitions from the currently active Smart Device and then add definitions for the ...
