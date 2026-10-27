# ESP-NOW_WiFi_Gateway
A Gateway between ESP-NOW sensors and your WiFi/MQTT/Pushover......etc

Currently Still awaiting the hardware to test but this is what it should look like
<img width="1840" height="1183" alt="image" src="https://github.com/user-attachments/assets/d3dd373d-776d-4292-bb3b-342299cdb658" />

There are locations for 2 Xaio ESP32 S3s the one on the right will be the ESP-NOW receiver, the one on the left will be connected to the WiFi and receive data from the right hand EPS and transfer it over to MQTT or any other configured service.
The left ESP32 can also be connected to an optional external screen via the I2C connector and has a discrete RGB LED for status display.

Programming the two ESP32s can be done by connecting to the single USBC connector on the PCB which has the two USB data lines, USB1 and USB2 connected to each ESP32 respectively, this means that each ESP32 can be programmed seperately depending on the orientaion of the USB connector, there is an LED under each ESP32 to indicate which ESP32 is connected to the flasher, this uses the CC1/CC2 connections.  One drawback to this approach is that you must use a USB C to USB C connection cable which seperates the USB data connections, a USB A to C cable will not work because it shorts out the two USB busses. 
