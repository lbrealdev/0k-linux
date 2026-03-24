# nmap

nmap - Network exploration tool and security / port scanner

## Installation

```shell
sudo apt install nmap -y
```

## Usage

Get version:
```shell
nmap --version
```

Discover active devices on the local network subnet `192.168.1.0/24`, also known as `ping scan`:
```shell
nmap -sP 192.168.1.0/24
```

Check which hosts are up, without scanning ports:
```shell
sudo nmap -sn 192.168.1.0/24
```
