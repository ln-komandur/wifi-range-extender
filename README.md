# Wifi Range Extender with TP-Link WR940N

## Assumptions:
1. IP address of primary router is 192.168.0.1
2. Wifi Range extender also has the same IP address (192.168.0.1) to begin with
3. The Primary router and the extender have different SSIDs and Passwords to begin with
4. When connected to the extender, to begin with there is no internet
5. The Primary router is connected to the internet (via a separate modem or otherwise)


## Steps
1. Connect to the Wifi Network (SSID) of the Wifi Extender. Open its admin page at http://192.168.0.1 and login with admin credentials.
2. Under Network -> LAN, change ip address of the extender to have an IP address different from the parent router / dhcp server. This is to avoid any IP address conflicts. e.g. Change from http://192.168.0.1 to http://192.168.0.2 . Disable IGMP and restart the device
3. Use new IP (http://192.168.0.2) to log into Wifi extender admin page. In wireless settings, enable WDS mode and survey for the primary router and give the credentials for the Primary router's Wifi
4. Connect to http://192.168.0.2 and disable DHCP and give the IP address of the default gateway as the primary router's (e.g. Change from http://192.168.0.2 (self) to http://192.168.0.1) and restart the device. After it restarts there WILL BE internet connection when connecting to the SSID of the extender IF the primary router is connected to the Internet.
5. Connect	to http://192.168.0.2 and give the same password as primary router under Wireless Security. Do not change the SSID yet. Reconnect and reauthenticate with this password after connection is lost because you just changed the password. Then change the name of the wifi SSID on extender to be the same as gateway. Do not mix up this order. 
6. From now on, you can connect to both routers using only the primary router's Wifi SSID. You can access their admin pages by their distinguishing IP addresses
7. Change admin password of the Wifi Extender if needed (if you had done any hard resets while performing the above steps)
8. You can also make any other fine tuning further to the above.
