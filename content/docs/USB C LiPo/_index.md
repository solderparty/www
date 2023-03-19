---
title: "LiPo Battery Charger w/ USB-C Plug"
weight: 4
---

Charge your LiPo batteries directly from your USB Type-C port!

This board can be used to charge 3.7V/4.2V lithium polymer (LiPo) and lithium ion (LiIon) batteries. The JST connector is very common for these kinds of batteries. You can also use the header pins to skip the connector and charge the battery that way.

The two LEDs show the status of the charging process. While the battery is charging, the "Charge" (orange) LED is on, once the battery is fully charged the "Done" (green) LED lights up. It is normal for either or both LEDs to be on if no battery is connected.

See the Downloads section for the datasheet of the ME4055-N (MCP73831 for rev 1) IC and more details about the charging process.

By default the battery is charged with 600mA (500mA for rev 1), if you want to change the charge current you can change the R2 resistor. See the schematics or the datasheet for more information.

# Safety warnings

**Make sure the batteries you're trying to charge match the configuration (1S), chemistry (LiPo or LiIon), and voltage (3.7V/4.2V) of the charger!**

**Make sure you don't swap the polarity of the battery (+ and - are marked on the board)!**

**Don't leave the charger unattended while charging.**

**It is normal for the charger to get warm while charging (within reason), if you feel it getting too warm, you can lower the charge current (see above).**

<div class="container">

[![Plugs](/docs/usb-c-lipo/perspective.jpg)](/docs/usb-c-lipo/perspective.jpg)

</div>
