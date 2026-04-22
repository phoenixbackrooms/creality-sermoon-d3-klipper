# Klipper on the Creality Sermoon D3
Note: This configuration is far from perfect, but it prints :D
Motherboard: CR6WU220525S14
Firmware compilation options:
```
[ ] Enable extra low-level configuration options
    Micro-controller Architecture (STMicroelectronics STM32)  --->
    Processor model (STM32F401)  --->
    Bootloader offset (64KiB bootloader)  --->
    Communication interface (Serial (on USART1 PA10/PA9))  --->
    Feature Configuration  --->
```
Current functionality:
[X] LEDs
[X] Filament runout sensor
[X] CRTouch
[X] XYZ movement
[X] Hotbed heating and temperature sensing
[X] Hotend heating and temperature sensing
[X] Part cooling fan
[X] Hotend cooling fan
[X] Exhaust fans
[] Door sensor (can't find the pin for it, minor issue)
[] LCD (not worth fixing)
[] Camera (Likely not fixable, likely routed to secondary MCU and even if it wasn't Klipper doesn't support it)

Based on [The Creality Sonic Pad config for the CR-M4](https://github.com/CrealityOfficial/Creality_Sonic_Pad/blob/main/printer_configrations/printer-CrM4-401.cfg)
