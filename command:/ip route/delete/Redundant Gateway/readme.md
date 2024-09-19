# Delete Redundant Gateway
If you have a server with a 2nd "Private" network, it can interfere with internet access!

sch: https://www.google.com/search?q=ip+route+remove

# guide:
- https://unix.stackexchange.com/questions/403511/how-to-delete-an-ip-route

# source:
Remove duplicate route:
```
interface=enp7s0
gateway=10.0.1.1
mask=32

ip route del $gateway/$mask

sudo ip addr flush dev $interface
```
