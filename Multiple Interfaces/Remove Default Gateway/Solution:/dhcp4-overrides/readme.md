```
dhcp4-overrides:
  use-routes: false
```

# Solution:
sch: https://www.google.com/search?q=%22ip+route+del+default%22+netplan+reboot

## Answer:
- https://askubuntu.com/questions/1298995/default-gateway-route-being-automatically-added-to-main-table
- https://unix.stackexchange.com/questions/517995/prevent-netplan-from-creating-default-routes-to-0-0-0-0-0


## source:
/etc/netplan/99_config.yaml
```
network:
    ethernets:
        ens19:
            dhcp4: true
            dhcp4-overrides:
                use-routes: false
            routes:
              - to: 10.0.0.0/16
                via: 10.0.90.1
    version: 2
```
