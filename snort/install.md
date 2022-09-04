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

