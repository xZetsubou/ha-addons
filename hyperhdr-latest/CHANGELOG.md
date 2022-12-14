# HyperHDR 19.0.0.0beta2 Latest

- # New features:
- HyperHDR got new packages repository (Github Pages). More details: https://awawa-dev.github.io/ Also RPM packages are available there and Arch Linux installers are planned.
- The SD images that come with this release are already linked to the HyperHDR repository, so a future update should be much simpler.
- Add support for ESP32-S2 mini board. It requires latest HyperSerialESP32 v8 firmware https://github.com/awawa-dev/HyperSerialESP32/releases/tag/v8.0.0.0 . This firmware brings also support for multi-segments, that allows to double the refresh rate of large sk6812/ws2812b setups for free (well, at least a proper LED strip design is required)
- ESP8266/ESP32 handshake for the AWA Adalight (#432)
- Save/restore WLED state and set max brightness at startup (#353)
- Add support for utv007 / Linux (#423)


# Improvements:
- Improved LED device performance (dropping frames that have exceeded the hardware capabilities of the LED device, UDP/SPI devices are not affected as the process is handled by the OS)
- Update de.json (#411) Thanks @Duese123
- Update Github actions/upload@v3 (#373)

# Fixed Bugs:
- Automatic signal detection timing (#410)
- Fix the black color for disabled LEDs (#419)


# More Info:
https://github.com/awawa-dev/HyperHDR/discussions/458
