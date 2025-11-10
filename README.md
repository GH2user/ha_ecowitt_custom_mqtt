# ha_ecowitt_custom_mqtt
Home-Assistant files to use the custom MQTT server from Ecowitt


Based on the work done by @matthijsberg at https://github.com/matthijsberg/GW2000A-HA-MQTT/tree/main
Matthijs added all sensors for each device at the Gateway. My concept is seperating all devices while maintaining links to the Gateway and adding some features.


Supported Devices:
- GW2000A Gateway, firmware 3.2.5, 3.2.6
- WS90 Personal Weather Station
- WH30 Temp Sensor with probe
- WH31 Temp/Hum Sensor
- WH40 Rainfall Collector
- WH51 Soil Sensor (by @matthijsberg)
- WH57 Lightning Detector

It should be possible to use WH30 for all Temperature sensors and WH31 for all Temp/Hum sensors. The GW3000 gateway should also work as it generates the same MQTT-output according Ecowitt-discord.

Please refer to the wiki for more details on installation and usage.


At the MQTT integration page it will look like below image.





# NOTES
+ running the various ECOWITT integrations together:
  - you can run MQTT as a custom server simultainious with the OFFICIAL ECOWITT integration from HACS,
    ideal for experimenting and checking data for this project
  - HA-core integration is using a custom server and can NOT run together with MQTT as a custom server
  - HA-core integration can run together with the OFFCIAL ECOWITT integration from HACS

+ Home Assistant Packages are used for this project https://www.home-assistant.io/docs/configuration/packages/

+ Suggest to start getting the Gateway working before adding the devices

+ Refer to the wiki documents for installation guide and usage



If you have any other devices please leave a message with the output of the Diagnostic sensor 'raw data' from the Gateway. It should then be possible to add that one to the repository. You can also create a pull-request if you already added the device on your own fork.

Comments, additions are welcome.
