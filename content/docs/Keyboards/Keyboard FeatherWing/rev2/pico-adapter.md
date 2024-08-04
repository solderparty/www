---
title: Raspberry Pi Pico Adapter
weight: 4
url: "/docs/keyboard-featherwing/rev2/pico-adapter"
---

This adapter was designed specifically to allow driving the Keyboard FeatherWing with a Raspberry Pi Pico board.

{{% alert title="Note" %}}
Because the Pico only has 3 analog pins, only A0, A1, and A5 of the Keyboard FeatherWing can actually be used to read analog values.
{{% /alert %}}

{{% alert title="Warning" color="warning" %}}
This revision of the adapter has a small HW bug where the two BAT header pins are not connected together. The pins are not used by the Pico, so they don't affect any functionality, however, if you want to use the BAT pin with the Keyboard FeatherWing plugged in, you have to short the two pins together with a piece of wire or a solder blob.
{{% /alert %}}

<div class="text-center">

[![RPi Pico Adapter](/docs/keyboard-featherwing/rev2/pico_adapter_small.jpg)](/docs/keyboard-featherwing/rev2/pico_adapter.jpg)

</div>

## Hardware

Solder the Pico either directly to the Adapter board using the SMD pads, or using pin header footprint.

For a less bulky experience, we recommend soldering the pin headers that connect to the FeatherWing in such a way that the plastic part is on the same side as the Pico. See the picture above for clarification.

The KiCad hardware source files for the board can be found on [Github](https://github.com/solderparty/keyboard_featherwing_pico_adapter).

## Software

If you are using CircuitPython, we prepared [a board file](https://github.com/solderparty/keyboard_featherwing_sw/blob/main/circuitpython/kfw_pico_board.py) which you can import using `import kfw_pico_board as board`. The file allows you to access Pico's pins and peripherals as if you were using a Feather board (`board.D1` etc.).

## Schematics

<div class="text-center">

[![Drawing](/docs/keyboard-featherwing/rev2/schematics_pico_adapter.png)](/docs/keyboard-featherwing/rev2/schematics_pico_adapter.png)

</div>


## Drawing

<div class="text-center">

[![Drawing](/docs/keyboard-featherwing/rev2/drawing_pico_adapter.png)](/docs/keyboard-featherwing/rev2/drawing_pico_adapter.png)

</div>
