# Tor browser

### Sources

- [Tor](https://www.torproject.org/)
- [Tor Debian Repository](https://support.torproject.org/apt/)
- [Running Tor Browser](https://tb-manual.torproject.org/running-tor-browser/)
- [Installation](https://tb-manual.torproject.org/installation/)

### Install and verify signature

Download `tor` from **Tor Project** page:
```shell
curl -fsSL https://www.torproject.org/dist/torbrowser/14.0/tor-browser-linux-x86_64-14.0.tar.xz -o tor-browser-linux-x86_64-14.0.tar.xz
```

Download signature key:
```shell
curl -fsSL https://www.torproject.org/dist/torbrowser/14.0/tor-browser-linux-x86_64-14.0.tar.xz.asc -o tor-browser-linux-x86_64-14.0.tar.xz.asc
```

After downloading `tor` installer, let's check the signature:
```shell
gpg --auto-key-locate nodefault,wkd --locate-keys torbrowser@torproject.org
```

Generate key:
```shell
gpg --output ./tor.keyring --export 0xEF6E286DDA85EA2A4BA7DE684E2C6E8793298290
```

Verifying the signature:
```shell
gpgv --keyring ./tor.keyring ./tor-browser-linux-x86_64-14.0.tar.xz.asc ./tor-browser-linux-x86_64-14.0.tar.xz
```
**NOTE**: [Tor: How To Verify Signature](https://support.torproject.org/tbb/how-to-verify-signature/)

Once the signature has been verified, extract the contents of the package:
```shell
tar -xf tor-browser-linux-x86_64-14.0.tar.xz
```

Navigate to the extracted directory:
```shell
cd tor-browser/
```

Once inside the directory, run `tor browser`.
```shell
./start-tor-browser.desktop
```
