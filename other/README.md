
# TCP/Serial bridge
The provided tasmota firmware image includes a TCP/Serial bridge function that can be configured to create a direct connection to the meter. This is useful in order to find out communication parameters and format of the information sent ny the meter. The script controlled Smart Meter Interface must not be enabled while using the TCP/Serial bridge (and vice versa). The script can be disabled via a tick box in the Edit Script web page. The TCP/Serial bridge is enabled via the Configure Module page. Yoe need to select the 2 GPIO pins connected to your meter and configure them as "TCP Rx" and "TCP Tx". To disable the TCP/Serial bridge the 2 GPIO pins needs to be configured as "None".

I received the following information from my meter using the TCP/Serial bridge:
```
/LGF5E360

0-0:1.0.0(220820130240W)
1-0:1.8.0(00000418.657*kWh)
1-0:2.8.0(00000024.461*kWh)
1-0:3.8.0(00000000.000*kVArh)
1-0:4.8.0(00000411.846*kVArh)
1-0:1.7.0(0000.000*kW)
1-0:2.7.0(0000.351*kW)
1-0:3.7.0(0000.000*kVAr)
1-0:4.7.0(0001.554*kVAr)
1-0:21.7.0(0000.189*kW)
1-0:22.7.0(0000.000*kW)
1-0:41.7.0(0000.000*kW)
1-0:42.7.0(0000.384*kW)
1-0:61.7.0(0000.000*kW)
1-0:62.7.0(0000.157*kW)
1-0:23.7.0(0000.000*kVAr)
1-0:24.7.0(0000.334*kVAr)
1-0:43.7.0(0000.000*kVAr)
1-0:44.7.0(0000.511*kVAr)
1-0:63.7.0(0000.000*kVAr)
1-0:64.7.0(0000.708*kVAr)
1-0:32.7.0(231.4*V)
1-0:52.232.3*V)
1-0:31.7.0(001.6*A)
1-0:51.7.0(002.7*A)
1-0:71.7.0(003.1*A)
!B1D8
```

Each line with a sensor value is prefixed with the sensor type according to the information [here](https://www.promotic.eu/en/pmdoc/Subsystems/Comm/PmDrivers/IEC62056_OBIS.htm).

I used this information to create the sensor lines in my [script file](../scripts/landisgyre360/script.txt).
