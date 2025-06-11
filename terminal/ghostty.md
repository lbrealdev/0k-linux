# Ghostty

## Sources

- https://ghostty.org
- https://github.com/ghostty-org/ghostty

## Installation

Currently, `ghostty` for Debian is provided by an community-maintained repository.

- https://github.com/clayrisser/debian-ghostty/

```shell
echo 'deb http://download.opensuse.org/repositories/home:/clayrisser:/bookworm/Debian_12/ /' | sudo tee /etc/apt/sources.list.d/home:clayrisser:bookworm.list
curl -fsSL https://download.opensuse.org/repositories/home:clayrisser:bookworm/Debian_12/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/home_clayrisser_bookworm.gpg > /dev/null
sudo apt update
sudo apt install ghostty
```

You may find some dependency errors at the time of `ghostty` installation, to fix these errors follow the commands below:
```shell
apt search libx11-dev
apt-cache policy libx11-dev
sudo apt install libx11-dev
```

## Usage

Ghostty help:
```shell
ghostty +help
```

Get ghostty version:
```shell
ghostty +version
```

Ghostty show config:
```shell
ghostty +show-config
```

List fonts:
```shell
ghostty +list-fonts
```

List themes:
```shell
ghostty +list-themes
```

Ghostty configuration file:
```
~/.config/ghostty/config
```

## Related links

- https://ghostty.org/docs/install/binary#linux-(official)
- https://github.com/ghostty-org/ghostty/discussions/3739
- https://askubuntu.com/questions/694681/installing-libx11-a-libx11-so-and-xlib-h
