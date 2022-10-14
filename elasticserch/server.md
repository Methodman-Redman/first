# site
`https://www.itseclab.jp/security_info/security_intro/elasticstack_construction/`  
- all 8.x

- logstash
```
[elasticsearch-8.x]
name=Elasticsearch repository for 8.x packages
baseurl=https://artifacts.elastic.co/packages/8.x/yum
gpgcheck=1
gpgkey=https://artifacts.elastic.co/GPG-KEY-elasticsearch
enabled=1
autorefresh=1
type=rpm-md
```

`https://www.creationline.com/blog/h-hibino/39088`


# secound
```
root@localhost ~]# yum update
CentOS Stream 8 - AppStream                     4.5 MB/s |  25 MB     00:05    
CentOS Stream 8 - BaseOS                        4.3 MB/s |  25 MB     00:05    
CentOS Stream 8 - Extras                         48 kB/s |  18 kB     00:00    
CentOS Stream 8 - Extras common packages         11 kB/s | 4.9 kB     00:00    
Dependencies resolved.
Nothing to do.
Complete!
[root@localhost ~]# dnf update
Last metadata expiration check: 0:01:15 ago on Fri 14 Oct 2022 10:16:04 PM JST.
Dependencies resolved.
Nothing to do.
Complete!
[root@localhost ~]# yum install git
Last metadata expiration check: 0:01:49 ago on Fri 14 Oct 2022 10:16:04 PM JST.
Dependencies resolved.
================================================================================
 Package               Arch        Version                 Repository      Size
================================================================================
[root@localhost ~]# yum install --allowerasing docker-ce.x86_64 
Last metadata expiration check: 0:01:42 ago on Fri 14 Oct 2022 10:30:56 PM JST.
Dependencies resolved.

Complete!
[root@localhost ~]# yum install --allowerasing docker-ce-cli-.x86_64 

Complete!
[root@localhost ~]# yum install --allowerasing containerd.io docker-compose-plugin
Last metadata expiration check: 0:01:36 ago on Fri 14 Oct 2022 10:34:48 PM JST.
Package containerd.io-1.6.8-3.1.el8.x86_64 is already installed.
Dependencies resolved.
================================================================================
 Package                  Arch      Version           Repository           Size
================================================================================

Installed:
  docker-compose-plugin-2.11.2-3.el8.x86_64                                     

Complete!
[root@localhost ~]# docker -v
Docker version 20.10.19, build d85ef84
[root@localhost ~]# systemctl start docker
[root@localhost ~]# docker run hello-world
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
2db29710123e: Pull complete 
Digest: sha256:18a657d0cc1c7d0678a3fbea8b7eb4918bba25968d3e1b0adebfa71caddbc346
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.


```
