# Raspberry Pi Pico Setup

## Steps:
1. Copy adafruit-circuitpython-raspberry_pi_pico_w-it_IT-8.0.5.uf2 file in the RPI Pico base folder.
2. Copy in the RPI Pico lib folder:
    - adafruit_hid
    - adafruit_debouncer.mpy
    - adafruit_ticks.mpy
    - asyncio
    - adafruit_wsgi 
3. Copy in the RPI Pico base folder:
    - boot.py
    - duckyinpython.py
    - code.py
    - webapp.py
    - wsgiserver.py
    - secrets.py
    - keyboard_layout_win_it.py
    - keyboard_layout_win_sw.py
    - keycode_win_it.py
    - keycode_win_sw.py
4. Copy payload.dd in the RPI Pico base folder to open Rick Roll Youtube Video when the Raspberry Pi Pico is plugged.

## Reset RPI Pico
1. Plug the RPI Pico in the computer pressing the bootsel button.
2. Copy the flash_nuke.uf2 file in the RPI Pico base folder.
