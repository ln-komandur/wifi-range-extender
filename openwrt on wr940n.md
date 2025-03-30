# Install openwrt on TP-Link WR940N

**Hardware version:** V4

**openwrt instructions** are [here](https://openwrt.org/toh/tp-link/tl-wr940n)

**openwrt version:** 18.06.9 

**openwrt firmware files:**

`openwrt-18.06.9-ar71xx-tiny-tl-wr940n-v4-squashfs-factory.bin` is [here](https://downloads.openwrt.org/releases/18.06.9/targets/ar71xx/tiny/openwrt-18.06.9-ar71xx-tiny-tl-wr940n-v4-squashfs-factory.bin)

`openwrt-18.06.9-ar71xx-tiny-tl-wr940n-v4-squashfs-sysupgrade.bin` is [here](https://downloads.openwrt.org/releases/18.06.9/targets/ar71xx/tiny/openwrt-18.06.9-ar71xx-tiny-tl-wr940n-v4-squashfs-sysupgrade.bin)

## Useful videos

[For openwrt](https://youtu.be/zXrxEmLoFbw)

[For DD-wrt](https://youtu.be/nAqVgkVcgwo)

[To restore a bricked router](https://youtu.be/ZW5fpOWpI0I) on windows 

## Error 18005

![Error 18005](./Error%2018005.png)

If you get error  18005 when trying to flash `openwrt-18.06.9-ar71xx-tiny-tl-wr940n-v4-squashfs-factory.bin`, then put the following commands in the SSID field within those single quotes and save one by one

```
`echo "httpd -k"> /tmp/s`
`echo "sleep 10">> /tmp/s`
`echo "httpd -r&">> /tmp/s`
`echo "sleep 10">> /tmp/s`
`echo "httpd -k">> /tmp/s`
`echo "sleep 10">> /tmp/s`
`echo "httpd -f">> /tmp/s`
`sh /tmp/s`
```
