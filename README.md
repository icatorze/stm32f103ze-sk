# stm32f103ze-sk
Experiences and tricks to run an old STM32F103ZE-SK kit

This board has a Segger J-Link hard wired to uC. I run a Debian 9 for while, and J-Link was detected like:

#sudo dmesg
```
...
[189010.860040] usb 2-2: new full-speed USB device number 2 using uhci_hcd
[189011.064090] usb 2-2: New USB device found, idVendor=1366, idProduct=0101
[189011.064094] usb 2-2: New USB device strings: Mfr=1, Product=2, SerialNumber=3
[189011.064097] usb 2-2: Product: J-Link
[189011.064099] usb 2-2: Manufacturer: SEGGER
[189011.064102] usb 2-2: SerialNumber: xxxxxxxxxxx
...
```
