adbmove
=======

A simple python utility to do the following
- move files/directories from your android device to your laptop
- copy files/directories from your android device to your laptop
- perform the above from any particular device with the --device parm

###Prerequisites
- python installation :)
- access to adb on the system path
- the directories to be moved/copied should be accessible via adb

###Usage

```bash
./adbmove.py [--device devicename] [--copy] source_dir destination_dir
```

###Example

Move files from /mnt/sdcard/alpha to the current directory

```bash
./adbmove.py /mnt/sdcard/alpha
```

Copy files from /mnt/sdcard/alpha on a particular device (assuming multiple devices are connected) to the Desktop

```bash
./adbmove.py --device TA9330F9WK --copy /mnt/sdcard/alpha ~/Desktop
```

The device id that needs to be passed in --device can be obtained from adb devices

###Sample output

```bash
Moved  /mnt/sdcard/alpha --> ~/Desktop
```
