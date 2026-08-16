# Linux Network

Search NET-3 networking toolkit:
```shell
apt search net-tools
```

Install netstat:
```shell
sudo apt install net-tools
```

Tuna please! Also known as:
```shell
netstat -tunapl
```

Modern equivalent (`ss` is in `iproute2`):
```shell
ss -tunapl
```

Tests the connection to the IP address 8.8.8.8 by sending 10 packets:
```shell
ping 8.8.8.8 -c 10
```
