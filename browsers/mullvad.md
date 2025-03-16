# Mullvad browser

### Sources

- https://mullvad.net/en/browser

### Install

Download `mullvad` browser from **Mullvad** website:
```shell
curl -fsSLo mullvad-latest.tar.xz "https://mullvad.net/en/download/browser/linux64/latest"
```

Once the download is finished, extract using tar:
```shell
tar -xf mullvad-latest.tar.xz
```

Navigate to the extracted directory:
```shell
cd mullvad-latest/
```

Once inside the directory, run `mullvad browser`.
```shell
./start-mullvad-browser.desktop
```

Add a Dock / Dash shortcut:
```shell
cp start-mullvad-browser.desktop ~/.local/share/applications/
```
