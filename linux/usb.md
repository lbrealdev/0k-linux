# Linux USB

## Format USB on Linux

### Usage

Run these commands to format the USB:

As a sudo user:
```shell
sudo su
```

List all block devices:
```shell
lsblk
```

List all mounted filesystems:
```shell
df -hT
```

After identifying your USB device, unmount the USB by running this command:
```shell
umount /dev/sdc1
```

**NOTE:** The `/dev/sdc1` is my USB drive device on my computer, you should identify your device once you connect it to the computer, with the commands listed above `lsblk` and `df`.

Format the USB by running this command:
```shell
LABEL_NAME="<usb-name>"

mkfs.vfat -I -F 32 -n $LABEL_NAME /dev/sdc -v
```

### Other Linux commands to detect USB

List USB devices:
```shell
lsusb
```

Print USB device details:
```shell
usb-devices
```

Print devices USB filtering by version:
```shell
usb-devices | grep -i -E "Product=USB DISK [0-9]+\.[0-9]" -B4 -A5
```
