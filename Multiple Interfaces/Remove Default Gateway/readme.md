# Delete Redundant Gateway
If you have a server with a 2nd "Private" network, it can interfere with internet access!

sch: https://www.google.com/search?q=linux+ip+route+delete+default+gateway


# Guide: Solution:
- https://www.baeldung.com/linux/ip-remove-default-gateway

# source:
Remove duplicate route:
```
interface=enp7s0
sudo ip route del default dev $interface
```
