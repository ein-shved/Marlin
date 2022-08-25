<p align="center"><img src="buildroot/share/pixmaps/logo/marlin-outrun-nf-500.png" height="250" alt="MarlinFirmware's logo" /></p>

<h1 align="center">Marlin 3D Printer Firmware</h1>

<p align="center">
    <a href="/LICENSE"><img alt="GPL-V3.0 License" src="https://img.shields.io/github/license/marlinfirmware/marlin.svg"></a>
    <a href="https://github.com/MarlinFirmware/Marlin/graphs/contributors"><img alt="Contributors" src="https://img.shields.io/github/contributors/marlinfirmware/marlin.svg"></a>
    <a href="https://github.com/MarlinFirmware/Marlin/releases"><img alt="Last Release Date" src="https://img.shields.io/github/release-date/MarlinFirmware/Marlin"></a>
    <a href="https://github.com/MarlinFirmware/Marlin/actions"><img alt="CI Status" src="https://github.com/MarlinFirmware/Marlin/actions/workflows/test-builds.yml/badge.svg"></a>
    <a href="https://github.com/sponsors/thinkyhead"><img alt="GitHub Sponsors" src="https://img.shields.io/github/sponsors/thinkyhead?color=db61a2"></a>
    <br />
    <a href="https://twitter.com/MarlinFirmware"><img alt="Follow MarlinFirmware on Twitter" src="https://img.shields.io/twitter/follow/MarlinFirmware?style=social&logo=twitter"></a>
</p>

Additional documentation can be found at the [Marlin Home Page](https://marlinfw.org/).
Please test this firmware and let us know if it misbehaves in any way. Volunteers are standing by!

## Two Trees SPRO

This is personal fork of Marlin to store configuration of own printer - Two
Trees Sapphire Pro with direct Big Tree Teck Matrix extruder (E3D Hemera clone).
See commit history for details.

### Specific filament calibrations

### E3Dv6 heatblock

##### PLA FDPlast

Parameter|Value
---------|-----
Max mass flow|12.3 mm3/s
Linear Advance K-Factor|0.0
Flow|95%
Temperature|215
Retraction|0.5mm
Bed Temperature|60/70

###### Flow Measurements

Length|Speed mm/min|Speed mm/s|Perc|Weight|Time
------|------------|----------|----|------|----
2000|240|4  |100%|5.9g|500s
2000|300|5  |125%|5.9g|400s
2000|312|5.2|130%|5.9g|384.6s
2000|336|5.6|140%|5.8g|357.1s
2000|360|6  |150%|5.8g|333.3s


##### PetG FDPlast

Parameter|Value
---------|-----
Max mass flow|15.12 mm3/s
Linear Advance K-Factor|0.0
Retraction|0.85mm
Flow|100%
Temperature|230
Bed Temperature|80/90

###### Flow Measurements

2362 mm3

Length|Speed mm/min|Speed mm/s|Perc|Time|Weight|Flow
------|------------|----------|----|----|------|----
1000|240|4  |100%|250.0s|3.00g|9.45
1000|300|5  |125%|200.0s|2.99g|11.81
1000|312|5.2|130%|192.3s|2.99g|12.28
1000|336|5.6|140%|178.6s|2.99g|13.22
1000|360|6  |150%|166.(6)s|2.98g|14.17
1000|384|6.4|160%|156.25s|2.97g|15.12


## Marlin 2.1

Marlin 2.1 continues to support both 32-bit ARM and 8-bit AVR boards while adding support for up to 9 coordinated axes and to up to 8 extruders.

Download earlier versions of Marlin on the [Releases page](https://github.com/MarlinFirmware/Marlin/releases).

## Example Configurations

Before building Marlin you'll need to configure it for your specific hardware. Your vendor should have already provided source code with configurations for the installed firmware, but if you ever decide to upgrade you'll need updated configuration files. Marlin users have contributed dozens of tested example configurations to get you started. Visit the [MarlinFirmware/Configurations](https://github.com/MarlinFirmware/Configurations) repository to find the right configuration for your hardware.

## Building Marlin 2.1

To build Marlin 2.1 you'll need [Arduino IDE 1.8.8 or newer](https://www.arduino.cc/en/main/software) or [PlatformIO](http://docs.platformio.org/en/latest/ide.html#platformio-ide). Detailed build and install instructions are posted at:

  - [Installing Marlin (Arduino)](http://marlinfw.org/docs/basics/install_arduino.html)
  - [Installing Marlin (VSCode)](http://marlinfw.org/docs/basics/install_platformio_vscode.html).

### Supported Platforms

  Platform|MCU|Example Boards
  --------|---|-------
  [Arduino AVR](https://www.arduino.cc/)|ATmega|RAMPS, Melzi, RAMBo
  [Teensy++ 2.0](https://www.microchip.com/en-us/product/AT90USB1286)|AT90USB1286|Printrboard
  [Arduino Due](https://www.arduino.cc/en/Guide/ArduinoDue)|SAM3X8E|RAMPS-FD, RADDS, RAMPS4DUE
  [ESP32](https://github.com/espressif/arduino-esp32)|ESP32|FYSETC E4, E4d@BOX, MRR
  [LPC1768](https://www.nxp.com/products/processors-and-microcontrollers/arm-microcontrollers/general-purpose-mcus/lpc1700-cortex-m3/512-kb-flash-64-kb-sram-ethernet-usb-lqfp100-package:LPC1768FBD100)|ARM® Cortex-M3|MKS SBASE, Re-ARM, Selena Compact
  [LPC1769](https://www.nxp.com/products/processors-and-microcontrollers/arm-microcontrollers/general-purpose-mcus/lpc1700-cortex-m3/512-kb-flash-64-kb-sram-ethernet-usb-lqfp100-package:LPC1769FBD100)|ARM® Cortex-M3|Smoothieboard, Azteeg X5 mini, TH3D EZBoard
  [STM32F103](https://www.st.com/en/microcontrollers-microprocessors/stm32f103.html)|ARM® Cortex-M3|Malyan M200, GTM32 Pro, MKS Robin, BTT SKR Mini
  [STM32F401](https://www.st.com/en/microcontrollers-microprocessors/stm32f401.html)|ARM® Cortex-M4|ARMED, Rumba32, SKR Pro, Lerdge, FYSETC S6
  [STM32F7x6](https://www.st.com/en/microcontrollers-microprocessors/stm32f7x6.html)|ARM® Cortex-M7|The Borg, RemRam V1
  [SAMD51P20A](https://www.adafruit.com/product/4064)|ARM® Cortex-M4|Adafruit Grand Central M4
  [Teensy 3.5](https://www.pjrc.com/store/teensy35.html)|ARM® Cortex-M4|
  [Teensy 3.6](https://www.pjrc.com/store/teensy36.html)|ARM® Cortex-M4|
  [Teensy 4.0](https://www.pjrc.com/store/teensy40.html)|ARM® Cortex-M7|
  [Teensy 4.1](https://www.pjrc.com/store/teensy41.html)|ARM® Cortex-M7|
  Linux Native|x86/ARM/etc.|Raspberry Pi

## Submitting Patches

- Submit **Bug Fixes** as Pull Requests to the ([bugfix-2.1.x](https://github.com/MarlinFirmware/Marlin/tree/bugfix-2.1.x)) branch.
- Follow the [Coding Standards](http://marlinfw.org/docs/development/coding_standards.html) to gain points with the maintainers.
- Please submit your questions and concerns to the [Issue Queue](https://github.com/MarlinFirmware/Marlin/issues).

## Marlin Support

The Issue Queue is reserved for Bug Reports and Feature Requests. To get help with configuration and troubleshooting, please use the following resources:

- [Marlin Documentation](https://marlinfw.org) - Official Marlin documentation
- [Marlin Discord](https://discord.gg/n5NJ59y) - Discuss issues with Marlin users and developers
- Facebook Group ["Marlin Firmware"](https://www.facebook.com/groups/1049718498464482/)
- RepRap.org [Marlin Forum](https://forums.reprap.org/list.php?415)
- Facebook Group ["Marlin Firmware for 3D Printers"](https://www.facebook.com/groups/3Dtechtalk/)
- [Marlin Configuration](https://www.youtube.com/results?search_query=marlin+configuration) on YouTube

## Contributors

Marlin is constantly improving thanks to a huge number of contributors from all over the world bringing their specialties and talents. Huge thanks are due to [all the contributors](https://github.com/MarlinFirmware/Marlin/graphs/contributors) who regularly patch up bugs, help direct traffic, and basically keep Marlin from falling apart. Marlin's continued existence would not be possible without them.

## Administration

Regular users can open and close their own issues, but only the administrators can do project-related things like add labels, merge changes, set milestones, and kick trolls. The current Marlin admin team consists of:

 - Scott Lahteine [[@thinkyhead](https://github.com/thinkyhead)] - USA - Project Maintainer &nbsp; [💸 Donate](https://www.thinkyhead.com/donate-to-marlin)
 - Roxanne Neufeld [[@Roxy-3D](https://github.com/Roxy-3D)] - USA
 - Keith Bennett [[@thisiskeithb](https://github.com/thisiskeithb)] - USA &nbsp; [💸 Donate](https://github.com/sponsors/thisiskeithb)
 - Peter Ellens [[@ellensp](https://github.com/ellensp)] - New Zealand
 - Victor Oliveira [[@rhapsodyv](https://github.com/rhapsodyv)] - Brazil
 - Chris Pepper [[@p3p](https://github.com/p3p)] - UK
 - Jason Smith [[@sjasonsmith](https://github.com/sjasonsmith)] - USA
 - Luu Lac [[@shitcreek](https://github.com/shitcreek)] - USA
 - Bob Kuhn [[@Bob-the-Kuhn](https://github.com/Bob-the-Kuhn)] - USA
 - Erik van der Zalm [[@ErikZalm](https://github.com/ErikZalm)] - Netherlands &nbsp; [💸 Donate](https://flattr.com/submit/auto?user_id=ErikZalm&url=https://github.com/MarlinFirmware/Marlin&title=Marlin&language=&tags=github&category=software)

## License

Marlin is published under the [GPL license](/LICENSE) because we believe in open development. The GPL comes with both rights and obligations. Whether you use Marlin firmware as the driver for your open or closed-source product, you must keep Marlin open, and you must provide your compatible Marlin source code to end users upon request. The most straightforward way to comply with the Marlin license is to make a fork of Marlin on Github, perform your modifications, and direct users to your modified fork.

While we can't prevent the use of this code in products (3D printers, CNC, etc.) that are closed source or crippled by a patent, we would prefer that you choose another firmware or, better yet, make your own.
