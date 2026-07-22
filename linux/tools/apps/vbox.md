# virtual box

## Source

- https://www.virtualbox.org/

## Usage

Resize `vdi`:
```shell
VBoxManage modifymedium "/path/to/yourdisk.vdi" --resize 51200
```

List virtual machines:
```shell
VBoxManage list vms
```

List running virtual machines:
```shell
VBoxManage list runningvms
```

Get VirtualBox processes:
```shell
ps -aux | grep -E 'VirtualBoxVM|VBox|VirtualBox'
```

```shell
sudo kill -9 $(ps -aux | grep -E 'VirtualBoxVM|VBox|VirtualBox' | awk '{print $2}' | head -n -1)
```

## Resources

- [OSBoxes](https://www.osboxes.org/)

## Related links

- [AutoStart VirtualBox VMs on System Boot on Linux](https://tinfoil-hat.net/posts/vbox-autostart/)
- [SSH into VirtualBox VM](https://www.golinuxcloud.com/ssh-into-virtualbox-vm/)
