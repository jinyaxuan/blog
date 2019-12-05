---
id: connect-to-nju-vpn-without-the-terrible-client
tags: []
date: 2019-12-03 10:02:19
title: Connect to NJU VPN without the Terrible Client
categories: WTF
---

```bash
apt install x-window-system-core
apt install gnome-core
apt install libgtk2.0-0:i386


ip route add table 100 default via <GATEWAY> dev eth0
ip route add table 200 default dev tun0 # proto kernel scope link src 2.0.0.118
ip rule add from all table 100
ip rule add fwmark 254 table 200


# iptables -t nat -D OUTPUT -p udp -m udp ! --sport 7789 --dport 53 -j DNAT --to-destination 127.0.0.1:5373
# ip rule add to 114.114.114.114 table main


# no-resolv
# server=114.114.114.114
```

```json
{
    "log": {
        "error": "/var/log/v2ray.log",
        "loglevel": "warning"
    },
    "inbounds": [
        {
            "protocol": "vmess",
            "port": <PORT>,
            "settings": {
                "clients": [
                    {
                        "id": "<USER_ID>"
                    }
                ]
            }
        }
    ],
    "outbounds": [
        {
            "protocol": "freedom",
            "tag": "direct",
            "streamSettings": {
                "sockopt": {
                    "mark": 254
                }
            }
        }
    ]
}
```
