# install  
`https://qiita.com/Ynolen/items/e7e8915b78c8add2e4da`  
`wget https://www.snort.org/downloads/snort/snort-2.9.20.tar.gz`   
`sed -i 's/include \$RULE\_PATH/#include \$RULE\_PATH/' /etc/snort/rules/snort.conf`


```bash

yum update

# like install
yum install wget
yum install gcc
yum install flex
yum install bison
yum install libpcap-devel
yum install pcre-devel
yum install libdnet-devel
yum install zlib-devel
yum install openssl-devel

#daq install
wget https://www.snort.org/downloads/snort/daq-2.0.7.tar.gz
tar -xvzf daq-2.0.7.tar.gz
cd daq-2.0.7
./configure && make && make install
cd ..
wget http://luajit.org/download/LuaJIT-2.0.5.tar.gz
tar -xvzf LuaJIT-2.0.5.tar.gz
cd LuaJIT-2.0.5
make && make install

# snort install
cd ..
wget https://www.snort.org/downloads/snort/snort-2.9.20.tar.gz
tar -xvzf snort-2.9.20.tar.gz
cd snort-2.9.20
./configure --enable-sourcefire && make && make install
snort -V

   ,,_     -*> Snort! <*-
  o"  )~   Version 2.9.20 GRE (Build 82) 
   ''''    By Martin Roesch & The Snort Team: http://www.snort.org/contact#team
           Copyright (C) 2014-2022 Cisco and/or its affiliates. All rights reserved.
           Copyright (C) 1998-2013 Sourcefire, Inc., et al.
           Using libpcap version 1.5.3
           Using PCRE version: 8.32 2012-11-30
           Using ZLIB version: 1.2.7
```

# community rules install
```bash
wget https://www.snort.org/rules/community -O ~/community.tar.gz
tar -xvf ~/community.tar.gz -C ~/
cp ~/community-rules/* /etc/snort/rules
sed -i 's/include \$RULE\_PATH/#include \$RULE\_PATH/' /etc/snort/snort.conf
vi  /etc/snort/snort.conf
#-----snort.conf-----
# Setup the network addresses you are protecting
ipvar HOME_NET <server_public_ip>/24

# Path to your rules files (this can be a relative path)
var RULE_PATH /etc/snort/rules
var SO_RULE_PATH /etc/snort/so_rules
var PREPROC_RULE_PATH /etc/snort/preproc_rules

# Set the absolute path appropriately
var WHITE_LIST_PATH /etc/snort/rules
var BLACK_LIST_PATH /etc/snort/rules

# unified2
# Recommended for most installs
output unified2: filename snort.log, limit 128

include $RULE_PATH/local.rules
include $RULE_PATH/community.rules
#-----snort.conf-----

sudo snort -T -c /etc/snort/snort.conf
vi /etc/snort/rules/local.rules
#-----local.rules-----
alert icmp any any -> $HOME_NET any (msg:"ICMP get"; sid:10000001; rev:001;)
#-----local.rules-----

snort -u snort -g snort -c /etc/snort/snort.conf -i ens33 -A console
# ping check

vi /lib/systemd/system/snort.service
#-----snort.service-----
[Unit]
Description=Snort NIDS Daemon
After=syslog.target network.target

[Service]
Type=simple
ExecStart=/usr/local/bin/snort -u snort -g snort -c /etc/snort/snort.conf -i ens33 -A full -b -D 

[Install]
WantedBy=multi-user.target
#-----snort.service-----
```

# check
```bash
sudo systemctl daemon-reload
sudo systemctl start snort
sudo systemctl status snort
```

# community.rules
- Line59,153-164,407-
```bash
:%s/$ETERNAL...//g
```

# mistake plus

`https://qiita.com/Brutus/items/b11c3324492a4e25a152`
```bash
# vi /etc/snort/snort.conf
> include $RULE_PATH/community.rules
```

