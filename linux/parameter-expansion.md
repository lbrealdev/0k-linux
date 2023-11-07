# Parameter Expansion

### Examples

Default if Unset or Empty:

```shell
java=""
JAVA_VERSION="${java:-8}"
echo $java
echo $JAVA_VERSION
```

Default if Unset or Empty and Set:

```shell
java=""
JAVA_VERSION="${java:=8}"
echo $java
echo $JAVA_VERSION
```
