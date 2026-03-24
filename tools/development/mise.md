# mise

mise - dev tools, env vars, task runner

## Usage

### Install

Download `mise` binary from GitHub release page with `curl`:

```shell
curl -fsSLo "mise" "https://github.com/jdx/mise/releases/download/v2025.11.8/mise-v2025.11.8-linux-x64"
```

Move `mise` binary to `/usr/local/bin`:

```shell
sudo mv mise /usr/local/bin/
```

Make `mise` binary executable with `chmod`:

```shell
sudo chmod +x /usr/local/bin/mise
```

Enable shell integration using `mise activate`:

```shell
echo 'eval "$(mise activate bash)"' >> ~/.bashrc
```

Add shims path to the PATH environment variable:

```shell
echo 'export PATH=$HOME/.local/share/mise/shims:$PATH' >> ~/.bashrc
```

### Option

Install `mise` via the official install script:

```shell
curl -s https://mise.run | sh
```

Activate shell integration after install script:

```shell
echo 'eval "$(mise activate bash)"' >> ~/.bashrc
```

### Shim

Regenerate shims after installing tools outside of mise:

```shell
mise reshim
```

### Uninstall

Remove `mise` activation lines from `~/.bashrc`:

```shell
sed -i.bak '/\bmise\b/d' ~/.bashrc
```

Remove the `mise` binary:

```shell
sudo rm -rf /usr/local/bin/mise
```

### Update

Update `mise` to the latest version with `self-update`:

```shell
mise self-update -y
```

### Cache

Clear mise's internal cache:

```shell
mise cache clear
```

### Settings

Enable experimental features with `mise settings set`:

```shell
mise settings set experimental true
```

### Manage Tools

Search for a tool in the registry with `mise search`:

```shell
mise search <tool>
```

List installed and active tools with `mise ls`:

```shell
mise ls
```

Display tool metadata with `mise tool`:

```shell
mise tool python
```

List outdated tools with `mise outdated`:

```shell
mise outdated
```

Upgrade all outdated tools with `mise upgrade`:

```shell
mise upgrade
```

Upgrade a specific tool:

```shell
mise upgrade <tool>
```

Install a specific tool with `mise install`:

```shell
mise install <tool>
```

Remove a specific tool with `mise uninstall`:

```shell
mise uninstall <tool>
```

Remove installed tool from `mise.toml` with `mise unuse`:

```shell
mise unuse <tool> -y
```

Display the installation path for a tool with `mise where`:

```shell
mise where <tool>
```

Run a one-off command with a specific tool version using `mise x`:

```shell
mise x node@25 -- node --version
```

### Tools

Install `node`:
```shell
mise use -g node
```

Install `mermaid-cli`:
```shell
mise use -g npm:@mermaid-js/mermaid-cli
```

Install `aws-cli`:
```shell
mise use -g aws-cli
```

### Config

List configuration files with `mise config ls` (or `mise cfg ls`):

```shell
# full
mise config ls

# alias
mise cfg ls
```

Set a config value with `mise cfg set`:

```shell
mise cfg set tools.deno latest
```

List tools with config source, as JSON, and with locations using `-c`, `-J`, `-l` flags:

```shell
mise ls -c -J -l
```

Print all binary paths managed by mise:

```shell
mise bin-paths
```

### Doctor

Run diagnostics to check mise setup:

```shell
mise doctor
```

Check PATH configuration:

```shell
mise doctor path
```

## References

- [mise](https://mise.jdx.dev/)
- [mise GitHub](https://github.com/jdx/mise/)
- [mise Versions](https://mise-versions.jdx.dev/)
