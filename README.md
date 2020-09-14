# Homey App Issues
If you have any issues with the Homey app, put them in the [issues](https://github.com/Homey-Eurotronic/homey-issues/issues) tab.

Please state your:  
Homey Version:  
Homey Mobile App Version:  
Eurotronic App Version:  
Your Issue Description:

## Supported Devices:
+ Stella Z-Wave
+ Comet Z-Wave
+ Spirit Z-Wave
+ Spirit (Aeotec Boxed) Z-Wave
+ Air Quality Sensor
+ Temperature/Humidity Sensor

### Device Functions Stella/Comet:
+ Read target temperature (not the manual set temperature) (°C)
+ Read last measured temperature (not trigger-able) (°C)
+ On every Wake-Up:
  - Read measured temperature (trigger-able) (°C)
  - Set target temperature (°C)
  - Read/Set modes (Off, Comfortable, Economic, Manual)
  - Set economy target temperature (Setting/flow) (°C)
+ Set manual valve position

### Device Functions Spirit (/Aeotec Boxed):
+ Read/Set target temperature (°C)
+ Read/Set measured (room) temperature (set = flow and/or direct association only) (°C)
+ Read/Set modes (Off, Comfortable, Economic, Boost, Manual)
+ Set economy target temperature (setting/flow) (°C)
+ Read/Set (child) protection
+ Set manual valve position
+ Error occurred (flow only)

### Device Functions Air Quality Sensor:
+ Read air quality
+ Read measured VOC level (ppm)
+ Read measured CO2 level (ppm)
+ Read measured temperature (°C)
+ Read calculated dewpoint temperature (°C)
+ Read measure humidity level (%)

### Device Functions Temperature/Humidity Sensor:
+ Read measured temperature (°C)
+ Read calculated dewpoint temperature (°C)
+ Read measure humidity level (%)

### Notes
**Stella/Comet:**
**The temperature and mode(s) will only be SET when the device Wakes Up.**
Wake-Up is by default set to 1 hour (3600 seconds) on homey.  
If you want to change the Wake-Up Interval, make sure you use Steps of 240 seconds.

### Supported Languages:
* English
* Dutch (Nederlands)
* German (Deutsch)

### Change Log:
**v2.3.0:**
- Add support Air Quality Sensor
- Add support Temperature/Humidity Sensor
- Add German translation

**v2.2.0:**
- Official app transfer to Eurotronic Technology GmbH
- Fix Protection status not synchronizing of the Spirit valve
- Add support for the Aeotec Limited boxed Spirit valve
- Update Meshdriver to 1.3.24

**v2.1.0:**
- Add battery types for Homey v3's Energy

**v2.0.7:**
- [Spirit] Fix device's measured temperature overwriting the external temperature sensor (when used).
- Update meshdriver to v1.3.3

**v2.0.6:**
- [Comet] Fix crash

**v2.0.5:**
- [Stella] Fix crash
- [Spirit] (Re)set measured temperature on change of external temperature setting
- Add insights for manual value

**v2.0.4:**
- Fix the wrong device (last included) being the device always controlled from flows

**v2.0.3:**
- [Spirit] Fix not being able to send the room temperature
- Added a setting for the Economic temperature

**v2.0.2:**
- Fix rounding errors manual control
- Rewritten internal functions making the app more stable (in particular with multiple devices)
- Fixed `$deg;C` special character which didn't work, to normal `°C`

**v2.0.1:**
- [Spirit] Fix external temperature setting not set-able
- Fix set eco temperature flow card
- Update Meshdriver to v1.2.30
- Fix whitespacing

**v2.0.0:**
- Rewrite to SDKv2
- Update Meshdriver to v1.2.28

**v1.2.1:**
- [Spirit] Fix default temperature reporting, normal default is too high.
- [Spirit]: Fix a few text errors.
- [Spirit]: Added id's for (future) firmware updates of the spirit.

**v1.2.0:**
- Add support Spirit Z-Wave
- Fixed temperature ranges of Stella and Comet thermostatic
- Fixed "manual position" value not being inserted in the global token
- Update Z-Wave driver to 1.1.9

**v1.1.3:**
- Fix set economic temperature bug.

**v1.1.1 & 1.1.2:**
- Minor fixes

**v1.1.0:**
- Add support for manual position control (re-pair needed for full support)
- Update Z-Wave driver to 1.1.8
- A lot of code improvements

**v1.0.0:**  
- Added support Stella Z-Wave
- [Comet] Update mode support
- [Comet] Updated Read me
- [Comet] Changed error logging
