# install
```bash
sudo yum upgrade -y

## dpkg install(your like install)
sudo yum -y install epel-release
sudo yum repolist
sudo yum install dpkg-devel dpkg-dev

## sub install(error cut version)
sudo yum install gcc make httpd unzip wget sendmail inotify-tools -y

Loaded plugins: fastestmirror, langpacks
Loading mirror speeds from cached hostfile
 * base: ftp.riken.jp
 * extras: ftp.riken.jp
 * updates: ftp.riken.jp
Package gcc-4.8.5-44.el7.x86_64 already installed and latest version
Package 1:make-3.82-24.el7.x86_64 already installed and latest version
Package unzip-6.0-24.el7_9.x86_64 already installed and latest version
Package wget-1.14-18.el7_6.1.x86_64 already installed and latest version
Package sendmail-8.14.7-6.el7.x86_64 already installed and latest version
No package inotify-tools available. #error
Nothing to do

```

## ossec install
```bash
wget https://github.com/ossec/ossec-hids/archive/2.9.0.tar.gz
tar -xvzf 2.9.0.tar.gz
cd ossec-hids-2.9.0
sh install.sh
```

## manual
```bash
# start
/var/ossec/bin/ossec-control start
# stop
/var/ossec/bin/ossec-control stop
# restart
/var/ossec/bin/ossec-control restart
```

# web_ui
```bash
sudo yum install httpd php
sudo chkconfig httpd on

sudo yum install git
git clone https://github.com/ossec/ossec-wui.git

sudo mv ossec-wui /var/www/html/ossec
cd /var/www/html/ossec/
sudo ./setup.sh

# -----------.sh-----------------
Username: root
New password:
Re-type new password:
Adding password for user root
Enter your web server user name (e.g. apache, www, nobody, www-data, ...)
apache
Enter your OSSEC install directory path (e.g. /var/ossec)
/var/ossec
You must restart your web server after this setup is done.
Setup completed successfuly.
# ------------.sh-----------------

sudo gpasswd -a apache ossec
sudo chmod 770 /var/ossec/tmp
sudo chgrp apache /var/ossec/tmp
sudo service httpd start

# SELinux setting
setenforce 0

# thanks
# https://bobcares.com/blog/install-ossec-ubuntu-like-a-pro/
# https://dev.classmethod.jp/articles/using-ossec-on-ec2/
# https://qiita.com/hanaita0102/items/5d3675e4dc1530b255ba
```

# rules
```bash
[root@localhost rules]# pwd
/var/ossec/rules
[root@localhost rules]# ls
apache_rules.xml     courier_rules.xml    imapd_rules.xml        ms-se_rules.xml        pam_rules.xml         racoon_rules.xml       squid_rules.xml        trend-osce_rules.xml        web_rules.xml
apparmor_rules.xml   dovecot_rules.xml    local_rules.xml        mysql_rules.xml        php_rules.xml         roundcube_rules.xml    sshd_rules.xml         unbound_rules.xml           wordpress_rules.xml
arpwatch_rules.xml   dropbear_rules.xml   mailscanner_rules.xml  named_rules.xml        pix_rules.xml         rules_config.xml       symantec-av_rules.xml  vmpop3d_rules.xml           zeus_rules.xml
asterisk_rules.xml   firewalld_rules.xml  mcafee_av_rules.xml    netscreenfw_rules.xml  policy_rules.xml      sendmail_rules.xml     symantec-ws_rules.xml  vmware_rules.xml
attack_rules.xml     firewall_rules.xml   msauth_rules.xml       nginx_rules.xml        postfix_rules.xml     smbd_rules.xml         syslog_rules.xml       vpn_concentrator_rules.xml
cimserver_rules.xml  ftpd_rules.xml       ms_dhcp_rules.xml      openbsd_rules.xml      postgresql_rules.xml  solaris_bsm_rules.xml  sysmon_rules.xml       vpopmail_rules.xml
cisco-ios_rules.xml  hordeimp_rules.xml   ms-exchange_rules.xml  opensmtpd_rules.xml    proftpd_rules.xml     sonicwall_rules.xml    systemd_rules.xml      vsftpd_rules.xml
clam_av_rules.xml    ids_rules.xml        ms_ftpd_rules.xml      ossec_rules.xml        pure-ftpd_rules.xml   spamd_rules.xml        telnetd_rules.xml      web_appsec_rules.xml
```



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
