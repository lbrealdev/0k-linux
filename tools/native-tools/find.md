# find

find - search for files in a directory hierarchy

## Usage

Use find to search in `/var/local/*` without entering subdirectories, looking only for directories that were modified in the last 7 days, and print their paths:
```shell
find /var/local/* -maxdepth 1 -type d -mtime 7 -print
```

Use find to search in the current directory, print the paths of the found items, redirect the error output (stderr), and filter the results using grep:
```shell
find ./ -print 2>&1 | grep "<pattern>"
```

The same command as the previous one, but now using the option to search recursively in all files and directories, ignoring case sensitivity, and displaying the line number where the pattern is found:
```shell
find ./ -print 2>&1 | grep -Rin "<pattern>"
```

Locate and display detailed information for all files with the '.yml' extension within the `/home/user/` directory.
```shell
find /home/user/ -name "*.yml" -ls
```

Use find to search two directories:
```shell
find ./ -type d \( -name "<pattern>" -o -name "<pattern>" \)
```

Use find to seach for specific files and move to destination path:
```shell
find . -type f -name "pattern_*" -exec mv "{}" /move/to/path \;
```
