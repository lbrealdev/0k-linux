# Tor browser

### Install and verify signature

Download `tor` from **Tor Project** page:
```shell
curl -SLfs https://www.torproject.org/dist/torbrowser/13.0.14/tor-browser-linux-x86_64-13.0.14.tar.xz -o tor-browser-linux-x86_64-13.0.14.tar.xz
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
gpgv --keyring ./tor.keyring ./tor-browser-linux-x86_64-13.0.14.tar.xz.asc ./tor-browser-linux-x86_64-13.0.14.tar.xz
```
**NOTE**: [Tor: How To Verify Signature](https://support.torproject.org/tbb/how-to-verify-signature/)

Once the signature has been verified, extract the contents of the package:
```shell
tar -xf tor-browser-linux-x86_64-13.0.14.tar.xz
```

Navigate to the extracted directory:
```shell
cd tor-browser/
```

Once inside the directory, run `tor browser`.
```shell
./start-tor-browser.desktop
```

**Official page:** https://www.torproject.org/

