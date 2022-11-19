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

## rsyslog stop(socketが何も言わない)
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
何も出ない
```

## journal change restart
### jounal
```
Nov 18 22:18:27 ubuntu systemd-journald[31810]: Received SIGTERM from PID 1 (systemd).
Nov 18 22:18:27 ubuntu systemd[1]: Stopping Journal Service...
Nov 18 22:18:27 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 18 22:18:27 ubuntu systemd[1]: Stopped Journal Service.
Nov 18 22:18:27 ubuntu systemd[1]: Starting Journal Service...
Nov 18 22:18:27 ubuntu systemd-journald[31831]: Journal started
Nov 18 22:18:27 ubuntu systemd-journald[31831]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 18 22:18:27 ubuntu systemd[1]: Started Journal Service.
# logger test後
Nov 18 22:19:07 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 22:19:07 ubuntu rsyslogd[31833]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 18 22:19:07 ubuntu rsyslogd[31833]: rsyslogd's groupid changed to 110
Nov 18 22:19:07 ubuntu rsyslogd[31833]: rsyslogd's userid changed to 104
Nov 18 22:19:07 ubuntu rsyslogd[31833]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31833" x-info="https://www.rsyslog.com"] start
Nov 18 22:19:07 ubuntu systemd[1]: Started System Logging Service.

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
## rsyslog start
### jounal
```
Nov 18 22:26:23 ubuntu systemd[1]: Listening on Syslog Socket.
Nov 18 22:26:23 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 22:26:23 ubuntu rsyslogd[31865]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 18 22:26:23 ubuntu rsyslogd[31865]: rsyslogd's groupid changed to 110
Nov 18 22:26:23 ubuntu systemd[1]: Started System Logging Service.
Nov 18 22:26:23 ubuntu rsyslogd[31865]: rsyslogd's userid changed to 104
Nov 18 22:26:23 ubuntu rsyslogd[31865]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31865" x-info="https://www.rsyslog.com"] start

```
### rsyslog
```
Nov 18 22:26:23 ubuntu systemd[1]: Listening on Syslog Socket.
Nov 18 22:26:23 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 22:26:23 ubuntu rsyslogd: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 18 22:26:23 ubuntu rsyslogd: rsyslogd's groupid changed to 110
Nov 18 22:26:23 ubuntu systemd[1]: Started System Logging Service.
Nov 18 22:26:23 ubuntu rsyslogd: rsyslogd's userid changed to 104
Nov 18 22:26:23 ubuntu rsyslogd: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31865" x-info="https://www.rsyslog.com"] start
Nov 18 22:26:23 ubuntu kernel: [ 6578.355585] systemd[1]: Stopping Journal Service...
Nov 18 22:26:23 ubuntu kernel: [ 6578.355599] systemd-journald[31842]: Received SIGTERM from PID 1 (systemd).
Nov 18 22:26:23 ubuntu kernel: [ 6578.356758] systemd[1]: systemd-journald.service: Succeeded.
Nov 18 22:26:23 ubuntu kernel: [ 6578.357870] systemd[1]: Stopped Journal Service.
Nov 18 22:26:23 ubuntu kernel: [ 6578.361534] systemd[1]: Starting Journal Service...
Nov 18 22:26:23 ubuntu kernel: [ 6578.396190] systemd[1]: Started Journal Service.

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
