waubesa
=======

> _**Note:**_ these flows use features introduced in Node-RED version 3.0, including wire junctions and dynamic links. They will not load correctly into earlier version of Node-RED.

Home automation for Philips Hue lights, Hunter-Douglas PowerView window shades etc.

### About

This flow implements more sophisticated time-based automation than is supported directly by either Apple HomeKit or the native apps supplied by "smart home" hardware.

For example, these flows activate different holiday-themed scenes automatically based on the date. They also can drive window shade automation based on the sun's position at a given location on a given date.

### Configuration

These flows rely on some sensitive configuration data provided via environment variables. The simplest, least secure way to define these is by adding them to a file the Node-RED runtime is configured to use (`~/.node-red/environment` by default).

| Environment Variable     | Description                                                             |
|--------------------------|-------------------------------------------------------------------------|
| LATITUDE                 | Coordinate for use with [suncalc](https://github.com/mourner/suncalc)   |
| LONGITUDE                | Coordinate for use with [suncalc](https://github.com/mourner/suncalc)   |
| GROUND_FLOOR_HUE_ADDRESS | IP address of the _Chez Nous Main_ bridge                               |
| GROUND_FLOOR_HUE_KEY     | API access token for the _Chez Nous Main_ bridge                        |
| GROUND_FLOOR_HUE_TOPIC   | Base MQTT topic for server-sent events from the _Chez Nous Main_ bridge |
| BASEMENT_HUE_ADDRESS     | IP address of the _Basement Hue_ bridge                                 |
| BASEMENT_HUE_KEY         | API access token for the _Basement Hue_ bridge                          |
| BASEMENT_HUE_TOPIC       | Base MQTT topic for server-sent events from the _Basement Hue_ bridge   |
| POWERVIEW_ADDRESS        | IP address of the PowerView hub                                         |
