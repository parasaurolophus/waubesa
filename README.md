waubesa
=======

Integrate Hue lights and other home automation devices and services with HomeKit.

### About

This primarily exists to expose more of the Philips Hue Bridge API to Apple HomeKit than is directly supported by either the Philips or Apple mobile applications. For example, this allows starting a "dynamic scene" via a HomeKit automation, instead of only manually as is the case with the Hue application.

These flows also provide more sophisticated time-based automation than is supported natively by either Philips Hue or Apple Home. For example, these flows activate different holiday-themed scenes automatically based on the date. They also can drive window shade automation based on offsets from sunrise and sunset at a given location.

### Configuration

These flows rely on some sensitive configuration data provided via environment variables. The simplest, least secure way to define these is by adding them to a file the Node-RED runtime is configured to use; `~/.node-red/environment` by default.

| Environment Variable   | Description                                                             |
|------------------------|-------------------------------------------------------------------------|
| LATITUDE               | Coordinate for use with [suncalc](https://github.com/mourner/suncalc)   |
| LONGITUDE              | Coordinate for use with [suncalc](https://github.com/mourner/suncalc)   |
| CHEZ_NOUS_MAIN_ADDRESS | IP address of the _Chez Nous Main_ bridge                               |
| CHEZ_NOUS_MAIN_KEY     | API access token for the _Chez Nous Main_ bridge                        |
| CHEZ_NOUS_MAIN_TOPIC   | Base MQTT topic for server-sent events from the _Chez Nous Main_ bridge |
| BASEMENT_HUE_ADDRESS   | IP address of the _Basement Hue_ bridge                                 |
| BASEMENT_HUE_KEY       | API access token for the _Basement Hue_ bridge                          |
| BASEMENT_HUE_TOPIC     | Base MQTT topic for server-sent events from the _Basement Hue_ bridge   |
| POWERVIEW_ADDRESS      | IP address of the PowerView hub                                         |

