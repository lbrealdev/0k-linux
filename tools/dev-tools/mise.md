# mise

mise - dev tools, env vars, task runner

## Sources

- Website: https://mise.jdx.dev/
- GitHub Repository: https://github.com/jdx/mise/

## Usage

```shell
curl -sSL "https://github.com/jdx/mise/releases/download/v2024.6.6/mise-v2024.6.6-linux-x64" > /usr/local/bin/mise

chmod +x /usr/local/bin/mise
```

```shell
echo 'eval "$(mise activate bash)"' >> ~/.bashrc
```

```shell
echo 'export PATH=$HOME/.local/share/mise/shims:$PATH' >> ~/.bashrc
```

Update `mise` version:
```shell
mise self-update
```

```shell
mise use --global node@22

mise settings set experimental true

mise use -g npm:@mermaid-js/mermaid-cli

mise ls

mise uninstall npm:@mermaid-js/mermaid-cli
```
