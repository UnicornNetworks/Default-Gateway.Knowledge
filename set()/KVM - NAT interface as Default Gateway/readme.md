# Guide:
https://www.cyberciti.biz/faq/linux-setup-default-gateway-with-route-command/


# Syntax:
route add default gw {IP-ADDRESS} {INTERFACE-NAME}

# example:
```
sudo route add default gw 192.168.122.1 enp1s0

sudo ip route add 192.168.122.0/24 dev enp1s0
```
