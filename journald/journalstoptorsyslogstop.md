# journalstoptorsyslogstop（ubuntu20.04）
## journalstop
### syslog
```

```
### journalctl
```
Nov 18 18:23:01 ubuntu systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 18 18:23:01 ubuntu systemd[1]: Closed Journal Socket (/dev/log).
Nov 18 18:23:12 ubuntu systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 18 18:23:12 ubuntu systemd[1]: Closed Journal Audit Socket.
Nov 18 18:23:22 ubuntu systemd[1]: Stopping Journal Service...
Nov 18 18:23:22 ubuntu systemd-journald[31214]: Journal stopped
```

### syslog
```
Nov 18 18:23:01 ubuntu systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 18 18:23:01 ubuntu systemd[1]: Closed Journal Socket (/dev/log).
Nov 18 18:23:12 ubuntu systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 18 18:23:12 ubuntu systemd[1]: Closed Journal Audit Socket.
Nov 18 18:23:22 ubuntu kernel: [  872.820421] systemd[1]: Stopping Journal Service...
Nov 18 18:23:22 ubuntu kernel: [  872.821489] systemd-journald[31214]: Received SIGTERM from PID 1 (systemd).
Nov 18 18:23:22 ubuntu kernel: [  872.826509] systemd[1]: systemd-journald.service: Succeeded.
Nov 18 18:23:22 ubuntu kernel: [  872.826886] systemd[1]: Stopped Journal Service.
Nov 18 18:23:22 ubuntu kernel: [  872.828677] systemd[1]: systemd-journald.socket: Succeeded.
Nov 18 18:23:22 ubuntu kernel: [  872.829837] systemd[1]: Closed Journal Socket.
↑以降にこの項目にNov 18 18:23:12 ubuntu systemd[1]:からの信号がいかない事を確認する。
（Nov 18 18:23:22 ubuntu kernel:からの信号は流れる）
```

rsyslogstop

### journalctl
```
```

### syslog
```
Nov 18 18:47:38 ubuntu kernel: [ 2328.470937] systemd[31306]: fprintd.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 18 18:47:38 ubuntu kernel: [ 2328.526365] systemd[1]: Started Fingerprint Authentication Daemon.
Nov 18 18:48:08 ubuntu kernel: [ 2358.513541] systemd[1]: fprintd.service: Succeeded.
Nov 18 18:48:25 ubuntu kernel: [ 2375.422193] systemd[1]: Stopping System Logging Service...

```
## journalstart (patarn 1)
### journalctl
```
Nov 18 18:54:18 ubuntu systemd[1]: Listening on Journal Audit Socket.
Nov 18 18:54:18 ubuntu systemd[1]: Listening on Journal Socket (/dev/log).
Nov 18 18:54:18 ubuntu systemd[1]: Listening on Journal Socket.
Nov 18 18:54:18 ubuntu systemd[1]: Starting Journal Service...
Nov 18 18:54:18 ubuntu systemd-journald[31374]: Journal started
Nov 18 18:54:18 ubuntu systemd-journald[31374]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 18 18:54:18 ubuntu systemd[1]: Started Journal Service.
```

### syslog
```

```
## syslog start
### journalctl
```
ov 18 18:55:16 ubuntu systemd[1]: Listening on Syslog Socket.
Nov 18 18:55:16 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 18:55:16 ubuntu rsyslogd[31380]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 18 18:55:16 ubuntu rsyslogd[31380]: rsyslogd's groupid changed to 110
Nov 18 18:55:16 ubuntu rsyslogd[31380]: rsyslogd's userid changed to 104
Nov 18 18:55:16 ubuntu rsyslogd[31380]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31380" x-info="https://www.rsyslog.com"] start
Nov 18 18:55:16 ubuntu systemd[1]: Started System Logging Service.

```

### rsyslog
```
Nov 18 18:55:16 ubuntu kernel: [ 2375.430034] systemd[1]: rsyslog.service: Succeeded.
Nov 18 18:55:16 ubuntu kernel: [ 2375.430659] systemd[1]: Stopped System Logging Service.
Nov 18 18:55:16 ubuntu kernel: [ 2443.906987] systemd[1]: syslog.socket: Succeeded.
Nov 18 18:55:16 ubuntu kernel: [ 2443.907775] systemd[1]: Closed Syslog Socket.
Nov 18 18:55:16 ubuntu kernel: [ 2728.591468] systemd[1]: Listening on Journal Audit Socket.
Nov 18 18:55:16 ubuntu kernel: [ 2728.593514] systemd[1]: Listening on Journal Socket (/dev/log).
Nov 18 18:55:16 ubuntu kernel: [ 2728.594943] systemd[1]: Listening on Journal Socket.
Nov 18 18:55:16 ubuntu kernel: [ 2728.599190] systemd[1]: Starting Journal Service...
Nov 18 18:55:16 ubuntu kernel: [ 2728.639501] systemd[1]: Started Journal Service.
Nov 18 18:55:16 ubuntu systemd[1]: Listening on Syslog Socket.
Nov 18 18:55:16 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 18:55:16 ubuntu rsyslogd: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 18 18:55:16 ubuntu rsyslogd: rsyslogd's groupid changed to 110
Nov 18 18:55:16 ubuntu rsyslogd: rsyslogd's userid changed to 104
Nov 18 18:55:16 ubuntu rsyslogd: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31380" x-info="https://www.rsyslog.com"] start
Nov 18 18:55:16 ubuntu systemd[1]: Started System Logging Service.

```

## syslog start (pataturn 2)
### journalctl
```
```

### syslog
```
Nov 18 19:00:46 ubuntu kernel: [ 2969.311651] systemd[1]: Stopping System Logging Service...
Nov 18 19:00:46 ubuntu kernel: [ 2969.313310] systemd[1]: rsyslog.service: Succeeded.
Nov 18 19:00:46 ubuntu kernel: [ 2969.313992] systemd[1]: Stopped System Logging Service.
Nov 18 19:00:46 ubuntu kernel: [ 2980.980457] systemd[1]: syslog.socket: Succeeded.
Nov 18 19:00:46 ubuntu kernel: [ 2980.981693] systemd[1]: Closed Syslog Socket.
Nov 18 19:00:46 ubuntu kernel: [ 3116.736701] systemd[1]: Listening on Syslog Socket.
Nov 18 19:00:46 ubuntu kernel: [ 3116.739827] systemd[1]: Starting System Logging Service...
Nov 18 19:00:46 ubuntu kernel: [ 3116.748515] systemd[1]: Started System Logging Service.

```
## journal start
### journalctl
```
Nov 18 19:01:23 ubuntu systemd-journald[31374]: Received SIGTERM from PID 1 (systemd).
Nov 18 19:01:23 ubuntu systemd[1]: Stopping Journal Service...
Nov 18 19:01:23 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 18 19:01:23 ubuntu systemd[1]: Stopped Journal Service.
Nov 18 19:01:23 ubuntu systemd[1]: NetworkManager-dispatcher.service: Succeeded.
Nov 18 19:01:23 ubuntu systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 18 19:01:23 ubuntu systemd[1]: Closed Journal Socket (/dev/log).
Nov 18 19:01:23 ubuntu systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 18 19:01:23 ubuntu systemd[1]: Closed Journal Audit Socket.
Nov 18 19:01:23 ubuntu systemd[1]: systemd-journald.socket: Succeeded.
Nov 18 19:01:23 ubuntu systemd[1]: Closed Journal Socket.
Nov 18 19:01:23 ubuntu systemd[1]: Stopping System Logging Service...
Nov 18 19:01:23 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 18 19:01:23 ubuntu systemd[1]: Stopped System Logging Service.
Nov 18 19:01:23 ubuntu systemd[1]: syslog.socket: Succeeded.
Nov 18 19:01:23 ubuntu systemd[1]: Closed Syslog Socket.
Nov 18 19:01:23 ubuntu systemd[1]: Listening on Syslog Socket.
Nov 18 19:01:23 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 19:01:23 ubuntu systemd[1]: Started System Logging Service.
Nov 18 19:01:23 ubuntu systemd[1]: Listening on Journal Audit Socket.
Nov 18 19:01:23 ubuntu systemd[1]: Listening on Journal Socket (/dev/log).
Nov 18 19:01:23 ubuntu systemd[1]: Listening on Journal Socket.
Nov 18 19:01:23 ubuntu systemd[1]: Starting Journal Service...
Nov 18 19:01:23 ubuntu systemd-journald[31416]: Journal started
Nov 18 19:01:23 ubuntu systemd-journald[31416]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 18 19:01:23 ubuntu systemd[1]: Started Journal Service.

```

### syslog
```
Nov 18 19:01:23 ubuntu kernel: [ 3153.482189] systemd[1]: Listening on Journal Audit Socket.
Nov 18 19:01:23 ubuntu kernel: [ 3153.482637] systemd[1]: Listening on Journal Socket (/dev/log).
Nov 18 19:01:23 ubuntu kernel: [ 3153.483236] systemd[1]: Listening on Journal Socket.
Nov 18 19:01:23 ubuntu kernel: [ 3153.492565] systemd[1]: Starting Journal Service...
Nov 18 19:01:23 ubuntu kernel: [ 3153.532788] systemd[1]: Started Journal Service.

```

### journalctl
```
```

### syslog
```
```

### journalctl
```
```

### syslog
```
```

### journalctl
```
```

### syslog
```
```

### journalctl
```
```

### syslog
```
```

### journalctl
```
```

### syslog
```
```

### journalctl
```
```

### syslog
```
```

### journalctl
```
```

### syslog
```
```

### journalctl
```
```

### syslog
```
```




