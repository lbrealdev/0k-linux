 # systemd

 // Add description
 
 List all services:
 ```
 systemctl list-units --type service --all
 ```

 List all timers:
 ```
 systemctl list-units --type timer --all
 ```

 List all targets:
 ```
 systemctl list-units --type target --all
 ```
 
 List unit file and show state:
 ```
 systemctl list-unit-files --full
 ```

 List unit file for timers:
 ```
 systemctl list-unit-files --type timer
 ```

 List unit file for targets:
 ```
 systemctl list-unit-files --type target
 ```

List unit file for services:
 ```
 systemctl list-unit-files --type service
 ```

 Show service unit file:
 ```
 systemctl cat sshd.service
 ```