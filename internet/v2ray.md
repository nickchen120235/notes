# v2ray
## Installation
### Server (Ubuntu 18.04 LTS, should work with other versions of Ubuntu as well.)
<code>wget https://install.direct/go.sh && chmod +x go.sh && ./go.sh</code>

<code>sudo</code> if you encounter any permission issue.

Use <code>systemctl</code> to control v2ray service
* Start v2ray service <code>sudo systemctl start v2ray</code>
* Stop v2ray service <code>sudo systemctl stop v2ray</code>
* View status of v2ray service <code>sudo systemctl status v2ray</code>

### Client (Windows 10)
Visit https://github.com/v2ray/v2ray-core/releases to get the executables.

## Basic Configuration (config.json)
*Note: only related parts are shown, for server side, basically it will work after installation*
### Server
Config file at <code>/etc/v2ray/config.json</code>
```json
"inbounds": [{
    "port": 1234,
    "protocol": "vmess",
    "settings": {
        "clients": [{
            "id": "712ce14d-4f85-49df-9588-9a57e9cd541e",
            "level": 1,
            "alterId": 64
        }]
    }
}]
```
"port": port number exposed to client\
"id": uuid of client
> Use <code>uuidgen</code> to generate uuid.\
> <code>New-Guid</code> in Windows PowerShell may also work. (Not tested)

### Client
Config file at <code>/v2ray-windows-64/config.json</code>

#### inbounds: Computer -> v2ray client
```json
"inbounds": [{
    "port": 10101,
    "listen": "127.0.0.1",
    "protocol": "http",
    "settings": {
        "auth": "noauth",
        "udp": false,
        "ip": "127.0.0.1"
    },
    "sniffing": {
        "enabled": true,
        "destOverride": ["http", "tls"]
    }
}]
```
"port": port exposed to local computer\
"listen": "127.0.0.1" to prevent any other computer found that the port is open\
"protocol": "http" for other clients on local computer to connect\
"settings", "sniffing" not sure how they work

#### outbounds: v2ray client -> v2ray server
```json
"outbound": [{
    "protocol": "vmess",
    "settings": {
        "vnext": [{
            "address": "1.1.1.1",
            "port": 1234,
            "users": [{
                "id": "712ce14d-4f85-49df-9588-9a57e9cd541e",
                "alterId": 64
            }]
        }]
    }
}]
```
"protocol": same as server\
"vnext":
- "address": server ip
- "port": same as server
- "users":
    - "id": same as server-side "client": "id"
    - "alterId": same as server-side "client": "alterId"
