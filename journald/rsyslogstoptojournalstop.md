# ubuntu20.04
## rsyslogstop
### jounal
```
Nov 19 21:56:15 ubuntu systemd[1]: Reloading.
Nov 19 21:56:15 ubuntu systemd-rc-local-generator[26444]: /etc/rc.local is not marked executable, skipping.
Nov 19 21:56:15 ubuntu systemd[1]: Reloading.
Nov 19 21:56:16 ubuntu systemd-rc-local-generator[26479]: /etc/rc.local is not marked executable, skipping.
Nov 19 21:56:16 ubuntu systemd[1]: Reloading.
Nov 19 21:56:16 ubuntu systemd-rc-local-generator[26525]: /etc/rc.local is not marked executable, skipping.
Nov 19 21:50:08 ubuntu systemd[1]: Stopping System Logging Service...
Nov 19 21:50:08 ubuntu rsyslogd[5482]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="5482" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 19 21:50:08 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 19 21:50:08 ubuntu systemd[1]: Stopped System Logging Service.


```
### rsyslog
```
Nov 19 21:50:00 ubuntu systemd[3530]: tracker-extract.service: Succeeded.
Nov 19 21:50:08 ubuntu systemd[1]: Stopping System Logging Service...

```
## journalstop
### jounal
```
Nov 19 21:52:25 ubuntu systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 21:52:25 ubuntu systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 21:52:25 ubuntu systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 19 21:52:25 ubuntu systemd[1]: Closed Journal Audit Socket.
Nov 19 21:52:25 ubuntu systemd[1]: Stopping Flush Journal to Persistent Storage...
Nov 19 21:52:25 ubuntu systemd[1]: systemd-journal-flush.service: Succeeded.
Nov 19 21:52:25 ubuntu systemd[1]: Stopped Flush Journal to Persistent Storage.
Nov 19 21:52:25 ubuntu systemd-journald[360]: Journal stopped


```
### rsyslog(systemctl stop 
```



```
##  journal start
### jounal
```
Nov 19 21:53:42 ubuntu systemd[1]: Stopping Journal Service...
Nov 19 21:53:42 ubuntu systemd-journald[360]: Received SIGTERM from PID 1 (systemd).
Nov 19 21:53:42 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 19 21:53:42 ubuntu systemd[1]: Stopped Journal Service.
Nov 19 21:53:42 ubuntu systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 21:53:42 ubuntu systemd[1]: Closed Journal Socket.
Nov 19 21:53:42 ubuntu systemd[1]: apt-daily.service: Succeeded.
Nov 19 21:53:42 ubuntu systemd[1]: Finished Daily apt download activities.
Nov 19 21:53:42 ubuntu systemd[1]: Starting Daily apt upgrade and clean activities...
Nov 19 21:53:42 ubuntu systemd[5808]: apt-daily-upgrade.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 21:53:42 ubuntu systemd[5818]: apt-daily-upgrade.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 21:53:42 ubuntu systemd[1]: Starting PackageKit Daemon...
Nov 19 21:53:42 ubuntu systemd[5911]: packagekit.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 21:53:42 ubuntu systemd[1]: Started PackageKit Daemon.
Nov 19 21:53:42 ubuntu kernel: kauditd_printk_skb: 2 callbacks suppressed
Nov 19 21:53:42 ubuntu kernel: audit: type=1400 audit(1668923618.815:59): apparmor="STATUS" operation="profile_replace" info="same as current profile, skipping" profile="unconfined" name="/usr/lib/NetworkManager/nm-dhcp-client.action" pid=6258 comm="apparmor_parser"
Nov 19 21:53:42 ubuntu kernel: audit: type=1400 audit(1668923618.815:60): apparmor="STATUS" operation="profile_replace" info="same as current profile, skipping" profile="unconfined" name="/usr/lib/NetworkManager/nm-dhcp-helper" pid=6258 comm="apparmor_parser"
Nov 19 21:53:42 ubuntu kernel: audit: type=1400 audit(1668923618.815:61): apparmor="STATUS" operation="profile_replace" info="same as current profile, skipping" profile="unconfined" name="/usr/lib/connman/scripts/dhclient-script" pid=6258 comm="apparmor_parser"
Nov 19 21:53:42 ubuntu kernel: audit: type=1400 audit(1668923618.819:62): apparmor="STATUS" operation="profile_replace" info="same as current profile, skipping" profile="unconfined" name="/{,usr/}sbin/dhclient" pid=6258 comm="apparmor_parser"
Nov 19 21:53:42 ubuntu systemd[1]: Listening on Journal Audit Socket.
Nov 19 21:53:42 ubuntu systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 21:53:42 ubuntu systemd[1]: Listening on Journal Socket.
Nov 19 21:53:42 ubuntu systemd[1]: Starting Journal Service...
Nov 19 21:53:42 ubuntu systemd-journald[6752]: Journal started
Nov 19 21:53:42 ubuntu systemd-journald[6752]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 19 21:53:42 ubuntu systemd[1]: Started Journal Service.

```
### rsyslog
```
```

## rsyslog start
### jounal
```
Nov 19 21:54:26 ubuntu systemd[1]: Starting System Logging Service...
Nov 19 21:54:26 ubuntu rsyslogd[13808]: rsyslogd's groupid changed to 110
Nov 19 21:54:26 ubuntu systemd[1]: Started System Logging Service.
Nov 19 21:54:26 ubuntu rsyslogd[13808]: rsyslogd's userid changed to 104
Nov 19 21:54:26 ubuntu rsyslogd[13808]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="13808" x-info="https://www.rsyslog.com"] start


```
### rsyslog
```
Nov 19 21:54:26 ubuntu kernel: [  528.971143] systemd[1]: Stopping Journal Service...
Nov 19 21:54:26 ubuntu kernel: [  528.971478] systemd-journald[360]: Received SIGTERM from PID 1 (systemd).
Nov 19 21:54:26 ubuntu kernel: [  529.030178] systemd[1]: systemd-journald.service: Succeeded.
Nov 19 21:54:26 ubuntu kernel: [  529.030938] systemd[1]: Stopped Journal Service.
Nov 19 21:54:26 ubuntu kernel: [  529.033706] systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 21:54:26 ubuntu kernel: [  529.034568] systemd[1]: Closed Journal Socket.
Nov 19 21:54:26 ubuntu kernel: [  563.417959] systemd[1]: apt-daily.service: Succeeded.
Nov 19 21:54:26 ubuntu kernel: [  563.418545] systemd[1]: Finished Daily apt download activities.
Nov 19 21:54:26 ubuntu kernel: [  563.428903] systemd[1]: Starting Daily apt upgrade and clean activities...
Nov 19 21:54:26 ubuntu kernel: [  563.428946] systemd[5808]: apt-daily-upgrade.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 21:54:26 ubuntu kernel: [  563.466235] systemd[5818]: apt-daily-upgrade.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 21:54:26 ubuntu kernel: [  592.413637] systemd[1]: Starting PackageKit Daemon...
Nov 19 21:54:26 ubuntu kernel: [  592.413967] systemd[5911]: packagekit.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 21:54:26 ubuntu kernel: [  592.440313] systemd[1]: Started PackageKit Daemon.
Nov 19 21:54:26 ubuntu kernel: [  602.306488] kauditd_printk_skb: 2 callbacks suppressed
Nov 19 21:54:26 ubuntu kernel: [  602.306491] audit: type=1400 audit(1668923618.815:59): apparmor="STATUS" operation="profile_replace" info="same as current profile, skipping" profile="unconfined" name="/usr/lib/NetworkManager/nm-dhcp-client.action" pid=6258 comm="apparmor_parser"
Nov 19 21:54:26 ubuntu kernel: [  602.307729] audit: type=1400 audit(1668923618.815:60): apparmor="STATUS" operation="profile_replace" info="same as current profile, skipping" profile="unconfined" name="/usr/lib/NetworkManager/nm-dhcp-helper" pid=6258 comm="apparmor_parser"
Nov 19 21:54:26 ubuntu kernel: [  602.308943] audit: type=1400 audit(1668923618.815:61): apparmor="STATUS" operation="profile_replace" info="same as current profile, skipping" profile="unconfined" name="/usr/lib/connman/scripts/dhclient-script" pid=6258 comm="apparmor_parser"
Nov 19 21:54:26 ubuntu kernel: [  602.311375] audit: type=1400 audit(1668923618.819:62): apparmor="STATUS" operation="profile_replace" info="same as current profile, skipping" profile="unconfined" name="/{,usr/}sbin/dhclient" pid=6258 comm="apparmor_parser"
Nov 19 21:54:26 ubuntu kernel: [  605.443614] systemd[1]: Listening on Journal Audit Socket.
Nov 19 21:54:26 ubuntu kernel: [  605.443828] systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 21:54:26 ubuntu kernel: [  605.444044] systemd[1]: Listening on Journal Socket.
Nov 19 21:54:26 ubuntu kernel: [  605.461027] systemd[1]: Starting Journal Service...
Nov 19 21:54:26 ubuntu kernel: [  605.511832] systemd[1]: Started Journal Service.
Nov 19 21:54:26 ubuntu rsyslogd: rsyslogd's groupid changed to 110
Nov 19 21:54:26 ubuntu systemd[1]: Started System Logging Service.
Nov 19 21:54:26 ubuntu rsyslogd: rsyslogd's userid changed to 104
Nov 19 21:54:26 ubuntu rsyslogd: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="13808" x-info="https://www.rsyslog.com"] start

```
# rsyslogaからstart
## rsyslog strat

### jounal
```
```
### rsyslog
```
Nov 18 22:10:21 ubuntu kernel: [ 5583.165257] systemd[1]: Stopping Journal Service...
Nov 18 22:10:21 ubuntu kernel: [ 5583.165435] systemd-journald[31764]: Received SIGTERM from PID 1 (systemd).
Nov 18 22:10:21 ubuntu kernel: [ 5583.171530] systemd[1]: systemd-journald.service: Succeeded.
Nov 18 22:10:21 ubuntu kernel: [ 5583.175500] systemd[1]: Stopped Journal Service.
Nov 18 22:10:21 ubuntu kernel: [ 5583.181951] systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 18 22:10:21 ubuntu kernel: [ 5583.182288] systemd[1]: Closed Journal Socket (/dev/log).
Nov 18 22:10:21 ubuntu kernel: [ 5583.188360] systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 18 22:10:21 ubuntu kernel: [ 5583.188839] systemd[1]: Closed Journal Audit Socket.
Nov 18 22:10:21 ubuntu kernel: [ 5583.200126] systemd[1]: systemd-journald.socket: Succeeded.
Nov 18 22:10:21 ubuntu kernel: [ 5583.200492] systemd[1]: Closed Journal Socket.
Nov 18 22:10:21 ubuntu kernel: [ 5678.050005] systemd[1]: Listening on Syslog Socket.
Nov 18 22:10:21 ubuntu kernel: [ 5678.056312] systemd[1]: Starting System Logging Service...
Nov 18 22:10:21 ubuntu kernel: [ 5678.061613] systemd[1]: Started System Logging Service.

```
journalstart
### jounal
```
Nov 18 22:10:59 ubuntu systemd[1]: Stopping Journal Service...
Nov 18 22:10:59 ubuntu systemd-journald[31764]: Received SIGTERM from PID 1 (systemd).
Nov 18 22:10:59 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 18 22:10:59 ubuntu systemd[1]: Stopped Journal Service.
Nov 18 22:10:59 ubuntu systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 18 22:10:59 ubuntu systemd[1]: Closed Journal Socket (/dev/log).
Nov 18 22:10:59 ubuntu systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 18 22:10:59 ubuntu systemd[1]: Closed Journal Audit Socket.
Nov 18 22:10:59 ubuntu systemd[1]: systemd-journald.socket: Succeeded.
Nov 18 22:10:59 ubuntu systemd[1]: Closed Journal Socket.
Nov 18 22:10:59 ubuntu systemd[1]: Listening on Syslog Socket.
Nov 18 22:10:59 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 22:10:59 ubuntu systemd[1]: Started System Logging Service.
Nov 18 22:10:59 ubuntu systemd[1]: Listening on Journal Audit Socket.
Nov 18 22:10:59 ubuntu systemd[1]: Listening on Journal Socket (/dev/log).
Nov 18 22:10:59 ubuntu systemd[1]: Listening on Journal Socket.
Nov 18 22:10:59 ubuntu systemd[1]: Starting Journal Service...
Nov 18 22:10:59 ubuntu systemd-journald[31805]: Journal started
Nov 18 22:10:59 ubuntu systemd-journald[31805]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 18 22:10:59 ubuntu systemd[1]: Started Journal Service.

```
### rsyslog
```
Nov 18 22:10:59 ubuntu kernel: [ 5715.366808] systemd[1]: Listening on Journal Audit Socket.
Nov 18 22:10:59 ubuntu kernel: [ 5715.367162] systemd[1]: Listening on Journal Socket (/dev/log).
Nov 18 22:10:59 ubuntu kernel: [ 5715.367440] systemd[1]: Listening on Journal Socket.
Nov 18 22:10:59 ubuntu kernel: [ 5715.373113] systemd[1]: Starting Journal Service...
Nov 18 22:10:59 ubuntu kernel: [ 5715.412159] systemd[1]: Started Journal Service.

```
