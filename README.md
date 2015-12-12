#Universal Data Aquisition Network System


#SensorMonitoring
In this project a system should be developed which is possible to carry out several sensor measurements and to send the values over WLAN to a central system. 
Afterwards in the central system the measuring results should be evaluated and documented for a period. 

![Bottom](https://github.com/NicoZellinger/SensorMonitoring/blob/master/docu/v10_b3.png)
![Bottom](https://github.com/NicoZellinger/SensorMonitoring/blob/master/docu/v10_t2.png)


# Hardware
In the essentials the sensor board is a WLAN module, a microcontroller and any sensor. 
The microcontroller reads the values of the sensor in a configureable frequency and transfers this to the WLAN module. 
The WLAN module sends the values to the central system (Raspberry Pi with Raspbian). 
Afterwards on the central system the measuring results are evaluated and documented. 
Beyond it, the central system administered the sensor boards. 


# Power
So that the sensor boards can be used mobile, the boards are supplied with a 3 volt battery. 
To put off the unloading of the battery as long as possible a "ultra low power" microcontroller from STMicroelectronic is used.
Besides, the controller is moved, as long as he takes up no measurement, into the Sleep mode. 
Above, the WLAN module and the sensor is separated with the help of a FET from the supply voltage (As long as no measurement is made). 