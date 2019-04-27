# stm32f103ze-sk
Experiences and tricks to run an old STM32F103ZE-SK kit.

IAR still has information about schematics about this board, you can download it here:

[IAR STM32F103ZE-SK Updates](https://www.iar.com/iar-embedded-workbench/add-ons-and-integrations/updates-for-iar-kickstart-kit/)

Direct link to files: 
ftp://ftp.iar.se/WWWfiles/kit_updates/IAR%20KickStart%20Kit-ST.zip

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

Download from Segger website, J-Link software .deb package:
[Segger J-Link software deb Package](https://www.segger.com/downloads/jlink/JLink_Linux_x86_64.deb)

Install deb package with dpkg command:
```console
jack@jaragua:~$ sudo dpkg -i JLink_Linux_V644g_x86_64.deb
```

After sucessfull installation, I connect an USB cable to board's USB_Jlink and run ~JLinkSTM32~ command to reset options byte to factory settings, choosing option 2 for STM32F1xxxx:
```console
jack@jaragua:/opt/SEGGER/JLink$ ./JLinkSTM32
```

I previously installed Eclipse CDT, gcc-arm-none-eabi and gdb-arm-none-eabi packages from Debian Repository:
```
jack@jaragua:~$ sudo apt-get install eclipse-cdt gcc-arm-none-eabi gdb-arm-none-eabi
```

Now, make a register in ST.com website to download STM32CubeMx and start configuration for a basis project:
[ST STM32CubeMX software](https://www.st.com/en/development-tools/stm32cubemx.html)








