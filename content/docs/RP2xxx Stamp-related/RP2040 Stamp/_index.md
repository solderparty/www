---
title: "RP2040 Stamp"
weight: 1
no_list: true
url: "/docs/rp2040-stamp/"
---

The Stamp was created to allow you to use the **Raspberry Pi RP2040** in your designs without having to solder small-pitch QFN chips or worry about lots of external circuitry.

All you need to get you started is a 5V supply or a LiPo battery. The Stamp will take care of the charging and switching the power sources.

The castellated edges with **2mm pitch** can be hand-soldered directly to a Carrier board, used with pin headers for more flexibility, or connected without soldering using [FlexyPins](/docs/flexypin), which are spring connectors designed for modules with castellated edges. You can find footprints for many PCB programs [here](https://github.com/solderparty/rp2xxx_stamp_footprints).

At only **1 by 1 inch**, the Stamp packs a lot of features:
* **8MB of FLASH**
* **500mA 3.3V LDO**
* **All 30 GPIOs broken out**
* **A Neopixel**
* LiPo supply and charging circuit (with charging LED)
* USB broken out
* SWD broken out
* Reset Button
* 12MHz crystal

and of course, everything that comes with the Raspberry Pi RP2040 itself:
* Dual core ARM Cortex-M0+ @ 133MHz
* 264kB SRAM
* 2 UARTs
* 2 SPIs
* 2 I2Cs
* 16 PWM channels
* USB with Host and Device support

The RP2040 comes with a pre-programmed ROM UF2 Bootloader, by pulling the BOOTSEL pin low and resetting, or by double-pressing the RESET button (if the FW supports it), you can upload new firmware using the USB disk drive.

In addition to the Stamps we also offer a few reference designs, see the Carriers in the [Stamp-related category](/docs/rp2xxx-stamp-related) as well as our [Flux projects](/docs/flux).

The CircuitPython firmware for the Stamp comes with a built-in board files for the Carriers, for example you can access the RP2040 Stamp Carrier pins and interfaces by using `import stamp_carrier_board as board`. See [here](https://github.com/adafruit/circuitpython/tree/main/ports/raspberrypi/boards/solderparty_rp2040_stamp) for all the available Carrier board files.

{{% store_links lectronz="https://lectronz.com/products/rp2040-stamp" tindie="https://www.tindie.com/products/arturo182/rp2040-stamp/" %}}

<div class="text-center">

[![Front](/docs/rp2040-stamp/front_small.jpg)](/docs/rp2040-stamp/front.jpg)

</div>

<div class="col-4 mx-auto">

![Powered by Raspberry Pi](/powered-by-raspberry-pi.png)

</div>
