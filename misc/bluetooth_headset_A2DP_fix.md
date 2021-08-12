# Fix Bluetooth headset A2DP

Basically:

Downgrade `bluez`, `bluez-lib` and `bluez-utils` to version 5.58-1 and remove `/var/lib/bluetooth` then re-pair headphones.

source: https://bbs.archlinux.org/viewtopic.php?pid=1978509#p1978509