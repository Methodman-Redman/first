# centos
## stop
```
[root@localhost systemd]# tail -f /var/log/messages 
Nov 17 22:28:31 localhost chronyd[932]: Source 31.210.52.137 replaced with 18.180.64.47 (2.centos.pool.ntp.org)
Nov 17 22:28:31 localhost systemd[1]: NetworkManager-dispatcher.service: Succeeded.
Nov 17 22:28:33 localhost su[10270]: (to root) cent on pts/0
Nov 17 22:29:01 localhost systemd[1]: fprintd.service: Succeeded.
Nov 17 22:29:33 localhost chronyd[932]: Selected source 204.93.207.12 (2.centos.pool.ntp.org)
Nov 17 22:31:30 localhost systemd[1]: systemd-journal-flush.service: Succeeded.
Nov 17 22:31:30 localhost systemd[1]: Stopped Flush Journal to Persistent Storage.
Nov 17 22:31:30 localhost systemd[1]: Stopping Journal Service...
Nov 17 22:31:30 localhost systemd[1]: Stopping Flush Journal to Persistent Storage...
Nov 17 22:31:30 localhost systemd-journald[730]: Journal stopped
```

```
[root@localhost systemd]# journalctl -n 10
-- Logs begin at Sun 2022-11-06 20:37:09 JST, end at Thu 2022-11-17 22:31:30 JST. --
Nov 17 22:28:33 localhost.localdomain su[10270]: (to root) cent on pts/0
Nov 17 22:28:33 localhost.localdomain su[10270]: pam_systemd(su:session): Cannot create session: Already running in a session or user slice
Nov 17 22:28:33 localhost.localdomain su[10270]: pam_unix(su:session): session opened for user root by (uid=1000)
Nov 17 22:29:01 localhost.localdomain systemd[1]: fprintd.service: Succeeded.
Nov 17 22:29:33 localhost.localdomain chronyd[932]: Selected source 204.93.207.12 (2.centos.pool.ntp.org)
Nov 17 22:31:30 localhost.localdomain systemd[1]: systemd-journal-flush.service: Succeeded.
Nov 17 22:31:30 localhost.localdomain systemd[1]: Stopped Flush Journal to Persistent Storage.
Nov 17 22:31:30 localhost.localdomain systemd[1]: Stopping Journal Service...
Nov 17 22:31:30 localhost.localdomain systemd[1]: Stopping Flush Journal to Persistent Storage...
Nov 17 22:31:30 localhost.localdomain systemd-journald[730]: Journal stopped
```

## normal
```
[root@localhost systemd]# journalctl -n 10
-- Logs begin at Sun 2022-11-06 20:37:09 JST, end at Thu 2022-11-17 22:35:57 JST. --
Nov 17 22:31:30 localhost.localdomain systemd[1]: Stopping Flush Journal to Persistent Storage...
Nov 17 22:31:30 localhost.localdomain systemd-journald[730]: Journal stopped
Nov 17 22:35:57 localhost.localdomain systemd[1]: systemd-journald.service: Succeeded.
Nov 17 22:35:57 localhost.localdomain systemd[1]: Stopped Journal Service.
Nov 17 22:35:57 localhost.localdomain systemd[1]: Starting Journal Service...
Nov 17 22:35:57 localhost.localdomain systemd-journald[10590]: Journal started
Nov 17 22:35:57 localhost.localdomain systemd-journald[10590]: Runtime journal (/run/log/journal/23baffd1890447448d3556e700bb8605) is 8.0M, max 89.2M, 81.2M free.
Nov 17 22:35:57 localhost.localdomain systemd[1]: Started Journal Service.
Nov 17 22:35:57 localhost.localdomain systemd[1]: Starting Flush Journal to Persistent Storage...
Nov 17 22:35:57 localhost.localdomain systemd[1]: Started Flush Journal to Persistent Storage.
```
```
[root@localhost systemd]# tail -f  /var/log/messages 
Nov 17 22:31:30 localhost systemd[1]: Stopping Flush Journal to Persistent Storage...
Nov 17 22:31:30 localhost systemd-journald[730]: Journal stopped
Nov 17 22:35:57 localhost systemd[1]: systemd-journald.service: Succeeded.
Nov 17 22:35:57 localhost systemd[1]: Stopped Journal Service.
Nov 17 22:35:57 localhost systemd[1]: Starting Journal Service...
Nov 17 22:35:57 localhost systemd-journald[10590]: Journal started
Nov 17 22:35:57 localhost systemd-journald[10590]: Runtime journal (/run/log/journal/23baffd1890447448d3556e700bb8605) is 8.0M, max 89.2M, 81.2M free.
Nov 17 22:35:57 localhost systemd[1]: Started Journal Service.
Nov 17 22:35:57 localhost systemd[1]: Starting Flush Journal to Persistent Storage...
Nov 17 22:35:57 localhost systemd[1]: Started Flush Journal to Persistent Storage.

```
