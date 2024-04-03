# Adafruit's Macropad and Keyboard Layouts

When using the `adafruit_macropad` library with Adafruit's Macropad, you can setup the layout and keycode classes in the constructor with code like this. Changing the **PLATFORM_LANGUAGE** modules names for the ones you use of course.

```py
from adafruit_macropad import MacroPad

from keyboard_layout_PLATFORM_LANGUAGE import KeyboardLayout
from keycode_PLATFORM_LANGUAGE import Keycode

macropad = MacroPad(
    layout_class=KeyboardLayout,
    keycode_class=Keycode,
)
```

[See this file in the macropad library](https://github.com/adafruit/Adafruit_CircuitPython_MacroPad/blob/main/examples/macropad_keyboard_layout.py) for a full example script.

## The Hotkeys Project

For [the popular hotkeys project](https://learn.adafruit.com/macropad-hotkeys), you will have to update **code.py** with the change above, making sure you replace the existing `macropad = MacroPad()` line, and not add one.

You also have to change the macros to use the keycodes setup in the macropad module instead of the `adafruit_hid` default keycode module. The `adafruit_macropad.keycodes` is a module-level variable that is setup with the value defined in the MacroPad class. When it's imported in the macros files it shares that value with the one defined in **code.py**.

Replace in every macro file:
```py
from adafruit_hid.keycode import Keycode
```
With:
```py
from adafruit_macropad import keycodes as Keycode
```

Note that some of the default macros might still use key names that are not available on your keyboard, or shortcuts that do not match the localized version of your applications. For example there is no `[` key on a French keyboard, if a shortcut uses it, it pust be changed to the correct shortcut for your application.
