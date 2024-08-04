---
title: Guided Tour
weight: 1
url: "/docs/keyboard-featherwing/rev2/guided-tour"
---

Let's have a quick look at the FeatherWing and what's on it.

<div class="text-center">

[![Guiuded Tour](/docs/keyboard-featherwing/rev2/tour_small.png)](/docs/keyboard-featherwing/rev2/tour.png)

</div>


- **2.6" 320x240 16-bit color LCD with resistive touch screen** - The LCD driver (ILI9341) is interfaced over SPI, the touch driver (TSC2004) is interfaced over I2C.
- **QWERTY keyboard** - A BB Q10 keyboard connected to a SAMD20, the key FIFO can be easily accessed over I2C.
- **5-way button** - Great for navigating menus, also connected to the SAMD.
- **4 soft tactile buttons** - Feel very nice to press, use them for whatever function you want; also connected to the SAMD.
- **Neopixel** - Allows you to show the status of your board.
- **Ambient Light Sensor** - Connected to Analog pin 5, can be used to dim the backlight based on the ambient light levels.
- **microSD connector** - Gotta keep those photos and other files somewhere, am I right?
- **Stemma QT/Qwiic connector** - Opens the door to an ecosystem of dozens, if not hundreds, of Stemma QT/Qwiic boards.
- **On/Off switch** - Connected to the Feather Enable pin, turns off the Feather at LDO level (varies between Feathers), as well as 5V
- **GPIO expander** - The SAMD20 also doubles as a I2C GPIO expander, you can access the Touch INT, and Card Detect over the expander, also there are a few test points for extra GPIOs.
- **Dual row sockets** - Thanks to these, you can still access the Feather pins even when the Feather is plugged in!
- **Four mounting holes** - Use these for enclosures or to attach a lanyard.
- **GPIO solder jumpers** - Almost all GPIOs can be disconnected from the FeatherWing, just in case you have something else in mind for them.
