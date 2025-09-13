# ps

ps - report a snapshot of the current processes.

## Usage

List process:
```shell
ps -auxwf
```

List processes filtering by a concrete process using grep:
```shell
ps -aux | grep <process>
```

```shell
ps -efa
```

```shell
ps -C "ghostty" -o user,pid,%mem,command
```

```shell
ps -eo user,pid,%mem,command --sort=%mem
```

```shell
ps -eo user,pid,%cpu,%mem,command --sort=%cpu
```
