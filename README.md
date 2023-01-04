# Script: ufwfirewall 
The Script prints the status of the ufw firewall.

![firewall status on](https://user-images.githubusercontent.com/90487955/210626416-c88d6369-2846-42e2-bec4-8367af643f28.png) ![firewall status off](https://user-images.githubusercontent.com/90487955/210626413-67138186-fb1c-4505-9feb-a3ba1f1f951a.png)    

Use `click-right` to disable and `click-left` to enable, you can change it as you like.

## Dependencies
* `ufw`


## Configuration

Add the following line in /etc/sudoers of your user:

``` python
user ALL=(ALL) NOPASSWD: /usr/bin/ufw
```
# Module

``` python
type = custom/script
exec = ~/.config/polybar/scripts/firewall.sh
interval = 5
format = <label>
click-right = sudo ufw disable
click-left = sudo ufw enable
```
