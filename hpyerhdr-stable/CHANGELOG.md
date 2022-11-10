# HyperHDR 18.0.0.0 Latest

# New features:
- Registering HyperHDR services with the MQTT broker
- System event support: hibernation/sleep/wake up/resume
- WLED Configuration Wizard can discover WLED devices on the network
- Added WLED auto-resume initialization and improved existing Philips Hue auto-resume feature
- Reworked network discovery service and added Windows support
- Frame Buffer software screen grabber (Linux)
- New config option to fix static flickering for DX11 grabber (#275)
- Improved Philips Hue wizard
- Protocol buffers HDR tone mapping (mainly for Android Screen Grabber #263)
- Replaced protobuf with a lightweight nanopb library
- Limit for software screen grabbers increased to 60FPS
- New software grabber for Linux: Wayland (pipewire/portal). Support for Ubuntu 22.04 LTS!
- Wayland grabber: support for pipewire/portal protocol version 4 persistent authentication
- New fully automatic LUT calibration for HDR/SDR/YUV
- New set of dedicated LUT tables for supported grabbers
- 30% improved performance for MJPEG HDR mode
- Add white channel calibration for RGBW led strips and latest HyperSerialEsp8266/HyperSerialESP32/HyperSPI (Adalight HyperSPI)
- New dynamic video cache buffers (improved performance, fixes #142)
- Performance information panel in the overview tab
- CPU performance and RAM usage (excluding Apple M1)
- CPU temperature reading (Linux only, when the sensor is present)
- Under-voltage detection (Raspberry Pi OS only)
- USB grabber performance (shows framerate and latency)
- Instance input images to LED colors performance
- LED device output performance
- New JSON API function to control USB grabber: brightness, contrast, saturation, hue
- USB grabber latency benchmark (link)
- HDR tone mapping for flatbuffers (PR #215 thanks @chbartsch)
- Dynamic LED layout resize on the container size changed
- Improved and refactored LED devices model and communication
- Flatbuffers: HDR tone mapping can use alternative filename: flat_lut_lin_tables.3d
- FlatBuffers: add support for high performance local sockets (link)
- The new build scheme allows graberless configuration and usage of external toolchains
- Add popular 'UDP raw' (WLED compatible) receiver for HyperHDR (link1 link2)

# Bug Fixing: 
- Fix variuos memory leaks reported by diagnostic tools
- Fix Philips Hue reconnection issues
- Synchronize interface to FlatBuffers HDR state when no USB grabbers are present in the build
- Fix for DirectX11 grabber secondary monitor capturing (fixes #223)
- Fix translations for parametrized items. Germany resources corrected (thanks @tuxuser)
- Fix for broken LED raw JSON editor (fixes #235)
- Fix looped communication in the remote tab
- Fix restart issue of X11 software screen grabber (fixes #167)
- Fix LED devices on/off race condition
- Fix saving Yeelight configuration (fixes #133)
- Fix inter-thread communication
- Fix saving changed Philips Hue configuration
- Fix LED devices state synchronization
- Fix invoking setting static color from the system menu
- Ignore Bluetooth devices during Adalight auto-discovery
- ProviderRestApi and ProviderUdpSSL are rewritten to fix variuos related issues
- ProviderUdpSSL (Philips Hue) ability to resume the connection when the communication stream is broken
- Fix for the undervoltage detection for newer Raspberry Pi OS

#Improvements:
- Migration from Pi-gen to CustomPiOS (Rpi SD images)
- Utilizing and migration to C++ smart pointers
- Move the flatbuffer server to separate thread
- Upgrade MBEDTLS to version 3.1
- Upgrade FlatBuffers to version 2.0.0
- Switch to mainline libjpegturbo 2.x
- Use prebuild protobuf compiler for Windows or the system library for other targets
- Updated rpi_ws281x library
- Windows and macOS releases are using QT6.2 LTS
- Windows: migrate the solution and documentation to Visual Studio 2022
- Removed: tinkerforge and USB-HID support
- Removed: LED device latch time