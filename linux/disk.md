# Linux Disk

### Linux disk error

```shell
Error mounting /dev/sdb at /media/localhost/94941159-309b-4a4a-a4b6-0908bd913704: Command-line `mount -t "ext4" -o "uhelper=udisks2,nodev,nosuid,errors=remount-ro" "/dev/sdb" "/media/localhost/94941159-309b-4a4a-a4b6-0908bd913704"' exited with non-zero exit status 32: mount: /dev/sdb: can't read superblock
```

Fix:
```shell
sudo su

fsck -y /dev/sdb
```
