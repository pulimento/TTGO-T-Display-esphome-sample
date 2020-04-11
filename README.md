# TTGO T-Display sample

This sample uses TTGO ESP32 T-Display board [details here](https://github.com/Xinyuan-LilyGO/TTGO-T-Display), optionally powered by a battery, alongside with homeassistant. It shows some sensor data in the display.

Currently, it uses custom components from [musk95](https://github.com/musk95/esphome), but there is a [pull request in esphome project](https://github.com/esphome/esphome/pull/918) that adds support for this display. Neverthless, code in this repo will continue to work.

## Pinout

![Pin map](pinmap.jpg)

## Usage

- In the root folder, create a secrets.yaml file (in this case, for wifi credentials). Example file included
- Change ttg.yaml accordingly
- Install EspHome from command line
- Connect your device via USB
- Run: `esphome ttg.yaml run` (or compile, upload or whatever)
- Profit!

## Future ideas in mind

- Underclock ESP?