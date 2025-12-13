# awesome-poe-smarthome
A list of smarthome devices designed to be PoE-first. In general, these are devices that work well (or at all) with Home Assistant. Due to that, I've included details on which integration allows the device to be added to HA. 

## Cameras
Cameras on PoE is very standard, so this list should only be cameras that include extra sensors.

| Camera | Extra Sensors | Integratioon |
|---|---|---|
| Unifi G4/G5/AI | Glass break and smoke detector noise sensors | Unifi Protect |
| Unifi Doorbell G4 | Package presence |

## Air Quality

| Device | Sensors | Integration |
|---|---|---|
| Awair Omni | Temp, Humidity, PM2.5, tVOC, Light, Noise | Awair; REST Sensors |
| Room Alert 3E | Temp, Humidity | SNMP |

## Presence

| Device | Sensors | Integration |
|---|---|---|
| Apollo R-Pro 1 | mmWave, light, LED light | ESPHome |
| Everything Presence Pro | mmWave, PIR | ESPHome |

## Lighting

| Device | Description | Integration |
|---|---|---|
| Unifi Floodlight | LED floodlight with flush mount. Integrated motion sensor. | Unifi Protect |

## Sirens/Speakers

| Device | Capabilities |
|---|---|---|
| Unifi PoE Siren | Siren | Unifi Protect |
| Unifi PoE Chime | Chime | Unifi Protect |
| Sonos Era 100 Pro | Media Player | Sonos |

## Weather / Outdoor Air Quality

| Device | Sensors | Integration |
|---|---|---|
| [AirVisual Outdoor](https://www.iqair.com/products/air-quality-monitors/airvisual-outdoor-2-pm) | AQI, PM1, PM2.5, PM10, temperature, relative humidity, barometric pressure, CO2 | AirVisual |

## Honorable Mentions
These are devices that work really well with PoE->USB adapters and can still be nicely wall-mounted. 

| Device | Description | Integration |
|---|---|---|
| [AirGradient ONE Indoor](https://www.airgradient.com/shop/#!/AirGradient-ONE-Indoor-Monitor-I-9PSL-Fully-Assembled-&-Tested/p/594725504) | USB-powered, but mounting bracket is sized for one- or two-gang box mounts, and looks visually good on the wall. | AirGradient |
