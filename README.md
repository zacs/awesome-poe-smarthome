# awesome-poe-smarthome
A list of smarthome devices designed to be PoE-first. In general, these are devices that work well (or at all) with Home Assistant. Due to that, I've included details on which integration allows the device to be added to HA. 

## Cameras
Cameras on PoE is very standard, so this list should only be cameras that include extra sensors.

| Devices | Extra Sensors | Integratioon |
|---|---|---|
| [Unifi G4/G5/AI](https://www.ui.com/camera-security) | Motion, glass break and smoke detector noise sensors | [Unifi Protect](https://www.home-assistant.io/integrations/unifiprotect/) |
| [Unifi Doorbell G4](https://store.ui.com/us/en/collections/unifi-protect-cameras/products/uvc-g4-doorbell) | Motion, package presence | [Unifi Protect](https://www.home-assistant.io/integrations/unifiprotect/) |

## Air Quality

| Device | Sensors | Integration |
|---|---|---|
| [Awair Omni](https://www.getawair.com/products/omni) | Temp, Humidity, PM2.5, tVOC, CO2, Light, Noise | [Awair](https://www.home-assistant.io/integrations/awair/); [REST Sensors](https://www.home-assistant.io/integrations/rest/) |
| [Room Alert 3E](https://avtech.com/products/room-alert-3e/) | Temp, Humidity | [SNMP](https://www.home-assistant.io/integrations/snmp/) ([example config](/examples/room_alert_3e.yaml))|

## Presence

| Device | Sensors | Integration |
|---|---|---|
| [Apollo R-Pro 1](https://www.apolloautomation.com/collections/all/products/apollo-automation-rp1-everything-smart-home-you-need-in-one-room) | mmWave, Dual mmWave (optional), temp, humidity, light, LED light | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |
| [Everything Presence Pro](https://shop.everythingsmart.io/en-us/products/everything-presence-pro) | Dual mmWave, PIR, light, temp/humidity/CO2 (optional module), LED light | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |

## Lighting

| Device | Description | Integration |
|---|---|---|
| [Unifi Floodlight](https://store.ui.com/us/en/collections/unifi-protect-cameras/products/up-floodlight) | LED floodlight with flush mount. Integrated motion sensor. | [Unifi Protect](https://www.home-assistant.io/integrations/unifiprotect/) |

## Sirens/Speakers

| Device | Capabilities | Integration |
|---|---|---|
| [Unifi PoE Siren](https://store.ui.com/us/en/collections/unifi-access/products/ua-siren) | Siren | [Unifi Protect](https://www.home-assistant.io/integrations/unifiprotect/) |
| [Unifi PoE Chime](https://store.ui.com/us/en/collections/unifi-access/products/ua-chime) | Chime | [Unifi Protect](https://www.home-assistant.io/integrations/unifiprotect/) |
| [Sonos Era 100 Pro](https://www.sonos.com/en-us/shop/era-100-pro) | Media Player | [Sonos](https://www.home-assistant.io/integrations/sonos/) |

## Weather / Outdoor Air Quality

| Device | Sensors | Integration |
|---|---|---|
| [AirVisual Outdoor](https://www.iqair.com/products/air-quality-monitors/airvisual-outdoor-2-pm) | AQI, PM1, PM2.5, PM10, temperature, relative humidity, barometric pressure, CO2 (optional) | [AirVisual](https://www.home-assistant.io/integrations/airvisual/) |

## Honorable Mentions
These are devices that work really well with PoE->USB adapters and can still be nicely wall-mounted. 

| Device | Description | Integration |
|---|---|---|
| [AirGradient ONE Indoor](https://www.airgradient.com/shop/#!/AirGradient-ONE-Indoor-Monitor-I-9PSL-Fully-Assembled-&-Tested/p/594725504) | USB-powered, but mounting bracket is sized for one- or two-gang box mounts, and looks visually good on the wall. | [AirGradient](https://www.home-assistant.io/integrations/airgradient/) |
