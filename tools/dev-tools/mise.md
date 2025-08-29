# mise

mise - dev tools, env vars, task runner

## Sources

- Website: https://mise.jdx.dev/
- GitHub Repository: https://github.com/jdx/mise/

## Usage

### Install

```shell
curl -fsSLo "mise" "https://github.com/jdx/mise/releases/download/v2025.8.18/mise-v2025.8.18-linux-x64"
```

```shell
sudo mv mise /usr/local/bin/
```

```shell
sudo chmod +x /usr/local/bin/mise
```

```shell
echo 'eval "$(mise activate bash)"' >> ~/.bashrc
```

```shell
echo 'export PATH=$HOME/.local/share/mise/shims:$PATH' >> ~/.bashrc
```

### Uninstall

// to do

### Update

Update `mise` version:
```shell
mise self-update
```

### Settings

```shell
mise settings set experimental true
```

### Manage Tools

List installed and active tools:
```shell
mise ls
```

Setup node v22:
```shell
mise use --global node@22
```

Setup mermaid-cli:
```shell
mise use -g npm:@mermaid-js/mermaid-cli

mise uninstall npm:@mermaid-js/mermaid-cli
```
