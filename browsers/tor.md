# Tor browser

Download `tor` from **Tor Project** page:
```shell
curl -SLfs https://www.torproject.org/dist/torbrowser/13.0/tor-browser-linux-x86_64-13.0.tar.xz -o tor-latest.tar.xz
```

Once the download is finished, extract the contents of the package:
```shell
tar -xf tor-latest.tar.xz
```

Navigate to the extracted directory:
```shell
cd tor-latest/
```

Once inside the directory, run `tor browser`.
```shell
./start-tor-browser.desktop
```

**Official page:** https://www.torproject.org/
