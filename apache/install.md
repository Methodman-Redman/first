# apache ready
```bash
yum list | grep httpd
yum install -y httpd httpd-tools httpd-devel httpd-manual
yum list installed | grep httpd
which httpd
```

# config file (No change)

```bash
vi /etc/httpd/conf/httpd.conf
- #ServerName www.example.com:80
+ ServerName CentOS7
```

# httpd.conf check

```bash
[root@CENTOS7 conf]# apachectl configtest
Syntax OK
[root@CENTOS7 conf]#
```

# apache start
```bash
systemctl start httpd
# stop
systemctl stop httpd
```

# firewall setting

```bash
firewall-cmd --add-service=http --zone=public --permanent
firewall-cmd --reload
firewall-cmd --list-all
```
