# Readme

## Notes to self

- I installed ZMK following [these instructions](https://zmk.dev/docs/user-setup). Everything is configured now, so you do not need to follow any of the steps before the section “Installing the firmware”.
- To [put the nice!nano into bootloader mode](https://nicekeyboards.com/docs/nice-nano/getting-started/#:~:text=To%20jump%20into%20the%20bootloader,the%20bootloader%2C%20connect%20your%20nice!), double tap RST and GND pins on the nice!nano quickly with tweezers while the keyboard is plugged to the laptop. If it flashed, you will see a new device called “NICENANO” (a pop up may show up first asking if you want to allow the device to connect to the computer).
- If you experience problems with bluetooth pairing, you may solve it by [resetting both keyboard halves](https://zmk.dev/docs/troubleshooting#reset-split-keyboard-procedure). The GitHub action has already been configured, so you just need to download the `firmware`' file from [here](https://github.com/benthamite/zmk-config/actions/runs/6066203621), and then follow the steps above.
  - Note that you may need to try multiple times since fixing this on macOS is pretty erratic and mysterious (as judging from multiple online comments and my own experience).

## Bluetooth maintenance

The normal thumb keys remain plain modifiers for Karabiner. Bluetooth controls
are available through a maintenance layer:

1. Do not press any key for one second.
2. Hold the four left-half keys `Q`, `T`, `Z`, and `B` within 75 ms.
3. Release `Q`, `T`, and `Z`, but keep `B` held.
4. While holding `B`, press `A`, `S`, `D`, `F`, or `G` to select Bluetooth
   profile 1–5. Press the outer left thumb key to clear the selected profile's
   pairing.
5. Release `B` to return to the normal layer.

After clearing a profile, forget `Corne` on the host before pairing it again.
The maintenance chord is entirely on the central half, so it remains available
when the peripheral half cannot connect.
