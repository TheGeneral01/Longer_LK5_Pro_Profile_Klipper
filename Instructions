 STEPS:

- You're going to need to flash your board first, the Generic MKS Robin E3 config is what I followed

- Follow the top steps here for the config on Klipper's config github (generic-mks-robin-e3), don't follow the rest of the instructions as they won't work on this board

- See other image file for the values when using makeconfig

- Don't edit the baud rate, it should say by default 250000 (change it to that if it shows differently)

- Hit Q, Save the menuconfig and enter "make"

- Once the firmware has been created, the firmware will be in "out" directory named "klipper.bin"

- Copy the klipper.bin file to an SD card and rename it to "firmware.bin" on the SD card, Make Sure it is FAT32, not ExFAT, *ONLY* FAT32

- Unplug the SD card, shut down your printer, and put the SD card into your printer (in my case it's the Longer LK5 Pro)

- Turn on the printer and the printer should start flashing the firmware

- Once it says it's done, and at 100% you can shut down the printer, unplug the SD card and turn it back on

Finally, you got that dang thing flashed, now you gotta edit your Klipper's printer.cfg file

- In your Klipper's printer.cfg file, you'll need to paste in the serial id under [mcu]

- You can easily obtain the serial id by accessing your host device's terminal -> ls /dev/serial/by-id/

- In my case, the serial shows on my Raspberry Pi as -> /dev/serial/by-id/usb-1a86_USB_Serial-if00-port0

- Copy that, and paste it into your printer.cfg file under [mcu] as

[mcu]

serial: /dev/serial/by-id/usb-1a86_USB_Serial-if00-port0

restart_method: command

- Restart Klipper and it should connect

As far as configuring the printer's motors, extruder and hot bed, I'm still working the kinks out there but I at least am able to control my LK5 Pro now through MainsailOS.

Hopefully someone out there finds this useful, I searched high and low for the answer but it's a pretty simple issue overall.

From @MrLuigiPower on Reddit: https://www.reddit.com/r/klippers/comments/1kf3z9p/finally_got_mks_robin_e3_v11_working_with_klipper/
