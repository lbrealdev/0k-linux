# diff

diff - compare files line by line

## Usage

```shell
diff file1.txt file2.txt
```

```shell
diff -q file1.txt file2.txt
```

View differences side-by-side:
```shell
diff -y file1.txt file2.txt
```

To focus only on the differences:
```shell
diff --suppress-common-lines -y file1.txt file2.txt
```
