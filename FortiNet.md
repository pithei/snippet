## Forti 
Key | Value
---- | ----
Target level | None. Physical conditioning supplement for BJJ
Learning Sources | 
Skill list | 
Task list | none
Daily time slot | time
Tools to obtain | Gi <br />


## Tips
- Eliminate any barrier
- Learn enough to self correct
- choose a project
- create fast feedback loops
- quantity over quality
- practice minimum 20 hours
- spaced repetition

## Forti VPN


```python
# IPSec TSHOOT
# http://cookbook.fortinet.com/ipsec-vpn-troubleshooting/
diagnose debug disable
diagnose vpn ike log-filter clear
diagnose debug application ike -1
diagnose vpn ike log-filter dst-addr4 <IP>
diagnose debug enable
 
# Va web ui flapp tunnel manualy
diagnose debug disable
 
# SSL VPN
diagnose debug reset
diagnose debug application sslvpn -1
diagnose debug application fnbamd -1
diagnose debug enable
```
## Changelog
ID | Date | Notes
---- | ---- | ----
10 | 2022.02.28 | aa

