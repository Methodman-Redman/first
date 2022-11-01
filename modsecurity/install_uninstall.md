# install_centos7
`https://www.tohoho-web.com/ex/modsecurity.html`
`https://www.itseclab.jp/security_info/security_intro/modsecurity_construction/`  
## wiki
`https://en.wikipedia.org/wiki/Trustwave_Holdings`  
- dirb 50_out

## modsecurity network(reverce_proxy)
`https://www.itseclab.jp/security_info/security_intro/modsecurity_construction/`
- + permission
- /etc/httpd/conf.d/test2.conf
```bash
ServerName 192.168.xx.136
ProxyRequests Off
ProxyPass / http://192.168.xx.134/index.html/
ProxyPassReverse / http://192.168.xx.134/index.html/

```


# rules_pass
```bash
[root@localhost activated_rules]# pwd
/etc/httpd/modsecurity.d/activated_rules
[root@localhost activated_rules]# ls
modsecurity_35_bad_robots.data               modsecurity_crs_41_sql_injection_attacks.conf
modsecurity_35_scanners.data                 modsecurity_crs_41_xss_attacks.conf
modsecurity_40_generic_attacks.data          modsecurity_crs_42_tight_security.conf
modsecurity_50_outbound.data                 modsecurity_crs_45_trojans.conf
modsecurity_50_outbound_malware.data         modsecurity_crs_47_common_exceptions.conf
modsecurity_crs_20_protocol_violations.conf  modsecurity_crs_48_local_exceptions.conf.example
modsecurity_crs_21_protocol_anomalies.conf   modsecurity_crs_49_inbound_blocking.conf
modsecurity_crs_23_request_limits.conf       modsecurity_crs_50_outbound.conf
modsecurity_crs_30_http_policy.conf          modsecurity_crs_59_outbound_blocking.conf
modsecurity_crs_35_bad_robots.conf           modsecurity_crs_60_correlation.conf
modsecurity_crs_40_generic_attacks.conf
```

# modsecurity_start/stop
```bash
vi /etc/httpd/conf.d/mod_security.conf
# Default recommended configuration
SecRuleEngine Off（←この項目で「On/Off/DetectionOnly）
```


`https://access.redhat.com/documentation/ja-jp/red_hat_enterprise_linux/8/html/deploying_different_types_of_servers/proc_adding-a-custom-rule-to-modsecurity_assembly_securing-web-applications-on-a-web-server-using-modsecurity`
