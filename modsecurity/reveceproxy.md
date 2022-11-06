# SELinux
```bash
/usr/sbin/setsebool -P httpd_can_network_connect 1
```
or
```bash
[root@rproxy /]# vi /etc/sysconfig/selinux
SELINUX=disabled
```
# /etc/httpd/conf.d/test.conf
```bash
ProxyRequests Off

<Proxy *>
Order deny,allow
Allow from all
</Proxy>

ProxyPass /foo http://192.168.19.130:8080
ProxyPassReverse /foo http://192.168.19.130:8080

```
