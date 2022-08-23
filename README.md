# tasmota-slimmelezer
Run the tasmota firmware on the SlimmeLezer+ device (and other Smart Meter Interface devices).

The tasmota project does not out-of-the-box provide a firmware image with Smart Meter Interface functionality included. However it is fairly easy to build such an image using available tasmota tools. The folder [firmware](firmware/README.md) provides a ready built tasmota firmware binary that includes the functionality to use the tasmota Smart Meter Interface on the SlimmeLezer+. Information about the process by which this image was created is also available. Download the image and upload it to your device using OTA. Once the device is restarted with the new image it will expose a WiFi Access Point. You need to connect to this AP from a computer/phone/tablet and you will then be presented with a page where you can enter SSID and credentials for WiFi network the device should connect to.

Once you have the new firmware running on your device you need to add a script that includes the settings for your corresponding meter(s). Some details about this process is found in the folder [scripts](scripts).

My metering device is a Landis+Gyr E360 device and its script file is found [here](scripts/landisgyre360/script.txt).

If you have some other meter, you would need to create your own script. [Here](other/README.md) you find some information that could be useful during the creation of your own script.


The knowledge compiled in these pages are mostly based on the information found here:

* [Tasmota Smart Meter Interface](https://tasmota.github.io/docs/Smart-Meter-Interface/)
* [Tasmota Scripting](https://tasmota.github.io/docs/Scripting-Language/)
* [OBIS coding](https://www.promotic.eu/en/pmdoc/Subsystems/Comm/PmDrivers/IEC62056_OBIS.htm)


