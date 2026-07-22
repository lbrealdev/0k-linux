# awk

gawk - pattern scanning and processing language

## Usage

Count the number of character `<pattern>`:
```shell
cat file.txt | awk -v FPAT='e' '{print NF}'
```

If `IGNORECASE` is set, it will catch both `Linux` and `linux`:
```shell
cat file.txt | awk -v IGNORECASE=1 -v FPAT='e' '{print NF}'
```

### AWK series by Tecmint

- https://www.tecmint.com/read-awk-input-from-stdin-in-linux/
