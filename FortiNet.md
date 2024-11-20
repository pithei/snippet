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


## Packet FLOW debug
```python
diag debug flow trace stop
diag debug { enable | disable | reset }
diag debug flow filter clear
 
diag debug flow filter { addr | saddr | daddr } <IP>
diag debug flow show console enable
diag debug flow trace start 100
diag debug enable
 
# FIXME - Disable acceleration for policy
config firewall policy
edit <ID>
set auto-asic-offload disable
diag firewall iprope show 100004 <policy_id>
diagnose firewall iprope clear 100004 <policy_id>
 
exec log filter device 1        # 1 Disk
exec log filter category 0      # 0 Traffic
exec log filter field policyid <policy_id>
```
