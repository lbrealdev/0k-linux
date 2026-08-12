# VirtualBox

## Source

- https://www.virtualbox.org/

## Contents

<!-- TOC -->

- [Resize VDI](#resize-vdi)
- [Kill VirtualBox processes](#kill-virtualbox-processes)
- [VBox commands](#vbox-commands)
- [Resources](#resources)
- [Related links](#related-links)

## Resize VDI

Grow a `.vdi` on the host when the VM is out of disk space.

`--resize` is the **new size in MB**, not the amount to add. `51200` is 50 GB.
Power the VM off first. This does not shrink a disk, and it does not grow
the partition or filesystem inside the guest.

Check the current size:

```shell
VBoxManage showmediuminfo disk "/path/to/yourdisk.vdi"
```

Set the new size (example: 50 GB):

```shell
VBoxManage modifymedium disk "/path/to/yourdisk.vdi" --resize 51200
```

Then boot the guest and extend the partition/filesystem there
(`growpart` + `resize2fs`/`xfs_growfs` on Linux, Disk Management on Windows).

## Kill VirtualBox processes

Use this when a VM is frozen or the VirtualBox UI will not quit.
Stop **one** VM with `VBoxManage` first. Killing every `VBox*` process
with `SIGKILL` can corrupt the disk and leave lock files behind.

See what is running:

```shell
VBoxManage list runningvms
```

Ask the VM to shut down (ACPI):

```shell
VBoxManage controlvm "VM name" acpipowerbutton
```

If it ignores ACPI, power it off:

```shell
VBoxManage controlvm "VM name" poweroff
```

If `VBoxManage` itself is stuck, list the processes:

```shell
pgrep -a -f 'VirtualBoxVM|VBox|VirtualBox'
```

Last resort, kill a **specific** PID (not the whole pipeline):

```shell
kill -9 <pid>
```

## VBox commands

List registered VMs (name and UUID), running or not:

```shell
VBoxManage list vms
```

List only VMs that are running right now:

```shell
VBoxManage list runningvms
```

## Resources

- [OSBoxes](https://www.osboxes.org/)

## Related links

- [AutoStart VirtualBox VMs on System Boot on Linux](https://tinfoil-hat.net/posts/vbox-autostart/)
- [SSH into VirtualBox VM](https://www.golinuxcloud.com/ssh-into-virtualbox-vm/)
