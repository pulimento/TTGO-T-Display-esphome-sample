# TTGO T-Display sample

This sample uses [TTGO ESP32 T-Display board](https://github.com/Xinyuan-LilyGO/TTGO-T-Display), optionally powered by a battery, with [ESPHome](https://esphome.io/), alongside with [Home Assistant](https://www.home-assistant.io/)

This sample features:
- The built-in OLED display (showing some sensors data)
- GPIO buttons
- Li-Po battery charge data
- R/W communication with HomeAssistant

~~Currently, it uses custom components from [musk95](https://github.com/musk95/esphome), but there is a [pull request in esphome project](https://github.com/esphome/esphome/pull/918) that adds support for this display. Neverthless, code in this repo will continue to work.~~

Initially, it used a custom component for the display. As of today (mid 2021), ESPHome has native support for this screen, so no custom component required.



## Pinout

![Pin map](pinmap.jpg)

## Usage

Make sure you have ESPHome CLI installed previously. If not, [here are the instructions](https://esphome.io/guides/getting_started_command_line.html)

- In the root folder, create a secrets.yaml file (in this case, for wifi credentials). Example file included
- Change ttg.yaml accordingly
- Connect your device via USB (if powered by a battery, OTA flashing is possible, thus USB is not needed)
- Run: `esphome ttg.yaml run` (or compile, upload or whatever)
- Profit!

## Future ideas in mind

- Underclock ESP? Possible from C++. ESP32.cpp, ESP.getCpuFreqMHz(). Could also be set.
- Power off screen (viewing [this PR](https://github.com/esphome/esphome/pull/918/files), it would be possible to digitally disable the backlight
- Pages (I've started trying it, in ttg-pages.yaml)
- Report battery correctly when charging