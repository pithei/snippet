## Forti 

## IPSec VPN


```js
# http://cookbook.fortinet.com/ipsec-vpn-troubleshooting/
diagnose debug disable
diagnose vpn ike log-filter clear
diagnose debug application ike -1
diagnose vpn ike log-filter dst-addr4 <IP>
diagnose debug enable
 
# Va web ui flapp tunnel manualy
diagnose debug disable
 

```

## SSL VPN

```bash
diagnose debug reset
diagnose debug application sslvpn -1
diagnose debug application fnbamd -1
diagnose debug enable
```

## FSSO

```python
diagnose debug reset
diagnose debug application sslvpn -1
diagnose debug application fnbamd -1
diagnose debug enable
```

