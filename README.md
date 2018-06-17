# Forward-internet-from-wifi-to-ethernet
How to forward internet from wifi to ethernet interface


DHCP server
https://www.tecmint.com/install-dhcp-server-in-ubuntu-debian/

IP tables:
iptables --table nat --append POSTROUTING --out-interface wlan0 -j MASQUERADE
iptables --append FORWARD --in-interface eth10 -j ACCEPT


for DNS resolv in client:
# echo "nameserver 8.8.8.8" > /etc/resolv.conf
