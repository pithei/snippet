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
# https://kb.fortinet.com/kb/documentLink.do?externalID=FD38640
# Each firewall has user.groups limit according to hardware and software
# latest data is here https://docs.fortinet.com/max-value-table
# you can verify current group count by issuing command
# show user group
 
 
# Choose vdom, show ldap servers ( optional )
config vdom
edit <VDOM>
show user ldap
 
 
# List connected FSSO CA.
diag debug reset
diag debug enable
diag debug authd fsso server-status
 
 
# List FSSO logon user on the FortiGate.
diag debug authd fsso list
 
# List authenticated users on the FortiGate.
diag firewall auth list

# Request CA to re-send active users list to FortiGate
diagnose debug authd fsso refresh-logons
 
# Request CA to re-send monitored groups list to FortiGate:
diagnose debug authd fsso refresh-groups
 
# Debugging authentication process*.
diag debug reset
diag debug console timestamp enable
diag debug application authd -1
diag debug application fnbamd -1
diag debug enable
 
# Stop debugging output.
diag debug reset
diag debug disable
 
#
*By default debugging is enabled for 30 minutes.
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
