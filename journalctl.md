# journalctl

Query the journal with message explanations in immediately jump to the end in the pager:
```shell
journalctl -xe
```

Follow the journal messages:
```shell
journalctl -xf
```

List all boots made:
```shell
journalctl --list-boots
```

Get logs from the last boot:
```shell
journalctl --boot
```
