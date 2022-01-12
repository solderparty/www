---
title: "Firmware"
weight: 1
no_list: true
---

## Arduino
You can also use the Arduino IDE with the RP2040 Stamp by using [Earle Philhower's Arduino core](https://github.com/earlephilhower/arduino-pico). Follow the instructions in the README file. After installation, the Stamp will be listed as a board in the IDE.

## CircuitPython
The Stamp comes pre-flashed with [CircuitPython](https://circuitpython.org), you can download the pre-built firmware from [the official website](https://circuitpython.org/board/solderparty_rp2040_stamp/) and you can find the source code [on github](https://github.com/adafruit/circuitpython/tree/main/ports/raspberrypi/boards/solderparty_rp2040_stamp).

## Pico-SDK
A pull request to the official [Raspberry Pi RP2040 SDK](https://github.com/raspberrypi/pico-sdk) is on [review right](https://github.com/raspberrypi/pico-sdk/pull/696) now, in the meanwhile you can use [our branch](https://github.com/solderparty/pico-sdk/tree/rp2040-stamp) to use the Stamp with the SDK.

## Rust
The [RP HAL](https://github.com/rp-rs/rp-hal) for Rust Embedded has [board files](https://github.com/rp-rs/rp-hal/tree/main/boards/solderparty-rp2040-stamp) for the Stamp. There's also an example on using the Stamp's Neopixel. Thank you to [Johan Kristell](https://github.com/jkristell) for this contribution.

## Others
Have you ported the RP2040 Stamp to another language/framework/library? Let us know and we'll gladly add it here!