# pico-ducky-bad-usb
🐥 Pico-Ducky: Turn Your Raspberry Pi Pico into a Rubber Ducky!
This project transforms your Raspberry Pi Pico into a functional USB Rubber Ducky for executing keystroke injection payloads. Follow the steps below to get your Pico-Ducky up and running.
## 🔧 Setup Instructions
1. Install Pico-Ducky Firmware
Head over to the pico-ducky GitHub repository and follow the setup instructions to flash the firmware onto your Raspberry Pi Pico.
2. Configure Non-US Keyboard Layout (Optional)
If you're using a non-US keyboard (e.g., Turkish), you’ll need additional layout files. Visit CircuitPython Keyboard Layouts to find your region’s layout.
3. (Optional) Add Language-Specific Files
Download the following files corresponding to your language (LANG is your country code):
    - keyboard_layout_win_LANG.py.
    - keycode_win_LANG.py.
    - Then, place them inside the lib folder of your CIRCUITPY drive.

    - At the start of the file remove or comment out these lines (add # at the start of the line).

          from adafruit_hid.keyboard_layout_us import KeyboardLayoutUS as KeyboardLayout
          from adafruit_hid.keycode import Keycode
    - And add or uncomment (remove the #) these lines.
    - Replace LANG with the letters for your language of choice. The name must match the file (without the py or mpy extension).

          from keyboard_layout_win_LANG import KeyboardLayout
          from keycode_win_LANG import Keycode

4. Find a Payload
Explore pre-made payloads at the official USB Rubber Ducky GitHub repository — from harmless pranks to useful automations.
5. Add Your Payload
Choose a payload you like and copy its content into a new file named payload.dd. Save this file to the root directory of your CIRCUITPY drive.
## ⚠️ Important Warning
Once the payload is added, it will execute immediately upon connection. After placing payload.dd on the device, safely eject and unplug the Pico before using it.
## ✅ Done!
Just plug your Pico-Ducky into a USB port and watch it go to work.
