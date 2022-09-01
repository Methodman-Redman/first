# uninstall
```bash
/var/ossec/bin/ossec-control stop #error
service ossec-hids stop 
chkconfig ossec-hids --del # error
rm -rf /var/ossec 
rm -f /etc/ossec-init.conf 
rm -f /etc/init.d/*ossec* 
userdel ossecr 
userdel ossec 
groupdel ossec
# https://github.com/ossec/ossec-hids/issues/1025
# + locate ossec
```
