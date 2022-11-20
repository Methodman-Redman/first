# journalstoptorsyslogstop（ubuntu20.04）
## journalstop

### journalctl
```
Nov 19 22:54:12 ubuntu systemd[1]: Stopping Flush Journal to Persistent Storage...
Nov 19 22:54:12 ubuntu systemd[1]: systemd-journal-flush.service: Succeeded.
Nov 19 22:54:12 ubuntu systemd[1]: Stopped Flush Journal to Persistent Storage.
Nov 19 22:54:12 ubuntu systemd-journald[360]: Journal stopped

```

### syslog
```
Nov 19 22:54:12 ubuntu systemd[1]: Stopping Flush Journal to Persistent Storage...
Nov 19 22:54:12 ubuntu systemd[1]: systemd-journal-flush.service: Succeeded.
Nov 19 22:54:12 ubuntu systemd[1]: Stopped Flush Journal to Persistent Storage.
Nov 19 22:54:12 ubuntu kernel: [  199.167571] systemd-journald[360]: Received SIGTERM from PID 1 (systemd).
Nov 19 22:54:12 ubuntu kernel: [  199.174839] systemd[1]: Stopping Journal Service...
Nov 19 22:54:12 ubuntu kernel: [  199.208402] systemd[1]: systemd-journald.service: Succeeded.
Nov 19 22:54:12 ubuntu kernel: [  199.209904] systemd[1]: Stopped Journal Service.
Nov 19 22:54:12 ubuntu kernel: [  199.224888] systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 19 22:54:12 ubuntu kernel: [  199.226698] systemd[1]: Closed Journal Audit Socket.
Nov 19 22:54:12 ubuntu kernel: [  199.243836] systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 22:54:12 ubuntu kernel: [  199.245092] systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 22:54:12 ubuntu kernel: [  199.262364] systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 22:54:12 ubuntu kernel: [  199.263784] systemd[1]: Closed Journal Socket.

↑以降にこの項目にNov 18 18:23:12 ubuntu systemd[1]:からの信号がいかない事を確認する。
（Nov 18 18:23:22 ubuntu kernel:からの信号は流れる）
```

## rsyslogstop

### journalctl
```
```

### syslog
```
Nov 19 23:19:00 ubuntu kernel: [  856.642870] systemd[1]: Reloading.
Nov 19 23:19:00 ubuntu kernel: [  856.781404] systemd-rc-local-generator[24769]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:19:00 ubuntu kernel: [  857.031245] systemd[1]: Reloading.
Nov 19 23:19:00 ubuntu kernel: [  857.151693] systemd-rc-local-generator[24855]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:19:00 ubuntu kernel: [  857.378844] systemd[1]: Reloading.
Nov 19 23:19:01 ubuntu kernel: [  857.536630] systemd-rc-local-generator[25028]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:19:01 ubuntu kernel: [  857.737394] systemd[1]: Starting Ubuntu Advantage Timer for running repeated jobs...
Nov 19 23:19:01 ubuntu kernel: [  857.737536] systemd[25137]: ua-timer.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 23:19:01 ubuntu kernel: [  858.149322] systemd[1]: ua-timer.service: Succeeded.
Nov 19 23:19:01 ubuntu kernel: [  858.149644] systemd[1]: Finished Ubuntu Advantage Timer for running repeated jobs.
Nov 19 23:19:07 ubuntu kernel: [  864.011945] systemd[1]: Stopping System Logging Service...



```
## journalstart (patarn 1)
### journalctl(kernel　iventの状況で...)
```
Nov 19 23:20:04 ubuntu systemd-journald[360]: Received SIGTERM from PID 1 (systemd).
Nov 19 23:20:04 ubuntu systemd[1]: Stopping Journal Service...
Nov 19 23:20:04 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 19 23:20:04 ubuntu systemd[1]: Stopped Journal Service.
Nov 19 23:20:04 ubuntu systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 19 23:20:04 ubuntu systemd[1]: Closed Journal Audit Socket.
Nov 19 23:20:04 ubuntu systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 23:20:04 ubuntu systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 23:20:04 ubuntu systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 23:20:04 ubuntu systemd[1]: Closed Journal Socket.
Nov 19 23:20:04 ubuntu systemd[1]: fprintd.service: Succeeded.
Nov 19 23:20:04 ubuntu systemd[1]: Reloading.
Nov 19 23:20:04 ubuntu systemd-rc-local-generator[24769]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:20:04 ubuntu systemd[1]: Reloading.
Nov 19 23:20:04 ubuntu systemd-rc-local-generator[24855]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:20:04 ubuntu systemd[1]: Reloading.
Nov 19 23:20:04 ubuntu systemd-rc-local-generator[25028]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:20:04 ubuntu systemd[1]: Starting Ubuntu Advantage Timer for running repeated jobs...
Nov 19 23:20:04 ubuntu systemd[25137]: ua-timer.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 23:20:04 ubuntu systemd[1]: ua-timer.service: Succeeded.
Nov 19 23:20:04 ubuntu systemd[1]: Finished Ubuntu Advantage Timer for running repeated jobs.
Nov 19 23:20:04 ubuntu systemd[1]: Stopping System Logging Service...
Nov 19 23:20:04 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 19 23:20:04 ubuntu systemd[1]: Stopped System Logging Service.
Nov 19 23:20:04 ubuntu systemd[1]: apt-daily-upgrade.service: Succeeded.
Nov 19 23:20:04 ubuntu systemd[1]: Finished Daily apt upgrade and clean activities.
Nov 19 23:20:04 ubuntu systemd[1]: Starting Cleanup of Temporary Directories...
Nov 19 23:20:04 ubuntu systemd[30980]: systemd-tmpfiles-clean.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 23:20:04 ubuntu systemd[1]: systemd-tmpfiles-clean.service: Succeeded.
Nov 19 23:20:04 ubuntu systemd[1]: Finished Cleanup of Temporary Directories.
Nov 19 23:20:04 ubuntu systemd[1]: Starting Network Manager Script Dispatcher Service...
Nov 19 23:20:04 ubuntu systemd[30981]: NetworkManager-dispatcher.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 23:20:04 ubuntu systemd[1]: Started Network Manager Script Dispatcher Service.
Nov 19 23:20:04 ubuntu systemd[1]: Listening on Journal Audit Socket.
Nov 19 23:20:04 ubuntu systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 23:20:04 ubuntu systemd[1]: Listening on Journal Socket.
Nov 19 23:20:04 ubuntu systemd[1]: Starting Journal Service...
Nov 19 23:20:04 ubuntu systemd-journald[30987]: Journal started
Nov 19 23:20:04 ubuntu systemd-journald[30987]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 19 23:20:04 ubuntu systemd[1]: Started Journal Service.
Nov 19 23:20:09 ubuntu systemd[1]: NetworkManager-dispatcher.service: Succeeded.

```

### syslog
```

```
## syslog start
### journalctl
```
Nov 19 23:20:41 ubuntu systemd[1]: Reloading.
Nov 19 23:20:41 ubuntu systemd-rc-local-generator[31010]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:20:41 ubuntu systemd[1]: Reloading.
Nov 19 23:20:41 ubuntu systemd-rc-local-generator[31033]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:20:41 ubuntu systemd[1]: Reloading.
Nov 19 23:20:42 ubuntu systemd-rc-local-generator[31054]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:20:51 ubuntu systemd[1]: Starting System Logging Service...
Nov 19 23:20:51 ubuntu systemd[1]: Started System Logging Service.
Nov 19 23:20:51 ubuntu rsyslogd[31063]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 19 23:20:51 ubuntu rsyslogd[31063]: rsyslogd's groupid changed to 110
Nov 19 23:20:51 ubuntu rsyslogd[31063]: rsyslogd's userid changed to 104
Nov 19 23:20:51 ubuntu rsyslogd[31063]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31063" x-info="https://www.rsyslog.com"] start

```

### rsyslog
```
Nov 19 23:20:09 ubuntu systemd[1]: NetworkManager-dispatcher.service: Succeeded.
Nov 19 23:20:41 ubuntu systemd[1]: Reloading.
Nov 19 23:20:41 ubuntu systemd[1]: message repeated 2 times: [ Reloading.]
Nov 19 23:20:51 ubuntu systemd[1]: Starting System Logging Service...
Nov 19 23:20:51 ubuntu systemd[1]: Started System Logging Service.
Nov 19 23:20:51 ubuntu kernel: [  864.018195] systemd[1]: rsyslog.service: Succeeded.
Nov 19 23:20:51 ubuntu kernel: [  864.018559] systemd[1]: Stopped System Logging Service.
Nov 19 23:20:51 ubuntu kernel: [  881.976420] systemd[1]: apt-daily-upgrade.service: Succeeded.
Nov 19 23:20:51 ubuntu kernel: [  881.976799] systemd[1]: Finished Daily apt upgrade and clean activities.
Nov 19 23:20:51 ubuntu kernel: [  900.437365] systemd[1]: Starting Cleanup of Temporary Directories...
Nov 19 23:20:51 ubuntu kernel: [  900.440471] systemd[30980]: systemd-tmpfiles-clean.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 23:20:51 ubuntu kernel: [  900.493452] systemd[1]: systemd-tmpfiles-clean.service: Succeeded.
Nov 19 23:20:51 ubuntu kernel: [  900.493793] systemd[1]: Finished Cleanup of Temporary Directories.
Nov 19 23:20:51 ubuntu kernel: [  915.655121] systemd[1]: Starting Network Manager Script Dispatcher Service...
Nov 19 23:20:51 ubuntu kernel: [  915.655948] systemd[30981]: NetworkManager-dispatcher.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 19 23:20:51 ubuntu kernel: [  915.665648] systemd[1]: Started Network Manager Script Dispatcher Service.
Nov 19 23:20:51 ubuntu kernel: [  920.591260] systemd[1]: Listening on Journal Audit Socket.
Nov 19 23:20:51 ubuntu kernel: [  920.591540] systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 23:20:51 ubuntu kernel: [  920.591822] systemd[1]: Listening on Journal Socket.
Nov 19 23:20:51 ubuntu kernel: [  920.596837] systemd[1]: Starting Journal Service...
Nov 19 23:20:51 ubuntu kernel: [  920.672830] systemd[1]: Started Journal Service.
Nov 19 23:20:51 ubuntu kernel: [  957.878929] systemd-rc-local-generator[31010]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:20:51 ubuntu kernel: [  958.120752] systemd-rc-local-generator[31033]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:20:51 ubuntu kernel: [  958.416015] systemd-rc-local-generator[31054]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:20:51 ubuntu rsyslogd: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 19 23:20:51 ubuntu rsyslogd: rsyslogd's groupid changed to 110
Nov 19 23:20:51 ubuntu rsyslogd: rsyslogd's userid changed to 104
Nov 19 23:20:51 ubuntu rsyslogd: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31063" x-info="https://www.rsyslog.com"] start


```

## syslog start (pataturn 2)
### journalctl
```
```

### syslog
```
Nov 19 23:23:04 ubuntu kernel: [ 1077.424519] systemd[1]: rsyslog.service: Succeeded.
Nov 19 23:23:04 ubuntu kernel: [ 1077.424948] systemd[1]: Stopped System Logging Service.
Nov 19 23:23:04 ubuntu kernel: [ 1096.300275] systemd[1]: Reloading.
Nov 19 23:23:04 ubuntu kernel: [ 1096.390695] systemd-rc-local-generator[31205]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:23:04 ubuntu kernel: [ 1096.538115] systemd[1]: Reloading.
Nov 19 23:23:04 ubuntu kernel: [ 1096.631654] systemd-rc-local-generator[31228]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:23:04 ubuntu kernel: [ 1096.770451] systemd[1]: Reloading.
Nov 19 23:23:04 ubuntu kernel: [ 1096.881404] systemd-rc-local-generator[31249]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:23:04 ubuntu kernel: [ 1101.175809] systemd[1]: Starting System Logging Service...
Nov 19 23:23:04 ubuntu kernel: [ 1101.180878] systemd[1]: Started System Logging Service.


```
## journal start
### journalctl
```
Nov 19 23:23:31 ubuntu systemd-journald[30987]: Received SIGTERM from PID 1 (systemd).
Nov 19 23:23:31 ubuntu systemd[1]: Stopping Journal Service...
Nov 19 23:23:31 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 19 23:23:31 ubuntu systemd[1]: Stopped Journal Service.
Nov 19 23:23:31 ubuntu systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 19 23:23:31 ubuntu systemd[1]: Closed Journal Audit Socket.
Nov 19 23:23:31 ubuntu systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 23:23:31 ubuntu systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 23:23:31 ubuntu systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 23:23:31 ubuntu systemd[1]: Closed Journal Socket.
Nov 19 23:23:31 ubuntu systemd[1]: Reloading.
Nov 19 23:23:31 ubuntu systemd-rc-local-generator[31129]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:23:31 ubuntu systemd[1]: Reloading.
Nov 19 23:23:31 ubuntu systemd-rc-local-generator[31153]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:23:31 ubuntu systemd[1]: Reloading.
Nov 19 23:23:31 ubuntu systemd-rc-local-generator[31174]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:23:31 ubuntu systemd[1]: Stopping System Logging Service...
Nov 19 23:23:31 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 19 23:23:31 ubuntu systemd[1]: Stopped System Logging Service.
Nov 19 23:23:31 ubuntu systemd[1]: Reloading.
Nov 19 23:23:31 ubuntu systemd-rc-local-generator[31205]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:23:31 ubuntu systemd[1]: Reloading.
Nov 19 23:23:31 ubuntu systemd-rc-local-generator[31228]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:23:31 ubuntu systemd[1]: Reloading.
Nov 19 23:23:31 ubuntu systemd-rc-local-generator[31249]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:23:31 ubuntu systemd[1]: Starting System Logging Service...
Nov 19 23:23:31 ubuntu systemd[1]: Started System Logging Service.
Nov 19 23:23:31 ubuntu systemd[1]: Listening on Journal Audit Socket.
Nov 19 23:23:31 ubuntu systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 23:23:31 ubuntu systemd[1]: Listening on Journal Socket.
Nov 19 23:23:31 ubuntu systemd[1]: Starting Journal Service...
Nov 19 23:23:31 ubuntu systemd-journald[31265]: Journal started
Nov 19 23:23:31 ubuntu systemd-journald[31265]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 19 23:23:31 ubuntu systemd[1]: Started Journal Service.

```

### syslog
```
Nov 19 23:23:04 ubuntu kernel: [ 1077.424519] systemd[1]: rsyslog.service: Succeeded.
Nov 19 23:23:04 ubuntu kernel: [ 1077.424948] systemd[1]: Stopped System Logging Service.
Nov 19 23:23:04 ubuntu kernel: [ 1096.300275] systemd[1]: Reloading.
Nov 19 23:23:04 ubuntu kernel: [ 1096.390695] systemd-rc-local-generator[31205]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:23:04 ubuntu kernel: [ 1096.538115] systemd[1]: Reloading.
Nov 19 23:23:04 ubuntu kernel: [ 1096.631654] systemd-rc-local-generator[31228]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:23:04 ubuntu kernel: [ 1096.770451] systemd[1]: Reloading.
Nov 19 23:23:04 ubuntu kernel: [ 1096.881404] systemd-rc-local-generator[31249]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:23:04 ubuntu kernel: [ 1101.175809] systemd[1]: Starting System Logging Service...
Nov 19 23:23:04 ubuntu kernel: [ 1101.180878] systemd[1]: Started System Logging Service.
Nov 19 23:23:31 ubuntu kernel: [ 1127.460578] systemd[1]: Listening on Journal Audit Socket.
Nov 19 23:23:31 ubuntu kernel: [ 1127.461097] systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 23:23:31 ubuntu kernel: [ 1127.461616] systemd[1]: Listening on Journal Socket.
Nov 19 23:23:31 ubuntu kernel: [ 1127.466474] systemd[1]: Starting Journal Service...
Nov 19 23:23:31 ubuntu kernel: [ 1127.498735] systemd[1]: Started Journal Service.


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




