# Tor browser

Download `tor` from Tor Project page:
```shell
curl -SLfs https://www.torproject.org/dist/torbrowser/12.5.1/tor-browser-linux64-12.5.1_ALL.tar.xz -o tor-browser.tar.xz
```

Once the download is finished, extract the contents of the package:
```shell
tar -xvf tor-browser.tar.xz
```

Navigate to the extracted directory:
```shell
cd tor-browser/
```

Once inside the directory, run `tor browser`.
```shell
./start-tor-browser.desktop
```
