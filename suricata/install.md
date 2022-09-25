yum -y install epel-release
yum -y install libpcap-devel pcre-devel libyaml-devel file-devel zlib-devel jansson-devel nss-devel libcap-ng-devel libnet-devel tar make libnetfilter_queue-devel lua-devel

# refarence
`https://suricata.readthedocs.io/en/suricata-6.0.5/install.html`

```bash
yum install epel-release yum-plugin-copr
yum copr enable @oisf/suricata-6.0
yum install suricata



```

https://suricata.readthedocs.io/en/suricata-6.0.5/install.html　　

https://qiita.com/centos1205/items/47f3e8f58b3d13458a3c
