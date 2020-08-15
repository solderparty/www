---
title: Example Code
weight: 3
---

Of course, we don't just leave you with the board and a "good luck"; here are some code examples to get you started with your FeatherWing.

Make sure to visit the [example code repo](https://github.com/arturo182/keyboard_featherwing_sw) on Github for more example code.

These examples have been tested with the [Adafruit Feather M4 Express](https://www.adafruit.com/product/3857), depending on which Feather you're using, some modifications might be needed.

## CircuitPython

Tested with CircuitPython 5.0. Additional libraries are needed, see [README.md](https://github.com/arturo182/keyboard_featherwing_sw/blob/master/circuitpython/README.md) for details.

### Initializing the LCD

{{< highlight python >}}
import adafruit_ili9341
import displayio
import board

displayio.release_displays()

spi = board.SPI()
tft_cs = board.D9
tft_dc = board.D10

display_bus = displayio.FourWire(spi, command=tft_dc, chip_select=tft_cs)
display = adafruit_ili9341.ILI9341(display_bus, width=320, height=240)
{{< / highlight >}}

### Using the Touch Screen

{{< highlight python >}}
import board, digitalio
from adafruit_stmpe610 import Adafruit_STMPE610_SPI

spi = board.SPI()
touch_cs = board.D6

touch = Adafruit_STMPE610_SPI(spi, digitalio.DigitalInOut(touch_cs))
while touch.buffer_empty:
    pass

print(touch.read_data())
{{< / highlight >}}

### Using the Keyboard

{{< highlight python >}}
from bbq10keyboard import BBQ10Keyboard
import board

i2c = board.I2C()
kbd = BBQ10Keyboard(i2c)

while kbd.key_count == 0:
    pass

print(kbd.keys)
{{< / highlight >}}

### Using the microSD card

{{< highlight python >}}
import board, digitalio
import adafruit_sdcard
import storage, os

spi = board.SPI()
sd_cs = board.D5

sdcard = adafruit_sdcard.SDCard(spi, digitalio.DigitalInOut(sd_cs))
vfs = storage.VfsFat(sdcard)
storage.mount(vfs, '/sd')

print(os.listdir('/sd/'))
{{< / highlight >}}

### Using the Neopixel

{{< highlight python >}}
import board,
import neopixel

neopix_pin = board.D11

pixels = neopixel.NeoPixel(neopix_pin, 1)
pixels[0] = 0xFF00FF
{{< / highlight >}}

## Arduino

### Initializing the LCD

{{< highlight cpp >}}
#include <Adafruit_GFX.h>
#include <Adafruit_ILI9341.h>

#define TFT_CS 9
#define TFT_DC 10

Adafruit_ILI9341 tft(TFT_CS, TFT_DC);

void setup()
{
  tft.begin();
  tft.setRotation(1);
  tft.println("Hello World");
}
{{< / highlight >}}

### Using the Touch Screen

{{< highlight cpp >}}
#include <Adafruit_STMPE610.h>

#define STMPE_CS 6

#define TS_MINX 150
#define TS_MINY 130
#define TS_MAXX 3800
#define TS_MAXY 4000

Adafruit_STMPE610 ts(STMPE_CS);

void setup()
{
  ts.begin();
  while (ts.bufferEmpty()) {
    ;
  }

  TS_Point p = ts.getPoint();
  p.x = map(p.x, TS_MINY, TS_MAXY, tft.height(), 0);
  p.y = map(p.y, TS_MINX, TS_MAXX, 0, tft.width());
}
{{< / highlight >}}

### Using the Keyboard

{{< highlight cpp >}}
#include <BBQ10Keyboard.h>

BBQ10Keyboard keyboard;

void setup()
{
  Wire.begin();
  keyboard.begin();
  while (!keyboard.keyCount()) {
    ;
  }
  const BBQ10Keyboard::KeyEvent key = keyboard.keyEvent();
}
{{< / highlight >}}

### Using the microSD card

{{< highlight cpp >}}
#include <SD.h>

#define SD_CS 5

void setup()
{
  SD.begin(SD_CS);
  File root = SD.open("/");
}
{{< / highlight >}}

### Using the Neopixel

{{< highlight cpp >}}
#include <Adafruit_NeoPixel.h>

#define NEOPIXEL_PIN 11

Adafruit_NeoPixel pixels(1, NEOPIXEL_PIN, NEO_GRB + NEO_KHZ800);

void setup()
{
    pixels.setPixelColor(0, pixels.Color(255, 0, 255));
    pixels.show();
}
{{< / highlight >}}
