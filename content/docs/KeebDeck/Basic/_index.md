---
title: "KeebDeck Basic"
weight: 2
no_list: true
---

An affordable handheld QWERTY USB keyboard with a silicone keypad.

This is our first product using our KeebDeck Keyboard, meant to be a cost-effective way to demonstrate the capabilities of the Keyboard. It exposes the key presses as a **USB HID** over **USB Type-C**. The board also includes an unpopulated **Qwiic connector** footprint on the back, and test points with an I2C interface compatible with our previous BBQ10/BBQ20 boards.

By default, the board is running the **QMK** firmware, an alternative FW can be flashed to enable the I2C interface. With this firmware, you can use the same BBQ10/BBQ20 libraries to read the keyboard FIFO and reconfigure the chip over I2C:
- [Arduino library](https://github.com/solderparty/arduino_bbq10kbd)
- [CircuitPython library](https://github.com/solderparty/arturo182_CircuitPython_BBQ10Keyboard)

See the BBQ20KBD [Example Code](/docs/bbq20kbd/examples/) section for example code for these modules.

Since the board implements a standard USB HID keyboard interface, it can be used with desktop computers (**Windows/Linux/MacOS**), smartphones (**iOS/Android**), and SBCs (**Raspberry Pi**, etc).

The KeebDeck Basic is powered by the **STM32F042** microcontroller. The board itself uses two PCBs sandwiched together, keeping the KeebDeck Keyboard in place. Threaded SMD standoffs are soldered to the back cover, and Phillips-head screws are used to keep the front cover attached.

The board also features an unpopulated footprint for an **optional Boot button** on the back (not required for normal operation). Because of a small design bug, if the footprint is shorted by a finger when plugging in the USB cable, the device might boot into the bootloader. To counter this, nail polish has been applied on top of the Boot button footprint. Note that the boot button is not required to boot into the bootloader, all you have to do is hold the Esc button while plugging in the USB cable, and the QMK firmware will boot the microcontroller into the bootloader. However, if you do want a dedicated boot button, the nail polish has to be removed before soldering.


We have created a [3D-printable frame](https://www.printables.com/model/1393415-a-frame-for-the-keebdeck-basic) for the board. This optional frame gives the board a more rounded shape and acts as a good starting point for your own 3D designs for the KeebDeck Basic. **Make sure not to over-tighten the screws, as there's always a small risk of the threaded standoffs ripping off the back PCB.**

The board also features unpopulated footprints for LED backlight circuitry. You can solder the missing parts to **add a backlight** to the keyboard. See the [Downloads](/docs/keebdeck/basic/downloads) section for the hardware source files.


**Note: This board is not 5V-tolerant!**

{{% store_links lectronz="https://lectronz.com/products/keebdeck-basic" %}}

<div class="text-center">

[![KeebDeck Basic Front](/docs/keebdeck/basic/front.jpg)](/docs/keebdeck/basic/front.jpg)

</div>

<div class="text-center">

[![KeebDeck Basic Back](/docs/keebdeck/basic/back.jpg)](/docs/keebdeck/basic/back.jpg)

</div>

<div class="text-center">

[![KeebDeck Basic Dimensions](/docs/keebdeck/basic/dimensions.png)](/docs/keebdeck/basic/dimensions.png)

</div>

<div class="text-center">

[![KeebDeck Basic Exploded](/docs/keebdeck/keyboard/render.jpg)](/docs/keebdeck/keyboard/render.jpg)

</div>
