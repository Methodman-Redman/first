`https://qiita.com/829yasubee/items/2eaf1dc517c1f3f7b64b`


```
ubuntu@ubuntu:/var/log$ cat syslog | grep Elastic
Nov 22 17:55:14 ubuntu systemd[1]: Started Elastic Agent is a unified agent to observe, monitor and protect your system..
ubuntu@ubuntu:/var/log$ journalctl | grep Elastic
Nov 22 17:55:14 ubuntu systemd[1]: Started Elastic Agent is a unified agent to observe, monitor and protect your system..
```

```
ps -aux
root       45595  0.7  0.8 1555128 35044 ?       Ssl  17:55   0:06 /opt/Elastic/Agent/elastic-agent
root       45611  0.4  2.8 1461816 112820 ?      Sl   17:55   0:03 /opt/Elastic/Agent/data/elastic-agent-1428d5/install/filebeat-7.10.0-linux-x86_64/filebeat -E setup.ilm.enabled=false -E setup.templ
root       45625  2.2  2.3 1426260 94112 ?       Sl   17:55   0:19 /opt/Elastic/Agent/data/elastic-agent-1428d5/install/metricbeat-7.10.0-linux-x86_64/metricbeat -E setup.ilm.enabled=false -E setup.t
root       45638  1.3  3.9 1462552 155356 ?      Sl   17:55   0:11 /opt/Elastic/Agent/data/elastic-agent-1428d5/install/filebeat-7.10.0-linux-x86_64/filebeat -E setup.ilm.enabled=false -E setup.templ
root       45655  0.1  2.1 1352016 85940 ?       Sl   17:55   0:01 /opt/Elastic/Agent/data/elastic-agent-1428d5/install/metricbeat-7.10.0-linux-x86_64/metricbeat -E setup.ilm.enabled=false -E setup.t
root       45829  0.1  0.0      0     0 ?        I    18:03   0:00 [kworker/0:0-events]

```

```
ubuntu@ubuntu:/opt/Elastic/Agent$ pwd
/opt/Elastic/Agent
ubuntu@ubuntu:/opt/Elastic/Agent$ ls
data  elastic-agent  elastic-agent.log  elastic-agent.reference.yml  elastic-agent.yml  elastic-agent.yml.2022-11-22T17-55-14.7662.bak  fleet.yml  LICENSE.txt  NOTICE.txt  README.md

```
