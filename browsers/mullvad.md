# Mullvad browser

Download `mullvad` browser from **Mullvad** page:
```shell
curl -SLfs https://mullvad.net/pt/download/browser/linux64/latest -o mullvad-browser.tar.xz
```

Once the download is finished, extract the contents of the package:
```shell
tar -xf mullvad-browser.tar.xz
```

Navigate to the extracted directory:
```shell
cd mullvad-browser/
```

Once inside the directory, run `mullvad browser`.
```shell
./start-mullvad-browser.desktop
```

Add a Dock / Dash shortcut:
```shell
cp start-mullvad-browser.desktop ~/.local/share/applications/
```

**Official page:** https://mullvad.net/en/browser
