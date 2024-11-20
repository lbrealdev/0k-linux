# mise

### Usage

```shell
curl -sSL "https://github.com/jdx/mise/releases/download/v2024.6.6/mise-v2024.6.6-linux-x64" > /usr/local/bin/mise

chmod +x /usr/local/bin/mise

echo 'eval "$(mise activate bash)"' >> ~/.bashrc

echo 'export PATH=$HOME/.local/share/mise/shims:$PATH' >> ~/.bashrc
```

```shell
mise use --global node@22

mise settings set experimental true

mise use -g npm:@mermaid-js/mermaid-cli

mise ls

mise uninstall npm:@mermaid-js/mermaid-cli
```

Update mise version:
```shell
mise self-update
```

### Source

- https://github.com/jdx/mise/
- https://mise.jdx.dev/
