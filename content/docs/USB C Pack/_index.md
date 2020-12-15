---
title: "USB Type-C Plug SMT Pack"
weight: 7
no_list: true
---

If you ever wanted to add a USB Type-C Plug to your design, you probably realized that it's hard to find one that's easy to solder, can be routed on 2-layer PCBs, and doesn't put constraints on your PCB thickness. We're happy to report this connector checks all these boxes! You've probably seen this connector used in [our](https://www.tindie.com/products/arturo182/serpente-a-tiny-circuitpython-prototyping-board/) [other](https://www.tindie.com/products/arturo182/usb-type-c-plug-breakout-usb-20-only/) [products](https://www.tindie.com/products/arturo182/usb-type-c-plug-breakout-usb-30-only/).

Because there's only so many pins you can fit in one row, the connector does not break out all the USB Type-C pins, but there's enough for most DIY uses. You get the USB 2.0 data pins (D+ and D-), the CC and VCONN pins, as well as two SuperSpeed differential pairs (RX2+/- and TX2+/-). The SBU pins are not available.

As per the USB Type-C specification, the plug has only one pair of D+/D- pins; it's up to the Receptacle to connect them together or use a mux for more advanced scenarios. Similar with CC and VCONN pins.

The connectors are delivered on a 24mm tape.

For more details about USB Type-C, we recommend [this application note](http://ww1.microchip.com/downloads/en/appnotes/00001953a.pdf) or the [USB Type-C Specification](https://www.usb.org/sites/default/files/USB%20Type-C%20Spec%20R2.0%20-%20August%202019.pdf).

<div class="container">

[![Plugs](/docs/usb-c-pack/plugs.jpg)](/docs/usb-c-pack/plugs.jpg)

</div>

# Datasheet

[![Datasheet](/docs/usb-c-breakout/C-UTC009-0C-1.png)](/docs/usb-c-breakout/C-UTC009-0C.pdf)

# CAD Files
- [KiCad footprint](https://github.com/arturo182/kicad-modules/blob/master/Connector_USB_Extra.pretty/USB_C_Plug_UTC009-C12.kicad_mod)
- [3D .step model](https://github.com/arturo182/kicad-modules/blob/master/packages3D/Connector_USB.3dshapes/C-UTC009.step)
