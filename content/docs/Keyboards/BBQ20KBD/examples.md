---
title: Example Code
weight: 3
url: "/docs/bbq20kbd/examples"
---

Of course, we don't just leave you with the board and a "good luck", here's some example code to get you started.

The BBQ20KBD interface is compatible with the one in the Keyboard PMOD, you can use the same libraries and code.

## CircuitPython

You can find the CircuitPython library [here](https://github.com/solderparty/arturo182_CircuitPython_BBQ10Keyboard), additional libraries are needed, see the README.md for more details. The code has been tested with CircuitPython 7.0.

{{< highlight python >}}
import board
from bbq10keyboard import BBQ10Keyboard, STATE_PRESS, STATE_RELEASE, STATE_LONG_PRESS

i2c = board.I2C()
kbd = BBQ10Keyboard(i2c)

kbd.backlight = 0.5

while True:
    key_count = kbd.key_count
    if key_count > 0:
        key = kbd.key
        state = 'pressed'
        if key[0] == STATE_LONG_PRESS:
            state = 'held down'
        elif key[0] == STATE_RELEASE:
            state = 'released'

        print("key: '%s' (dec %d, hex %02x) %s" % (key[1], ord(key[1]), ord(key[1]), state))
{{< / highlight >}}

## Arduino

You can find the Arduino library [here](https://github.com/solderparty/arduino_bbq10kbd) as well as through the Library Manager in the Arduino IDE.

{{< highlight cpp >}}
#include <BBQ10Keyboard.h>

BBQ10Keyboard keyboard;

void setup()
{
  Serial.begin(9600);
  Wire.begin();

  keyboard.begin();
  keyboard.setBacklight(0.5f);
}

void loop()
{
  const int keyCount = keyboard.keyCount();
  if (keyCount == 0)
    return;

  const BBQ10Keyboard::KeyEvent key = keyboard.keyEvent();
  String state = "pressed";
  if (key.state == BBQ10Keyboard::StateLongPress)
    state = "held down";
  else if (key.state == BBQ10Keyboard::StateRelease)
    state = "released";

  Serial.printf("key: '%c' (dec %d, hex %02x) %s\r\n", key.key, key.key, key.key, state.c_str());

  // pressing 'b' turns off the backlight and pressing Shift+b turns it on
  if (key.state == BBQ10Keyboard::StatePress) {
    if (key.key == 'b') {
      keyboard.setBacklight(0);
    } else if (key.key == 'B') {
      keyboard.setBacklight(1.0);
    }
  }
}
{{< / highlight >}}
