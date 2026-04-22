# Klipper on the Creality Sermoon D3
Note: This configuration is far from perfect, but it prints :D
Motherboard: CR6WU220525S14
![Photo of the CR6WU220525S14 shipped with the Creality Sermoon D3](https://github.com/phoenixbackrooms/creality-sermoon-d3-klipper/blob/main/mainboard.png)
Firmware compilation options:
```
[ ] Enable extra low-level configuration options
    Micro-controller Architecture (STMicroelectronics STM32)  --->
    Processor model (STM32F401)  --->
    Bootloader offset (64KiB bootloader)  --->
    Communication interface (Serial (on USART1 PA10/PA9))  --->
    Feature Configuration  --->
```
## Current functionality:
- [X] LEDs
- [X] Filament runout sensor
- [X] CRTouch
- [X] XYZ movement
- [X] Hotbed heating and temperature sensing
- [X] Hotend heating and temperature sensing
- [X] Part cooling fan
- [X] Hotend cooling fan
- [X] Exhaust fans
- [ ] Door sensor (Can't find the pin for it.)
- [ ] LCD (May be fixable.)
- [ ] Camera (Likely not fixable, likely routed to secondary MCU.)

## Other notes:
1. The stock firmware stores all prints you send to it over the network, likely the cloud as well to an SD card that doesn't get erased during a factory reset. All gcode files and logs remain readable without data recovery tools.
2. The mainboard contains a STM32F401VET6 for printer operation and a Mediatek MT7688AN with a whopping 128mb of RAM for network communication. A BT antenna is connected, but it seems to be unused on stock firmware.
3. During setup, the printer may ask you for a USB storage device. If the previous owner didn't provide you with one, connect whatever USB drive you have and it *should* go away and let you test it. But honestly if you're here, you're likely putting klipper on it anyway.
4. I *highly* recommend getting a slim USB C cable. Creality didn't make the USB C port easily accessible on this printer. The rear panel of the printer will not sit flush against the frame after this. Except if you fit your host inside the space behind the maintenance panel.
5. The camera quality on stock firmware looks like an Xbox 360 kinect, so not a huge loss other than the nice mounting bracket.
6. All the implementations for DWIN touchscreens seem to involve modifying klipper, which I am personally against. I recommend buying a used Windows tablet with an X86 CPU as you obtain both a host for Klipper and a nice, likely big, or at least not microscopic display for similar prices to a Raspberry pi or even similarly sized touchscreens.

Based on [The Creality Sonic Pad config for the CR-M4](https://github.com/CrealityOfficial/Creality_Sonic_Pad/blob/main/printer_configrations/printer-CrM4-401.cfg)
