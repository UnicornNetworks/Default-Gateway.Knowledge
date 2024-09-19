# Delete Redundant Gateway
If you have a server with a 2nd "Private" network, it can interfere with internet access!

sch: https://www.google.com/search?q=linux+ip+route+delete+default+gateway


# Guide: Solution:
- https://www.baeldung.com/linux/ip-remove-default-gateway


# source:
Remove duplicate route:
```
interface=enp7s0
gateway=10.0.1.1
mask=32

ip route -p del $gateway/$mask

sudo ip addr flush dev $interface

update_cache()
```

# Persistant:
sch: https://www.google.com/search?q=ip+route+delete+reboot&oq=ip+route+delete+reboot , https://www.google.com/search?q=ip+route+delete+persistent+reboot , https://www.google.com/search?q=%22ip+route+del%22+persistent+reboot

https://www.unix.com/solaris/228021-delete-route-so-does-not-persist-after-reboot.html

A.I.
>routes set using ip route add or route add can disappear after restarting. To prevent this, you can use the -p key to make the route permanent.
