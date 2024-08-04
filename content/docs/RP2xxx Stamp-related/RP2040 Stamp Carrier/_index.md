---
title: "RP2040 Stamp Carrier"
linkTitle: "RP2040&nbsp;Stamp&nbsp;Carrier"
weight: 5
no_list: true
url: "/docs/rp2040-stamp/carrier"
---

The Carrier was created as a reference design for the RP2040 Stamp, but don't let the name fool you, it is also compatible with the RP2350 Stamp. It comes with a combo SMD/TH Stamp footprint, you can solder the Stamp directly to the Carrier or use 2mm pin headers + sockets to be able to plug it in and out.

The board can be powered from the LiPo, over USB, or with a DC jack.

By using the RP2040 Stamp Carrier, you get everything that comes with the Stamp plus:

- A bootsel button
- 3.7/4.2V LiPo connector
- Qwiic connector
- USR LED
- Power (3.3V) LED
- SWD header
- USB Type-C connector
- DC Jack

The DC Jack input is center-positive and supports voltages in the range of 7-12V. If you have the LiPo and either DC or USB connected, the battery will begin charging.

The board follows the Uno shield pinout, making it compatible with a large ecosystem of shields, as long as they work on 3.3V IOs. **The pins are not 5V-tolerant**.

The SWD header follows the Cortex 10-pin standard.

The CircuitPython firmware for the Stamps comes with a built-in board file for the Carrier, you can access it using `import stamp_carrier_board as board`. After that, you can access all the Carrier pins and interfaces like you would with any other CPY board.

{{% store_links lectronz="https://lectronz.com/products/rp2040-stamp" tindie="https://www.tindie.com/products/arturo182/rp2040-stamp-carrier/" %}}

<div class="text-center">

[![With the RP2040 Stamp](/docs/rp2040-stamp/carrier/carrier.jpg)](/docs/rp2040-stamp/carrier/carrier.jpg)

</div>

<div class="text-center">

[![With the RP2350 Stamp](/docs/rp2040-stamp/carrier/carrier_rp2350.jpg)](/docs/rp2040-stamp/carrier/carrier_rp2350.jpg)

</div>

## Downloads

### Datasheets/Specifications
- [XL1509-5.0 buck converter](https://www.lcsc.com/datasheet/lcsc_datasheet_2403200255_UMW-Youtai-Semiconductor-Co---Ltd--XL1509-5-0_C2902368.pdf)

### Hardware Files
The KiCad hardware source files for the board can be found on [Github](https://github.com/solderparty/rp2040_stamp_carrier_hw/tree/rev1).

### Schematics

<div class="text-center">

[![Schematics](/docs/rp2040-stamp/carrier/schematics_rp2040_stamp_carrier.png)](/docs/rp2040-stamp/carrier/schematics_rp2040_stamp_carrier.png)

</div>

### Drawing

<div class="text-center">

[![Drawing](/docs/rp2040-stamp/carrier/drawing_rp2040_stamp_carrier.png)](/docs/rp2040-stamp/carrier/drawing_rp2040_stamp_carrier.png)

</div>

### Leaflet

<div class="text-center">

[![Leaflet](/docs/rp2040-stamp/carrier/rp2040_stamp_carrier_leaflet.png)](/docs/rp2040-stamp/carrier/rp2040_stamp_carrier_leaflet.png)

</div>
