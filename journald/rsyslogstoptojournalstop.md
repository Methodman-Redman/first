# ubuntu20.04
## rsyslogstop
### jounal
```
Nov 19 23:46:47 ubuntu systemd[1]: Reloading.
Nov 19 23:46:48 ubuntu systemd-rc-local-generator[31618]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:46:48 ubuntu systemd[1]: Reloading.
Nov 19 23:46:48 ubuntu systemd-rc-local-generator[31642]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:46:48 ubuntu systemd[1]: Reloading.
Nov 19 23:46:48 ubuntu systemd-rc-local-generator[31664]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:46:52 ubuntu systemd[1]: Stopping System Logging Service...
Nov 19 23:46:52 ubuntu rsyslogd[31440]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31440" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 19 23:46:52 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 19 23:46:52 ubuntu systemd[1]: Stopped System Logging Service.
Nov 19 23:46:58 ubuntu systemd[1]: fprintd.service: Succeeded.


```
### rsyslog
```
Nov 19 23:46:47 ubuntu systemd[1]: Reloading.
Nov 19 23:46:48 ubuntu kernel: [ 2524.441119] systemd-rc-local-generator[31618]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:46:48 ubuntu kernel: [ 2524.723578] systemd-rc-local-generator[31642]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:46:48 ubuntu kernel: [ 2525.012329] systemd-rc-local-generator[31664]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:46:48 ubuntu systemd[1]: message repeated 2 times: [ Reloading.]


```
## journalstop
### jounal
```
Nov 19 23:47:51 ubuntu systemd[1]: Stopping Journal Service...
Nov 19 23:47:51 ubuntu systemd-journald[31363]: Journal stopped
```
### rsys
```
```
# jour stat to rsys start
##  journal start
### jounal
```
ov 19 23:50:06 ubuntu systemd-journald[31363]: Received SIGTERM from PID 1 (systemd).
Nov 19 23:50:06 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 19 23:50:06 ubuntu systemd[1]: Stopped Journal Service.
Nov 19 23:50:06 ubuntu systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 19 23:50:06 ubuntu systemd[1]: Closed Journal Audit Socket.
Nov 19 23:50:06 ubuntu systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 23:50:06 ubuntu systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 23:50:06 ubuntu systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 23:50:06 ubuntu systemd[1]: Closed Journal Socket.
Nov 19 23:50:06 ubuntu systemd[1]: Starting Network Manager Script Dispatcher Service...
Nov 19 23:50:06 ubuntu systemd[31684]: NetworkManager-dispatcher.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 23:50:06 ubuntu systemd[1]: Started Network Manager Script Dispatcher Service.
Nov 19 23:50:06 ubuntu systemd[1]: Listening on Journal Audit Socket.
Nov 19 23:50:06 ubuntu systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 23:50:06 ubuntu systemd[1]: Listening on Journal Socket.
Nov 19 23:50:06 ubuntu systemd[1]: Starting Journal Service...
Nov 19 23:50:06 ubuntu systemd-journald[31690]: Journal started
Nov 19 23:50:06 ubuntu systemd-journald[31690]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 19 23:50:06 ubuntu systemd[1]: Started Journal Service.


```
### rsyslog
```
```

## rsyslog start
### jounal
```
Nov 19 23:50:52 ubuntu systemd[1]: Reloading.
Nov 19 23:50:53 ubuntu systemd-rc-local-generator[31711]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:50:53 ubuntu systemd[1]: Reloading.
Nov 19 23:50:53 ubuntu systemd-rc-local-generator[31735]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:50:53 ubuntu systemd[1]: Reloading.
Nov 19 23:50:53 ubuntu systemd-rc-local-generator[31757]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:51:09 ubuntu systemd[1]: Starting System Logging Service...
Nov 19 23:51:09 ubuntu rsyslogd[31767]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 19 23:51:09 ubuntu rsyslogd[31767]: rsyslogd's groupid changed to 110
Nov 19 23:51:09 ubuntu rsyslogd[31767]: rsyslogd's userid changed to 104
Nov 19 23:51:09 ubuntu rsyslogd[31767]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31767" x-info="https://www.rsyslog.com"] start
Nov 19 23:51:09 ubuntu systemd[1]: Started System Logging Service.

```
### rsyslog
```
Nov 19 23:46:52 ubuntu systemd[1]: Stopping System Logging Service...
Nov 19 23:46:52 ubuntu rsyslogd: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31440" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 19 23:46:52 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 19 23:46:52 ubuntu systemd[1]: Stopped System Logging Service.
Nov 19 23:46:58 ubuntu systemd[1]: fprintd.service: Succeeded.
Nov 19 23:50:09 ubuntu systemd[1]: NetworkManager-dispatcher.service: Succeeded.
Nov 19 23:50:52 ubuntu systemd[1]: Reloading.
Nov 19 23:50:53 ubuntu systemd[1]: message repeated 2 times: [ Reloading.]
Nov 19 23:51:09 ubuntu systemd[1]: Starting System Logging Service...
Nov 19 23:51:09 ubuntu rsyslogd: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 19 23:51:09 ubuntu rsyslogd: rsyslogd's groupid changed to 110
Nov 19 23:51:09 ubuntu rsyslogd: rsyslogd's userid changed to 104
Nov 19 23:51:09 ubuntu rsyslogd: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31767" x-info="https://www.rsyslog.com"] start
Nov 19 23:51:09 ubuntu kernel: [ 2587.544392] systemd[1]: Stopping Journal Service...
Nov 19 23:51:09 ubuntu kernel: [ 2587.544898] systemd-journald[31363]: Received SIGTERM from PID 1 (systemd).
Nov 19 23:51:09 ubuntu kernel: [ 2587.549507] systemd[1]: systemd-journald.service: Succeeded.
Nov 19 23:51:09 ubuntu kernel: [ 2587.549946] systemd[1]: Stopped Journal Service.
Nov 19 23:51:09 ubuntu kernel: [ 2587.556994] systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 19 23:51:09 ubuntu kernel: [ 2587.557292] systemd[1]: Closed Journal Audit Socket.
Nov 19 23:51:09 ubuntu kernel: [ 2587.566023] systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 23:51:09 ubuntu kernel: [ 2587.566374] systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 23:51:09 ubuntu kernel: [ 2587.572844] systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 23:51:09 ubuntu kernel: [ 2587.573143] systemd[1]: Closed Journal Socket.
Nov 19 23:51:09 ubuntu kernel: [ 2715.628556] systemd[1]: Starting Network Manager Script Dispatcher Service...
Nov 19 23:51:09 ubuntu kernel: [ 2715.628965] systemd[31684]: NetworkManager-dispatcher.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 23:51:09 ubuntu kernel: [ 2715.638000] systemd[1]: Started Network Manager Script Dispatcher Service.
Nov 19 23:51:09 ubuntu kernel: [ 2723.051224] systemd[1]: Listening on Journal Audit Socket.
Nov 19 23:51:09 ubuntu kernel: [ 2723.051534] systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 23:51:09 ubuntu kernel: [ 2723.051918] systemd[1]: Listening on Journal Socket.
Nov 19 23:51:09 ubuntu kernel: [ 2723.059126] systemd[1]: Starting Journal Service...
Nov 19 23:51:09 ubuntu kernel: [ 2723.090811] systemd[1]: Started Journal Service.
Nov 19 23:51:09 ubuntu kernel: [ 2769.408729] systemd-rc-local-generator[31711]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:51:09 ubuntu kernel: [ 2769.693186] systemd-rc-local-generator[31735]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:51:09 ubuntu kernel: [ 2769.930369] systemd-rc-local-generator[31757]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:51:09 ubuntu systemd[1]: Started System Logging Service.
```

# rsyslogaからstart
## rsyslog strat

### jounal
```
```
### rsyslog
```
Nov 19 23:52:12 ubuntu systemd[1]: Stopping System Logging Service...
Nov 19 23:52:12 ubuntu rsyslogd: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31767" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 19 23:52:12 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 19 23:52:12 ubuntu systemd[1]: Stopped System Logging Service.
Nov 19 23:52:45 ubuntu kernel: [ 2853.068637] systemd[1]: Stopping Journal Service...
Nov 19 23:52:45 ubuntu kernel: [ 2853.068799] systemd-journald[31690]: Received SIGTERM from PID 1 (systemd).
Nov 19 23:52:45 ubuntu kernel: [ 2853.074894] systemd[1]: systemd-journald.service: Succeeded.
Nov 19 23:52:45 ubuntu kernel: [ 2853.075836] systemd[1]: Stopped Journal Service.
Nov 19 23:52:45 ubuntu kernel: [ 2853.087365] systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 19 23:52:45 ubuntu kernel: [ 2853.087723] systemd[1]: Closed Journal Audit Socket.
Nov 19 23:52:45 ubuntu kernel: [ 2853.093997] systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 23:52:45 ubuntu kernel: [ 2853.094342] systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 23:52:45 ubuntu kernel: [ 2853.102173] systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 23:52:45 ubuntu kernel: [ 2853.102618] systemd[1]: Closed Journal Socket.
Nov 19 23:52:45 ubuntu kernel: [ 2872.990835] systemd[1]: Reloading.
Nov 19 23:52:45 ubuntu kernel: [ 2873.066688] systemd-rc-local-generator[31876]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:52:45 ubuntu kernel: [ 2873.238495] systemd[1]: Reloading.
Nov 19 23:52:45 ubuntu kernel: [ 2873.341942] systemd-rc-local-generator[31900]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:52:45 ubuntu kernel: [ 2873.474659] systemd[1]: Reloading.
Nov 19 23:52:45 ubuntu kernel: [ 2873.563091] systemd-rc-local-generator[31921]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:52:45 ubuntu kernel: [ 2881.473839] systemd[1]: Starting System Logging Service...
Nov 19 23:52:45 ubuntu kernel: [ 2881.480150] systemd[1]: Started System Logging Service.


```
journalstart
### jounal
```
Nov 19 23:53:08 ubuntu systemd[1]: Stopping Journal Service...
Nov 19 23:53:08 ubuntu systemd-journald[31690]: Received SIGTERM from PID 1 (systemd).
Nov 19 23:53:08 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 19 23:53:08 ubuntu systemd[1]: Stopped Journal Service.
Nov 19 23:53:08 ubuntu systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 19 23:53:08 ubuntu systemd[1]: Closed Journal Audit Socket.
Nov 19 23:53:08 ubuntu systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 23:53:08 ubuntu systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 23:53:08 ubuntu systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 23:53:08 ubuntu systemd[1]: Closed Journal Socket.
Nov 19 23:53:08 ubuntu systemd[1]: Reloading.
Nov 19 23:53:08 ubuntu systemd-rc-local-generator[31876]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:53:08 ubuntu systemd[1]: Reloading.
Nov 19 23:53:08 ubuntu systemd-rc-local-generator[31900]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:53:08 ubuntu systemd[1]: Reloading.
Nov 19 23:53:08 ubuntu systemd-rc-local-generator[31921]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:53:08 ubuntu systemd[1]: Starting System Logging Service...
Nov 19 23:53:08 ubuntu systemd[1]: Started System Logging Service.
Nov 19 23:53:08 ubuntu systemd[1]: Listening on Journal Audit Socket.
Nov 19 23:53:08 ubuntu systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 23:53:08 ubuntu systemd[1]: Listening on Journal Socket.
Nov 19 23:53:08 ubuntu systemd[1]: Starting Journal Service...
Nov 19 23:53:08 ubuntu systemd-journald[31936]: Journal started
Nov 19 23:53:08 ubuntu systemd-journald[31936]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 19 23:53:08 ubuntu systemd[1]: Started Journal Service.


```
### rsyslog
```
Nov 19 23:52:12 ubuntu systemd[1]: Stopping System Logging Service...
Nov 19 23:52:12 ubuntu rsyslogd: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31767" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 19 23:52:12 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 19 23:52:12 ubuntu systemd[1]: Stopped System Logging Service.
Nov 19 23:52:45 ubuntu kernel: [ 2853.068637] systemd[1]: Stopping Journal Service...
Nov 19 23:52:45 ubuntu kernel: [ 2853.068799] systemd-journald[31690]: Received SIGTERM from PID 1 (systemd).
Nov 19 23:52:45 ubuntu kernel: [ 2853.074894] systemd[1]: systemd-journald.service: Succeeded.
Nov 19 23:52:45 ubuntu kernel: [ 2853.075836] systemd[1]: Stopped Journal Service.
Nov 19 23:52:45 ubuntu kernel: [ 2853.087365] systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 19 23:52:45 ubuntu kernel: [ 2853.087723] systemd[1]: Closed Journal Audit Socket.
Nov 19 23:52:45 ubuntu kernel: [ 2853.093997] systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 23:52:45 ubuntu kernel: [ 2853.094342] systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 23:52:45 ubuntu kernel: [ 2853.102173] systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 23:52:45 ubuntu kernel: [ 2853.102618] systemd[1]: Closed Journal Socket.
Nov 19 23:52:45 ubuntu kernel: [ 2872.990835] systemd[1]: Reloading.
Nov 19 23:52:45 ubuntu kernel: [ 2873.066688] systemd-rc-local-generator[31876]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:52:45 ubuntu kernel: [ 2873.238495] systemd[1]: Reloading.
Nov 19 23:52:45 ubuntu kernel: [ 2873.341942] systemd-rc-local-generator[31900]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:52:45 ubuntu kernel: [ 2873.474659] systemd[1]: Reloading.
Nov 19 23:52:45 ubuntu kernel: [ 2873.563091] systemd-rc-local-generator[31921]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:52:45 ubuntu kernel: [ 2881.473839] systemd[1]: Starting System Logging Service...
Nov 19 23:52:45 ubuntu kernel: [ 2881.480150] systemd[1]: Started System Logging Service.
Nov 19 23:53:08 ubuntu kernel: [ 2905.066003] systemd[1]: Listening on Journal Audit Socket.
Nov 19 23:53:08 ubuntu kernel: [ 2905.066270] systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 23:53:08 ubuntu kernel: [ 2905.066538] systemd[1]: Listening on Journal Socket.
Nov 19 23:53:08 ubuntu kernel: [ 2905.072577] systemd[1]: Starting Journal Service...
Nov 19 23:53:08 ubuntu kernel: [ 2905.099675] systemd[1]: Started Journal Service.


```
