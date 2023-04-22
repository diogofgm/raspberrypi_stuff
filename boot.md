# Booting from USB is easy on a Pi1, Pi2, or Pi3:

1. Write the latest Raspbian image to an SD card and boot it.

2. Write the latest Raspbian image to a USB drive and plug it into the Pi.

3. Run blkid to determine the PARTUUID of the USB drive.

4. Edit /boot/cmdline.txt and change root=PARTUUID=xxxxxxxx to match the PARTUUID of the USB drive.

5. Reboot. The Pi should be running from the USB drive.

If you ever need to boot from a different USB drive or from the SD card, it's necessary to **FIRST** mount the boot partition of the SD card (/dev/mmcblk0p1) and edit the boot partition's cmdline.txt so that root=PARTUUID=xxxxxxxx matches the device you wish to boot from.
