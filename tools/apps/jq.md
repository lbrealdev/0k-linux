# jq

Command-line JSON processor.

## Sources

- https://jqlang.org/
- https://github.com/jqlang/jq

## Usage

Iterate over an array with `.[]`, filter objects with `select`, and format output with string interpolation `\()`:

```shell
cat repos.json | jq -r '.[] | select(.fork != true and .owner.login == "owner") | "\(.name),\(.private)"'
```

Same as above with an additional `select` condition to exclude private repos:

```shell
cat repos.json | jq -r '.[] | select(.fork != true and .owner.login == "owner" and .private == false) | "\(.name),\(.private)"'
```

Use `-R` for raw string input, `split` to break on delimiter, and object constructor `{}` to name the fields:

```shell
echo "repo-name,description,true,https://myweb.io" | jq -R 'split(",") | {name: .[0], description: .[1], private: .[2], homepage: .[3]}'
```

Use `map` with `length` to generate separator lines, `@tsv` to format as tab-separated values, and pipe to `column` for alignment:

```shell
cat repos.json | jq -r '(["REPO","PRIVATE","FORK","HOMEPAGE"] | (., map(length*"-"))), (.[] | [.full_name, .private, .fork, .homepage]) | @tsv' | column -ts $'\t'
```

## Merge JSON files

Slurp all input files into an array and merge with `add`:

```shell
jq -s 'add' file1.json file2.json
```

Deep merge with `*` (later values override earlier ones):

```shell
jq -s '.[0] * .[1]' file1.json file2.json
```

Merge specific keys from multiple files:

```shell
jq -s '{name: .[0].name, config: .[1].config}' file1.json file2.json
```
