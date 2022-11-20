# journal status change

## jounal chage + restart

### jounal
```
Nov 18 22:14:04 ubuntu systemd-journald[31805]: Journal stopped

```
### rsyslog
```
Nov 18 22:14:04 ubuntu kernel: [ 5900.986051] systemd-journald[31805]: Received SIGTERM from PID 1 (systemd).
Nov 18 22:14:04 ubuntu kernel: [ 5900.988948] systemd[1]: Stopping Journal Service...
Nov 18 22:14:04 ubuntu kernel: [ 5900.993370] systemd[1]: systemd-journald.service: Succeeded.
Nov 18 22:14:04 ubuntu kernel: [ 5900.995460] systemd[1]: Stopped Journal Service.
Nov 18 22:14:04 ubuntu kernel: [ 5901.001013] systemd[1]: Starting Journal Service...
Nov 18 22:14:04 ubuntu kernel: [ 5901.035926] systemd[1]: Started Journal Service.

```

## rsyslog stop
### jounal
```
何も出ない
```
### rsyslog
```
何も出ない
```

# rsysから復旧
## rsys start
### jounal
```
何も出ない
```
### rsyslog
```
Nov 19 23:32:07 ubuntu kernel: [ 1643.629065] systemd-rc-local-generator[31303]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:32:07 ubuntu kernel: [ 1643.959541] systemd-rc-local-generator[31327]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:32:07 ubuntu kernel: [ 1644.222967] systemd-rc-local-generator[31350]: /etc/rc.local is not marked executable, skipping.

```

## journal change restart
### jounal
```
Nov 19 23:33:05 ubuntu systemd[1]: Stopping Journal Service...
Nov 19 23:33:05 ubuntu systemd-journald[31282]: Received SIGTERM from PID 1 (systemd).
Nov 19 23:33:05 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 19 23:33:05 ubuntu systemd[1]: Stopped Journal Service.
Nov 19 23:33:05 ubuntu systemd[1]: Starting Journal Service...
Nov 19 23:33:05 ubuntu systemd-journald[31363]: Journal started
Nov 19 23:33:05 ubuntu systemd-journald[31363]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 19 23:33:05 ubuntu systemd[1]: Started Journal Service.


```
### rsyslog
```
Nov 18 22:33:58 ubuntu kernel: [ 7094.418338] systemd[1]: Stopping Journal Service...
Nov 18 22:33:58 ubuntu kernel: [ 7094.418472] systemd-journald[31891]: Received SIGTERM from PID 1 (systemd).
Nov 18 22:33:58 ubuntu kernel: [ 7094.421303] systemd[1]: systemd-journald.service: Succeeded.
Nov 18 22:33:58 ubuntu kernel: [ 7094.422591] systemd[1]: Stopped Journal Service.
Nov 18 22:33:58 ubuntu kernel: [ 7094.429455] systemd[1]: Starting Journal Service...
Nov 18 22:33:58 ubuntu kernel: [ 7094.463340] systemd[1]: Started Journal Service.


```

# journalから復旧
## journalstart

### jounal
```
Nov 18 22:25:22 ubuntu systemd[1]: Stopping Journal Service...
Nov 18 22:25:22 ubuntu systemd-journald[31842]: Received SIGTERM from PID 1 (systemd).
Nov 18 22:25:22 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 18 22:25:22 ubuntu systemd[1]: Stopped Journal Service.
Nov 18 22:25:22 ubuntu systemd[1]: Starting Journal Service...
Nov 18 22:25:22 ubuntu systemd-journald[31861]: Journal started
Nov 18 22:25:22 ubuntu systemd-journald[31861]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 18 22:25:22 ubuntu systemd[1]: Started Journal Service.

```
### rsyslog
```

```

## rsysstart
### jounal
```
Nov 19 23:34:47 ubuntu systemd[1]: Reloading.
Nov 19 23:34:47 ubuntu systemd-rc-local-generator[31384]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:34:47 ubuntu systemd[1]: Reloading.
Nov 19 23:34:47 ubuntu systemd-rc-local-generator[31409]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:34:47 ubuntu systemd[1]: Reloading.
Nov 19 23:34:47 ubuntu systemd-rc-local-generator[31431]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:34:53 ubuntu systemd[1]: Starting System Logging Service...
Nov 19 23:34:53 ubuntu rsyslogd[31440]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 19 23:34:53 ubuntu rsyslogd[31440]: rsyslogd's groupid changed to 110
Nov 19 23:34:53 ubuntu rsyslogd[31440]: rsyslogd's userid changed to 104
Nov 19 23:34:53 ubuntu rsyslogd[31440]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31440" x-info="https://www.rsyslog.com"] start
Nov 19 23:34:53 ubuntu systemd[1]: Started System Logging Service.

```
### rsyslog
```
Nov 19 23:34:53 ubuntu kernel: [ 1702.244678] systemd[1]: Stopping Journal Service...
Nov 19 23:34:53 ubuntu kernel: [ 1702.244823] systemd-journald[31282]: Received SIGTERM from PID 1 (systemd).
Nov 19 23:34:53 ubuntu kernel: [ 1702.245534] systemd[1]: systemd-journald.service: Succeeded.
Nov 19 23:34:53 ubuntu kernel: [ 1702.246020] systemd[1]: Stopped Journal Service.
Nov 19 23:34:53 ubuntu kernel: [ 1702.248045] systemd[1]: Starting Journal Service...
Nov 19 23:34:53 ubuntu kernel: [ 1702.283717] systemd[1]: Started Journal Service.
Nov 19 23:34:53 ubuntu kernel: [ 1803.510052] systemd-rc-local-generator[31384]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:34:53 ubuntu kernel: [ 1803.810564] systemd-rc-local-generator[31409]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:34:53 ubuntu kernel: [ 1804.066930] systemd-rc-local-generator[31431]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:34:47 ubuntu systemd[1]: Reloading.
Nov 19 23:34:47 ubuntu systemd[1]: message repeated 2 times: [ Reloading.]
Nov 19 23:34:53 ubuntu systemd[1]: Starting System Logging Service...
Nov 19 23:34:53 ubuntu rsyslogd: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 19 23:34:53 ubuntu rsyslogd: rsyslogd's groupid changed to 110
Nov 19 23:34:53 ubuntu rsyslogd: rsyslogd's userid changed to 104
Nov 19 23:34:53 ubuntu rsyslogd: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31440" x-info="https://www.rsyslog.com"] start
Nov 19 23:34:53 ubuntu systemd[1]: Started System Logging Service.

```

### jounal
```
```
### rsyslog
```
```
### jounal
```
```
### rsyslog
```
```
### jounal
```
```
### rsyslog
```
```
### jounal
```
```
### rsyslog
```
```
### jounal
```
```
### rsyslog
```
```
### jounal
```
```
### rsyslog
```
```
