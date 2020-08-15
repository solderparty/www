---
title: GPIO Configurations
weight: 3
---

Thanks to the flexibility of the SAMD21 SERCOM peripheral, the Serpente boards give you access to multiple serial interfaces with just 6 GPIOs. See [Pinout]({{< relref "/docs/serpente/r1/pinout.md" >}}) for an overview of the pins.

Note that most of the interfaces are easily accessible using CircuitPython, altough some of them can't be used at the same time:
{{< highlight python >}}
import board, busio

spi = board.SPI()
i2c = board.I2C()
uart = board.UART()
uart2 = busio.UART(board.TX2, board.RX2)
{{< / highlight >}}

Here's a list of some of the ways you can configure the GPIOs on your Serpente:

## SPI + 3 GPIOs
<div class="text-center"><img src="/docs/serpente/r1/config-spi.png" style="width: 500px"></div>

## I2C + 4 GPIOs
<div class="text-center"><img src="/docs/serpente/r1/config-i2c.png" style="width: 500px"></div>

## UART + 4 GPIOs
<div class="text-center">
    <img src="/docs/serpente/r1/config-uart.png" style="width: 500px">
    <br><br>
    or
    <br><br>
    <img src="/docs/serpente/r1/config-uart2.png" style="width: 500px">
</div>

## 2x UART + 2 GPIOs
<div class="text-center">
<img src="/docs/serpente/r1/config-2xuart.png" style="width: 500px"><br><br>

**Note: Because of a quirk on CircuitPython's implementation, you need to initialize UART 2 before UART.**
</div>

## SPI + I2C + 1 GPIO
<div class="text-center"><img src="/docs/serpente/r1/config-spi-i2c.png" style="width: 500px"></div>

## SPI + UART + 1 GPIO
<div class="text-center"><img src="/docs/serpente/r1/config-spi-uart.png" style="width: 500px"></div>

## UART + I2C + 2 GPIOs
<div class="text-center"><img src="/docs/serpente/r1/config-uart-i2c.png" style="width: 500px"></div>

## 6 GPIOs
See [Pinout]({{< relref "/docs/serpente/r1/pinout.md" >}}).
