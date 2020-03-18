# MQTT wake on lan

## What does this do?
This is a simple python script executed in a docker container, that can be configured to 
[start local devices over the network](https://en.wikipedia.org/wiki/Wake-on-LAN).

## Configuration
The connection to the MQTT broker can be configured by setting environment variables for the docker container,
a template [.env](.env.template) file is provided.
The devices to start are configured in [devices.yaml](devices.yaml). 
This includes the topic to listen on, the message to wait for and the MAC address of the remote device. 

The base for this specific script was a generic script to run commands for messages on MQTT topics, 
thus the structure of the configuration file.

## Related projects:
- [MQTT device controller](https://github.com/lunarys/mqtt-device-controller) for autonomously controlling remote devices
- [MQTT device status](https://github.com/lunarys/mqtt-device-status) for also receiving the status of the device via MQTT 