# network troubleshooting

Ping troubleshooting:
```
echo "example.com" > hosts.txt
```
Create `ping.sh`
```
vi ping.sh

#!/bin/bash

HOSTS=${HOSTS:-$1}

while read -p "Host to check: " hostname
do
    if [ -z "$hostname" ]; then
        echo "Quitting due to blank input"
        break
    fi
    ping -c 1 -w 5 $hostname > /dev/null 2>&1
    if [ "$?" -eq "0" ]; then
        echo "Contact made with $hostname"
    else
        echo "Failed to make contact with $hostname"
    fi
done < $HOSTS
```
Test connectivy with hosts:
```
./ping.sh hosts.txt
```
