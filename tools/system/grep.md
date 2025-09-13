# grep

grep, egrep, fgrep, rgrep - print lines that match patterns

## Usage

Show 2 lines before and after the match:
```shell
printf "C\nC++\nPython\nRust\nGolang\nRuby\nJava\nJavaScript\n" | grep -i -C2 "rust"
```

### Lookarounds

Extract all sequences of letters, digits, underscores, or hyphens that appear after a `/`:
```shell
echo "https://website.com/c/91m01377-8k90-1984-a77c-c098dvd6198" | grep -oP '(?<=/)[\w-]+'
```

Extract the substring after the last `/`:
```shell
echo "https://website.com/c/91m01377-8k90-1984-a77c-c098dvd6198" | grep -oP '[^/]+$'
```

Extracts digits that are immediately followed by `:` in the string:
```shell
echo "arn:aws:iam::111199712814:role/my-lambda-role" | grep -oP '\d+(?=:)'
```

Extracts digits preceded by `::` in the string:
```shell
echo "arn:aws:iam::111199712814:role/my-lambda-role" | grep -oP '(?<=::)\d+'
```
