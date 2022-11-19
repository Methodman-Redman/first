# cent rsys stop journal stop
## rsys stop
### journal
```
Nov 19 16:11:28 localhost.localdomain systemd[1]: Stopping System Logging Service...
Nov 19 16:11:29 localhost.localdomain rsyslogd[4110]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4110" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 19 16:11:29 localhost.localdomain systemd[1]: rsyslog.service: Succeeded.
Nov 19 16:11:29 localhost.localdomain systemd[1]: Stopped System Logging Service.

```
### messages
```
```
## journal stop

### journal
```
Nov 19 16:12:00 localhost.localdomain systemd[1]: Stopping Journal Service...
Nov 19 16:12:00 localhost.localdomain systemd-journald[4123]: Journal stopped

```
### messages
```
# rsys start to journal start
```
### journal
```
```
### messages
```
Nov 19 16:11:28 localhost systemd[1]: Stopping System Logging Service...
Nov 19 16:11:29 localhost rsyslogd[4110]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4110" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 19 16:11:29 localhost systemd[1]: rsyslog.service: Succeeded.
Nov 19 16:11:29 localhost systemd[1]: Stopped System Logging Service.
Nov 19 16:12:00 localhost systemd[1]: Stopping Journal Service...
Nov 19 16:12:00 localhost systemd-journald[4123]: Journal stopped

```
## journal start
### journal
```
Nov 19 16:13:40 localhost.localdomain systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:13:40 localhost.localdomain systemd[1]: Stopped Journal Service.
Nov 19 16:13:40 localhost.localdomain systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 16:13:40 localhost.localdomain systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 16:13:40 localhost.localdomain systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 16:13:40 localhost.localdomain systemd[1]: Closed Journal Socket.
Nov 19 16:13:40 localhost.localdomain systemd[1]: Starting System Logging Service...
Nov 19 16:13:40 localhost.localdomain systemd[1]: Started System Logging Service.
Nov 19 16:13:40 localhost.localdomain systemd[1]: Listening on Journal Socket.
Nov 19 16:13:40 localhost.localdomain systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 16:13:40 localhost.localdomain systemd[1]: Starting Journal Service...
Nov 19 16:13:40 localhost.localdomain systemd-journald[4186]: Journal started
Nov 19 16:13:40 localhost.localdomain systemd-journald[4186]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:13:40 localhost.localdomain systemd[1]: Started Journal Service.

```
### messages
```
Nov 19 16:13:40 localhost systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:13:40 localhost systemd[1]: Stopped Journal Service.
Nov 19 16:13:40 localhost systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 16:13:40 localhost systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 16:13:40 localhost systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 16:13:40 localhost systemd[1]: Closed Journal Socket.
Nov 19 16:13:40 localhost systemd[1]: Starting System Logging Service...
Nov 19 16:13:40 localhost systemd[1]: Started System Logging Service.
Nov 19 16:13:40 localhost systemd[1]: Listening on Journal Socket.
Nov 19 16:13:40 localhost systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 16:13:40 localhost systemd[1]: Starting Journal Service...
Nov 19 16:13:40 localhost systemd-journald[4186]: Journal started
Nov 19 16:13:40 localhost systemd-journald[4186]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:13:40 localhost systemd[1]: Started Journal Service.

```

# journal start to rsys start

### journal
```
Nov 19 16:15:50 localhost.localdomain systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:15:50 localhost.localdomain systemd[1]: Stopped Journal Service.
Nov 19 16:15:50 localhost.localdomain systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 16:15:50 localhost.localdomain systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 16:15:50 localhost.localdomain systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 16:15:50 localhost.localdomain systemd[1]: Closed Journal Socket.
Nov 19 16:15:50 localhost.localdomain systemd[1]: Listening on Journal Socket.
Nov 19 16:15:50 localhost.localdomain systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 16:15:50 localhost.localdomain systemd[1]: Starting Journal Service...
Nov 19 16:15:50 localhost.localdomain systemd-journald[4227]: Journal started
Nov 19 16:15:50 localhost.localdomain systemd-journald[4227]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:15:50 localhost.localdomain systemd[1]: Started Journal Service.

```
### messages
```

```

## rsys start
### journal
```
Nov 19 16:16:27 localhost.localdomain systemd[1]: Starting System Logging Service...
Nov 19 16:16:27 localhost.localdomain rsyslogd[4239]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4239" x-info="https://www.rsyslog.com"] start
Nov 19 16:16:27 localhost.localdomain systemd[1]: Started System Logging Service.
Nov 19 16:16:27 localhost.localdomain rsyslogd[4239]: imjournal: journal files changed, reloading...  [v8.2102.0-10.el8 try https://www.rsyslog.com/e/0 ]

```
### messages
```
Nov 19 16:15:13 localhost systemd[1]: Stopping System Logging Service...
Nov 19 16:15:13 localhost rsyslogd[4170]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4170" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 19 16:15:13 localhost systemd[1]: rsyslog.service: Succeeded.
Nov 19 16:15:13 localhost systemd[1]: Stopped System Logging Service.
Nov 19 16:15:17 localhost systemd[1]: Stopping Journal Service...
Nov 19 16:15:17 localhost systemd-journald[4186]: Journal stopped
Nov 19 16:15:50 localhost systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:15:50 localhost systemd[1]: Stopped Journal Service.
Nov 19 16:15:50 localhost systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 16:15:50 localhost systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 16:15:50 localhost systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 16:15:50 localhost systemd[1]: Closed Journal Socket.
Nov 19 16:15:50 localhost systemd[1]: Listening on Journal Socket.
Nov 19 16:15:50 localhost systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 16:15:50 localhost systemd[1]: Starting Journal Service...
Nov 19 16:15:50 localhost systemd-journald[4227]: Journal started
Nov 19 16:15:50 localhost systemd-journald[4227]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:15:50 localhost systemd[1]: Started Journal Service.
Nov 19 16:16:27 localhost systemd[1]: Starting System Logging Service...
Nov 19 16:16:27 localhost rsyslogd[4239]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4239" x-info="https://www.rsyslog.com"] start
Nov 19 16:16:27 localhost systemd[1]: Started System Logging Service.
Nov 19 16:16:27 localhost rsyslogd[4239]: imjournal: journal files changed, reloading...  [v8.2102.0-10.el8 try https://www.rsyslog.com/e/0 ]

```

