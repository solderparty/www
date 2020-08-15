---
title: Guided Tour
weight: 1
---

Let's have a quick look at the FeatherWing and what's on it.

<div class="container">

[![Guiuded Tour](/docs/keyboard-featherwing/tour_small.png)](/docs/keyboard-featherwing/tour.png)

</div>


- **2.6" 320x240 16-bit color LCD with resistive touch screen** - Both the LCD and the touch display are interfaced over SPI, the LCD is driven by ILI9341 and the touch is interfaced with the STMPE811.
- **QWERTY keyboard** - A BB Q10 keyboard connected to a SAMD20, the key FIFO can be easily accessed over I2C.
- **5-way button** - Great for navigating menus, also connected to the SAMD.
- **4 soft tactile buttons** - Feel very nice to press, use them for whatever function you want; also connected to the SAMD.
- **Neopixel** - Allows you to show the status of your board.
- **microSD connector** - Gotta keep those photos and other files somewhere, am I right?
- **Stemma QT/Qwiic connector** - Opens the door to an ecosystem of dozens, if not hundreds, of Stemma QT/Qwiic boards.
- **On/Off switch** - Connected to the Feather Enable pin, turns off the Feather at LDO level (varies between Feathers).
- **GPIO expander** - The touch driver also doubles as a GPIO expander for some of the less-used pins.
- **Dual row sockets** - Thanks to these, you can still access the Feather pins even when the Feather is plugged in!
- **Four mounting holes** - Use these for enclosures or to attach a lanyard.
- **GPIO solder jumpers** - Almost all GPIOs can be disconnected from the FeatherWing, just in case you have something else in mind for them.
