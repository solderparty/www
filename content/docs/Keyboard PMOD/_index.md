---
title: "Keyboard PMOD"
weight: 2
---

A BB Q10 Keyboard in PMOD format!

The board uses a ATSAMD20 chip to poll the keyboard and put key press information into a FIFO. A I2C interface can be used to read the FIFO, configure some of the functionality of the chip, and control the keyboard backlight. The key information can be received using polling or interrupts.

The firmware for the chip, as well as the protocol, can be found [here](https://github.com/arturo182/bbq10kbd_i2c_sw).

More information about the keyboard itself can be found [here](https://github.com/arturo182/bbq10kbd).

<div class="container">

[![Keyboard PMOD](/docs/keyboard-pmod/perspective.jpg)](/docs/keyboard-pmod/perspective.jpg)

</div>
