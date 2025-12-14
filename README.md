# awesome-poe-smarthome <!-- omit in toc -->
A list of smarthome devices designed to be PoE-first. In general, these are devices that work well (or at all) with Home Assistant. Due to that, I've included details on which integration allows the device to be added to HA.

### Table of Contents
- [Cameras](#cameras)
- [Air Quality](#air-quality)
- [Presence](#presence)
- [Lighting](#lighting)
- [Covers](#covers)
- [Sirens/Speakers](#sirensspeakers)
- [Weather / Outdoor Air Quality](#weather--outdoor-air-quality)
- [Displays](#displays)
- [Bluetooth Proxies / ESP32](#bluetooth-proxies--esp32)
- [Alarm Panels](#alarm-panels)
- [Hubs](#hubs)

## Cameras
Cameras on PoE is very standard, so this list should only be cameras that include extra sensors. _Note that the Unifi cameras require an NVR or Dream Machine to operate._

| Devices | Extra Sensors | Integratioon |
|---|---|---|
| [Unifi G4/G5/G6/AI](https://store.ui.com/us/en/category/all-cameras-nvrs)[^1] | Motion, glass break and smoke detector noise sensors | [Unifi Protect](https://www.home-assistant.io/integrations/unifiprotect/) |
| [Unifi Doorbell G4](https://store.ui.com/us/en/category/cameras-doorbells)[^1] | Motion, package presence | [Unifi Protect](https://www.home-assistant.io/integrations/unifiprotect/) |
| [Instar POE Cameras](https://www.instar.com/en_US/compare-all-poe-surveillance-cameras-for-indoors-and-outdoors) | Motion, AI-based human/vehicle/animal detection | MQTT |
| [Reolink](https://store.reolink.com/jp/poe-ip-cameras/) | Motion, Person/vehicle/pet detectoin. Optional: Spotlight, Siren | [Reolink](https://www.home-assistant.io/integrations/reolink/) |

[^1]: Requires a Unifi NVR or Dream Machine to function.

## Air Quality

| Device | Sensors | Integration |
|---|---|---|
| [Awair Omni](https://www.getawair.com/products/omni) | Temp, Humidity, PM2.5, tVOC, CO2, Light, Noise | [Awair](https://www.home-assistant.io/integrations/awair/); [REST Sensors](https://www.home-assistant.io/integrations/rest/) |
| [Room Alert 3E](https://avtech.com/articles/4778/product-spotlight-room-alert-3e-for-temperature-and-environment-monitoring/) | Temp, Humidity | [SNMP](https://www.home-assistant.io/integrations/snmp/) ([example config](/examples/room_alert_3e.yaml))|

## Presence

| Device | Sensors | Integration |
|---|---|---|
| [Apollo R-Pro 1](https://apolloautomation.com/products/r-pro-1) | mmWave (LD2450), UV, temp, humidity, light, LED light. Optional: second mmWave (LD2412), CO2 | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |
| [Everything Presence Pro](https://shop.everythingsmart.io/en-us/products/everything-presence-pro) | Dual mmWave, PIR, light, temp/humidity/CO2 (optional module), LED light | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |
| [Sensy-One E1](https://sensy-one.com/products/sensy-one-e1-white) | mmWave (LD2450) | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |
| [CeilSense](https://smarthomeshop.io/en/products/ceilsense) | mmWave (LD2412S), lux, LED light. Optional: temp, humidity, CO2) | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |

## Lighting

| Device | Description | Integration |
|---|---|---|
| [Unifi Floodlight](https://store.ui.com/us/en/category/cameras-special-devices/products/up-floodlight)[^1] | LED floodlight with flush mount. Integrated motion sensor. | [Unifi Protect](https://www.home-assistant.io/integrations/unifiprotect/) |

[^1]: Requires a Unifi NVR or Dream Machine to function.

## Covers

| Device | Integration |
|---|---|
| [Smartwings PoE Matter Over Ethernet Blinds](https://www.smartwingshome.com/pages/the-worlds-first-poe-matter-over-ethernet-motor) | Matter |

## Sirens/Speakers

| Device | Capabilities | Integration |
|---|---|---|
| [Unifi PoE Siren](https://store.ui.com/us/en/category/all-cameras-nvrs/collections/special-devices-sirens/products/up-siren-poe)[^1] | Siren | [Unifi Protect](https://www.home-assistant.io/integrations/unifiprotect/) |
| [Unifi PoE Chime](https://store.ui.com/us/en/category/cameras-doorbells/collections/pro-store-doorbells-chimes/products/uacc-chime-poe)[^1] | Chime | [Unifi Protect](https://www.home-assistant.io/integrations/unifiprotect/) |

[^1]: Requires a Unifi NVR or Dream Machine to function.
| [Sonos Era 100 Pro](https://www.sonos.com/en-us/shop/era-100-pro) | Media Player | [Sonos](https://www.home-assistant.io/integrations/sonos/) |

## Weather / Outdoor Air Quality

| Device | Sensors | Integration |
|---|---|---|
| [AirVisual Outdoor](https://www.iqair.com/products/air-quality-monitors/airvisual-outdoor-2-pm) | AQI, PM1, PM2.5, PM10, temperature, relative humidity, barometric pressure, CO2 (optional) | [AirVisual](https://www.home-assistant.io/integrations/airvisual/) |

## Displays

| Device | Description |
|---|---|
| Philips 10BDL3051T/02 | PoE for data and power. VESA mountable. Only runs Android 8 |
| [Geekland Displays](https://geekland.co/product-category/wall-mount-touch-screen-tablets/) | Poe for data and power. VESA mountable. Android 13. |


## Bluetooth Proxies / ESP32

| Device | Notes | Integration |
|---|---|---|
| [GL.iNet GL-S10](https://store.gl-inet.com/products/gl-s10-ble-iot-gateway) | [Custom flashing](https://devices.esphome.io/devices/gl-inet-gl-s10/) necessary. | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |
| [Olimex ESP32-POE](https://www.olimex.com/Products/IoT/ESP32/ESP32-POE/open-source-hardware) | Requires a case (3D printed). Available in multiple options including one with external antenna. | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |
| [M5stack with POE](https://shop.m5stack.com/products/esp32-ethernet-unit-with-poe) | Can add external sensors for temp, etc. | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |
| [Kincony E16P](https://devices.esphome.io/devices/kincony-e16p/) | 16 channel relay | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |

## Alarm Panels

| Device | Notes | Integration |
|---|---|---|
| [Konnected Alarm Panel Pro](https://konnected.io/products/konnected-alarm-panel-pro-12-zone-interface-kit) | 12 zone replacement board for wired alarm systems | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |

## Hubs

| Device | Protocols |
|---|---|
| [SMLight SLZB-06](https://smlight.tech/product/slzb-06) | Zigbee or Thread. Optionally Bluetooth Proxy |
| [TubesZB Z-Wave PoE Kit](https://tubeszb.com/product/z-wave-poe-kit/) | Z-wave. Requires a Zooz ZAC93 board. |