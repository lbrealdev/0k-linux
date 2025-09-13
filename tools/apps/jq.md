# jq

Command-line JSON processor.

## Sources

- https://jqlang.org/
- https://github.com/jqlang/jq

## Usage

```shell
cat repos.json | jq -r '.[] | select(.fork != true and .owner.login == "owner") | "\(.name),\(.private)"'
```

```shell
cat repos.json | jq -r '.[] | select(.fork != true and .owner.login == "owner" and .private == false) | "\(.name),\(.private)"'
```

```shell
echo "repo-name,description,true,https://myweb.io" | jq -R 'split(",") | {name: .[0], description: .[1], private: .[2], homepage: .[3]}'
```

```shell
cat repos.json | jq -r '(["REPO","PRIVATE","FORK","HOMEPAGE"] | (., map(length*"-"))), (.[] | [.full_name, .private, .fork, .homepage]) | @tsv' | column -ts $'\t'
```
