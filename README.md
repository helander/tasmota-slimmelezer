# tasmota-slimmelezer
##Run the tasmota firmware on the SlimmeLezer+ device

The tasmota project does not support out-of-the-box a downloadabe firmware image with Smart Meter Interface functionality included. However it is fairly easy to build such an image using available tasmota tools. The folder [firmware](firmware/README.md) provides a ready built tasmota firmware binary that includes the functionality to use the tasmota Smart Meter Interface on the SlimmeLezer+. Information about the process by which this image was created is also available. Download the image and upload it to your device using OTA.

Once you have the new firmware running on your device you need to upload a script file that includes the settings for your corresponding meter(s). Some details about this process is found in the folder [scripts](scripts/README.md).

My metering device is a Landis+Gyr E360 device and its script file is found [here](scripts/landisgyre360/script.txt).

If you have some other meter you would need to create your own script. [Here](other/README.md) you find some information that could be useful during the creation of your own script.
