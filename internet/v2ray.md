# v2ray
## Installation
### server side (Using Ubuntu 18.04 LTS, should work with other versions of Ubuntu as well.)
<code>wget https://install.direct/go.sh && chmod +x go.sh && ./go.sh</code>

You may need <code>sudo</code> in case of any permission issue.

Config file at <code>/etc/v2ray/config.json</code>

Use <code>systemctl</code> to control v2ray service
* Start v2ray service <code>sudo systemctl start v2ray</code>
* Stop v2ray service <code>sudo systemctl stop v2ray</code>
* View status of v2ray service <code>sudo systemctl status v2ray</code>
## Basic Configuration (config.json)
*Note: only related parts are shown, basically it will work after installation*
### Server side
```json
"inbounds": [{
    "port": /* portnumber */,
    "protocol": "vmess",
    "settings": {
        "clients": [{
            "id": /* uuid */,
            "level": 1,
            "alterId": 64
        }]
    }
}]
```
> Use <code>uuidgen</code> to generate uuid.\
> <code>New-Guid</code> in Windows PowerShell may also work. (Not tested)