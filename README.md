# Riden RD6006 controller via ESPHome

This device allows you to control a Riden RD6006 Power Supply via [Home Assistant](https://www.home-assistant.io/). It uses [ESPHome](https://esphome.io/) to abstract modbus commands and expose them to Home Assistant and makes it super easy to interface with your device over WiFi.

It is a replacement for the (frankly terrible) software running on the Riden WiFi module and intended as a replacement for their mobile apps and Windows software.

## Credits
This repo was based on a Python project by [Baldanos](https://github.com/Baldanos/rd6006).

## What you'll need:
- A [Riden RD6006](https://rdtech.aliexpress.com/store/923042) power supply with WiFi module
- An [FTDI adapter](https://www.aliexpress.com/item/32273550144.html)
- A [Home Assistant](https://www.home-assistant.io/) installation [with ESPHome](https://esphome.io/guides/getting_started_hassio.html)

## How to:
- Flash your RD6006 with the [UniSoft firmware](https://github.com/wildekek/riden-firmware-unisoft)
- Create a new ESPHome device and load this [configuration](/rd6006-controller.yaml)
- Update your WiFi credentials in ESPHome
- [Flash the Riden WiFi module with ESPHome](https://esphome.io/guides/physical_device_connection.html)
- Set the right settings in the Riden power supply:
	- UART Interface to "TTL+EN"
	- UART Baudrate to "115200"
	- Address to "1"
	- Skip keys lock to "ON"

## Features
<img width="825" alt="image" src="https://github.com/wildekek/rd6006-controller/assets/2332647/e5a712ff-85f0-40c0-9eed-f98f387a32b2">
