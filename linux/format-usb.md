# Linux - Format USB

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
LABEL_NAME="<usb-name-here>"

mkfs.vfat -I -F 32 -n $LABEL_NAME /dev/sdc -v
```
