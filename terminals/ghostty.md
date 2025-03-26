# Ghostty

Ghostty - [Web](https://ghostty.org/)/[GitHub](https://github.com/ghostty-org/ghostty)

## Installation

```shell
echo 'deb http://download.opensuse.org/repositories/home:/clayrisser:/bookworm/Debian_12/ /' | sudo tee /etc/apt/sources.list.d/home:clayrisser:bookworm.list
curl -fsSL https://download.opensuse.org/repositories/home:clayrisser:bookworm/Debian_12/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/home_clayrisser_bookworm.gpg > /dev/null
sudo apt update
sudo apt install ghostty
```

```shell
apt-file search libx11
apt list --installed | grep libx11
apt-cache search libx11
sudo nala install libx11-dev
```

- https://askubuntu.com/questions/694681/installing-libx11-a-libx11-so-and-xlib-h
- https://github.com/ghostty-org/ghostty/discussions/3739
- https://github.com/clayrisser/debian-ghostty/
- https://ghostty.org/docs/install/binary#linux-(official)
