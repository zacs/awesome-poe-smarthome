# awesome-poe-smarthome <!-- omit in toc -->
A list of smarthome devices designed to be PoE-first. In general, these are devices that work well (or at all) with Home Assistant. Due to that, I've included details on which integration allows the device to be added to HA.

### Table of Contents
- [Cameras](#cameras)
- [Air Quality](#air-quality)
- [Presence](#presence)
- [Lighting](#lighting)
- [Covers](#covers)
- [Sirens/Speakers](#sirensspeakers)
- [Media Players](#media-players)
- [Weather / Outdoor Air Quality](#weather--outdoor-air-quality)
- [Displays](#displays)
- [Bluetooth Proxies / ESP32](#bluetooth-proxies--esp32)
- [Alarm Panels](#alarm-panels)
- [Hubs](#hubs)
- [RF Control](#rf-control)
- [Small Computers](#small-computers)
- [Honorable Mentions](#honorable-mentions)
  - [Mains-Powered, Ethernet-enabled](#mains-powered-ethernet-enabled)
  - [USB-Powered Hubs](#usb-powered-hubs)
  - [PoE → USB](#poe--usb)

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
| [Room Alert 3E](https://avtech.com/articles/4778/product-spotlight-room-alert-3e-for-temperature-and-environment-monitoring/) | Temp | [SNMP](https://www.home-assistant.io/integrations/snmp/) ([example config](/examples/room_alert_3e.yaml))|

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
| [Somfy PoE Shades](https://www.somfysystems.com/en-us/discover-somfy/power-technology/power-over-ethernet) | Possibly none with Home Assistant. |
| [Powershades TRUEPoE](https://powershades.com/truepoe) | Possibly none with Home Assistant. |

## Sirens/Speakers

| Device | Capabilities | Integration |
|---|---|---|
| [Unifi PoE Siren](https://store.ui.com/us/en/category/all-cameras-nvrs/collections/special-devices-sirens/products/up-siren-poe)[^1] | Siren | [Unifi Protect](https://www.home-assistant.io/integrations/unifiprotect/) |
| [Unifi PoE Chime](https://store.ui.com/us/en/category/cameras-doorbells/collections/pro-store-doorbells-chimes/products/uacc-chime-poe)[^1] | Chime | [Unifi Protect](https://www.home-assistant.io/integrations/unifiprotect/) |

[^1]: Requires a Unifi NVR or Dream Machine to function.

## Media Players

| Device | Integration |
| [Sonos Era 100 Pro](https://www.sonos.com/en-us/shop/era-100-pro) | [Sonos](https://www.home-assistant.io/integrations/sonos/) |
| [Unifi PoE Audio Port](https://store.ui.com/us/en/products/upl-port) | Airplay possibly? Can't find confirmation. |

## Weather / Outdoor Air Quality

| Device | Sensors | Integration |
|---|---|---|
| [AirVisual Outdoor](https://www.iqair.com/products/air-quality-monitors/airvisual-outdoor-2-pm) | AQI, PM1, PM2.5, PM10, temperature, relative humidity, barometric pressure, CO2 (optional) | [AirVisual](https://www.home-assistant.io/integrations/airvisual/) |

## Displays

| Device | Description |
|---|---|
| Philips 10BDL3051T/02 | PoE for data and power. VESA mountable. Only runs Android 8 |
| [Geekland Displays](https://geekland.co/product-category/wall-mount-touch-screen-tablets/) | Poe for data and power. VESA mountable. Android 13. |
| [Unifi Connect Display](https://store.ui.com/us/en/category/digital-signage/products/uc-display21) | 21" screen that can run Android apps. $700, and requires Unifi Connect software, which means you need a Dream Machine or Cloud Key. |

## Bluetooth Proxies / ESP32

| Device | Notes | Integration |
|---|---|---|
| [GL.iNet GL-S10](https://store.gl-inet.com/products/gl-s10-ble-iot-gateway) | [Custom flashing](https://devices.esphome.io/devices/gl-inet-gl-s10/) necessary. | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |
| [Olimex ESP32-POE](https://www.olimex.com/Products/IoT/ESP32/ESP32-POE/open-source-hardware) | Requires a case (3D printed). Available in multiple options including one with external antenna. | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |
| [M5stack with POE](https://shop.m5stack.com/products/esp32-ethernet-unit-with-poe) | Can add external sensors for temp, etc. | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |
| [Kincony E16P](https://devices.esphome.io/devices/kincony-e16p/) | 16 channel relay. Just one example, they make many sizes. | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |

## Alarm Panels

| Device | Notes | Integration |
|---|---|---|
| [Konnected Alarm Panel Pro](https://konnected.io/products/konnected-alarm-panel-pro-12-zone-interface-kit) | 12 zone replacement board for wired alarm systems | [ESPHome](https://www.home-assistant.io/integrations/esphome/) |

## Hubs

| Device | Protocols |
|---|---|
| [SMLight SLZB-06](https://smlight.tech/product/slzb-06) (and many other SMLight gateways) | Zigbee or Thread. Optionally Bluetooth Proxy |
| [SMLight SLZB-MR1U](https://smlight.tech/global/slzbmr1u) | Gateway that can off any USB hub over TCP/IP. For example, you could connect a Home Assitant ZWA-2 to it. |
| [TubesZB Z-Wave PoE Kit](https://tubeszb.com/product/z-wave-poe-kit/) | Z-wave. Requires a Zooz ZAC93 board. |
| [Aqara Hub G5 Pro PoE](https://www.aqara.com/en/product/camera-hub-g5-pro/) | Zigbee, Matter over Thread. Note: It is also a camera. |
| [Sonoff Dongle Max](https://sonoff.tech/products/sonoff-dongle-max-zigbee-thread-poe-dongle-dongle-m) | Zigbee or Thread |

## RF Control

| Device | Description |
|---|---|
| [Bond Bridge Pro](https://bondhome.io/product/bond-bridge-pro/) | Supports controlling fans, shades, and fireplaces. |

## Small Computers

| Device | Notes |
|---|---|
| [Thinlabs PoE NUC](https://thinlabs.com/products/poe-mini-pc/) | Seems like it isn't available for general purchase. |
| [Dell Wyse 3040](https://www.dell.com/support/manuals/en-us/wyse-3040-thin-client/3040_ug/system-specifications) | Thin client with a low enough power draw that it can be PoE-powered with an adapter that has a barrel splitter. Similar performance as a RPi4. |

## Honorable Mentions
These devices aren't PoE for various reasons, but fit the theme of avoiding either DC wall warts or wifi. Some need/control more power by definition but still use ethernet for data, and others may just be USB-powered devices that are [usually] convenient to power via a PoE->USB converter (but still use wifi for their data).

### Mains-Powered, Ethernet-enabled

| Device | Description |
|---|---|
| [Yardian Pro Smart Sprinkler Controller](https://www.yardian.com/products/yardian-pro-smart-sprinkler-controller/) | Smart irrigation controller with built-in ethernet. Ac power required to manage the sprinkler solenoids, but a nice non-wifi solution. |
| [Wattboxes](https://www.snapav.com/shop/en/snapav/wattbox) | Ethernet-controlled power strips/distribution. Expensive new, but can be extremely cheap on eBay. Generally used on higher-end smarthome with Control4, Crestron, etc. Three-outlet version are usually ~$30, and rack mountable 8/16 plug units for ~$100. Supported via a custom component in HA. |
| [Unifi PDU Pro](https://store.ui.com/us/en/category/integrations-power-tech/collections/unifi-power-tech-power-distribution/products/usp-pdu-pro)[^1] | Another ethernet-enabled 2U rack-mount power distribution unit. Expensive, if you aren't in the Unifi ecosystem already. |

[^1]: Requires a Unifi NVR or Dream Machine to function.

### USB-Powered Hubs

The following hubs are nicely-equipped with USB power ports that are easily powered using PoE splitters ([example](https://www.amazon.com/UCTRONICS-PoE-Splitter-USB-C-Compliant/dp/B087F4QCTR/)). They use ethernet for data as well, so thie hit the power+data requirement in a roundabout way. 

_This list is nowhere near exhaustive. Please feel free to add others in a PR._

1. Lutron Caseta Hub
2. Philips Hue Hub
3. Hubitat
4. Home Assistant Green

### PoE → USB

Okay, these are just USB devices. But they are ones that are very well-suited for a converter because of their physical design, as described below. 

| Device | Why is it on this list? |
|---|---|
| [AirGradient One](https://www.airgradient.com/shop/#!/AirGradient-ONE-Indoor-Monitor-I-9PSL-Fully-Assembled-&-Tested/p/594725504) | It's mounting bracket is sized to fit right over a traditional one-gane box, and the USB cable is routed so that it would be completely invisible if it were wall-mounted. |
| [Ring Alarm Keypad Gen2](https://www.amazon.com/Ring-Alarm-Keypad/dp/B07ZB2DFMB) | Yes, it is a z-wave device! But it is wall-mounted and PoE lets you never worry about recharging it. It's USB cable is routed so that it can be totally hidden. Mounts over a one- or two-gang box with a [3D-printed faceplate](https://www.amazon.com/Wall-Electrical-Mount-Alarm-Keypad/dp/B0CS1M8LJW). |
