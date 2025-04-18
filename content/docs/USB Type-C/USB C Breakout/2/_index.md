---
title: "USB 2.0"
weight: 1
url: "/docs/usb-c-breakout/2"
---

This breakout board provides an easy way to extract signals and power from a USB Type-C Receptacle. By default, the CC pin is connected via a 5.1K resistor to GND (-), meaning the plug identifies as a downstream port, and the upstream port will provide up to 1.5A at 5V. You can replace or move the resistor to pull the CC pin to VBUS (+) or change the pull value.

The 2.0 variant of the breakout board skips the SuperSpeed pins; they are left floating.

As per the USB Type-C specification, the plug has only one pair of D+/D- pins; it's up to the Receptacle to connect them together or use a mux for more advanced scenarios. Similar with CC and VCONN pins.

For more details about USB Type-C, we recommend [this application note](http://ww1.microchip.com/downloads/en/appnotes/00001953a.pdf) or the [USB Type-C Specification](https://www.usb.org/sites/default/files/USB%20Type-C%20Spec%20R2.0%20-%20August%202019.pdf).

{{% store_links lectronz="https://lectronz.com/products/usb-type-c-plug-breakout-usb-20-only" tindie="https://www.tindie.com/products/arturo182/usb-type-c-plug-breakout-usb-20-only/" %}}

<div class="text-center">

[![USB 2.0 Breakout](/docs/usb-c-breakout/2/perspective.jpg)](/docs/usb-c-breakout/2/perspective.jpg)

</div>
