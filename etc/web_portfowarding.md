# images
client -> 192.168.xx.136:80 -> 192.168.xx.134:80
# 192.168.xx.136 config
```bash
# check
firewall-cmd --get-active-zone
public
  interfaces: ens33 ens36
# setting
firewall-cmd --zone=public --add-forward-port=port=80:proto=tcp:toport=80:toaddr=192.168.xx.134 --permanent
success
firewall-cmd --reload
success
firewall-cmd --list-all --zone=public
public (active)
  target: default
  icmp-block-inversion: no
  interfaces: ens33
  sources: 
  services: dhcpv6-client ssh
  ports: 
  protocols: 
  masquerade: no
  forward-ports: port=80:proto=tcp:toport=80:toaddr=192.168.xx.134
  source-ports: 
  icmp-blocks: 
  rich rules: 
	
firewall-cmd --zone=public --query-masquerade
no
firewall-cmd --zone=public --add-masquerade --permanent
success
firewall-cmd --reload
success
firewall-cmd --zone=public --query-masquerade
yes
firewall-cmd --list-all --zone=public
public (active)
  target: default
  icmp-block-inversion: no
  interfaces: ens33 ens36
  sources: 
  services: dhcpv6-client ssh
  ports: 
  protocols: 
  masquerade: yes
  forward-ports: port=80:proto=tcp:toport=80:toaddr=192.168.xx.134
  source-ports: 
  icmp-blocks: 
  rich rules: 

```
- client http://192.168.xx.136 -> 192.168.xx.134 yes
