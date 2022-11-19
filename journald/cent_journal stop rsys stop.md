# cent jounal stop rsys stop
## journal stop
### journal
```
Nov 19 16:02:07 localhost.localdomain systemd[1]: systemd-journal-flush.service: Succeeded.
Nov 19 16:02:07 localhost.localdomain systemd[1]: Stopped Flush Journal to Persistent Storage.
Nov 19 16:02:07 localhost.localdomain systemd-journald[735]: Journal stopped

```
### messages
```
Nov 19 16:02:07 localhost systemd[1]: systemd-journal-flush.service: Succeeded.
Nov 19 16:02:07 localhost systemd[1]: Stopped Flush Journal to Persistent Storage.
Nov 19 16:02:07 localhost systemd-journald[735]: Journal stopped
```
## rsys stop

どちらも何も出ない

# journalから起動
## journal start
### journal
```
Nov 19 16:05:15 localhost.localdomain systemd[1]: Stopping Journal Service...
Nov 19 16:05:15 localhost.localdomain systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:05:15 localhost.localdomain systemd[1]: Stopped Journal Service.
Nov 19 16:05:15 localhost.localdomain systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 16:05:15 localhost.localdomain systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 16:05:15 localhost.localdomain systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 16:05:15 localhost.localdomain systemd[1]: Closed Journal Socket.
Nov 19 16:05:15 localhost.localdomain systemd[1]: Stopping System Logging Service...
Nov 19 16:05:15 localhost.localdomain systemd[1]: rsyslog.service: Succeeded.
Nov 19 16:05:15 localhost.localdomain systemd[1]: Stopped System Logging Service.
Nov 19 16:05:15 localhost.localdomain systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 16:05:15 localhost.localdomain systemd[1]: Listening on Journal Socket.
Nov 19 16:05:15 localhost.localdomain systemd[1]: Starting Journal Service...
Nov 19 16:05:15 localhost.localdomain systemd-journald[4070]: Journal started
Nov 19 16:05:15 localhost.localdomain systemd-journald[4070]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:05:15 localhost.localdomain systemd[1]: Started Journal Service.

```
### messages
```
```

## rsys start
### journal
```
Nov 19 16:06:06 localhost.localdomain systemd[1]: Starting System Logging Service...
Nov 19 16:06:06 localhost.localdomain rsyslogd[4073]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4073" x-info="https://www.rsyslog.com"] start
Nov 19 16:06:06 localhost.localdomain systemd[1]: Started System Logging Service.
Nov 19 16:06:06 localhost.localdomain rsyslogd[4073]: imjournal: journal files changed, reloading...  [v8.2102.0-10.el8 try https://www.rsyslog.com/e/0 ]

```
### messages
```
Nov 19 16:02:07 localhost systemd[1]: systemd-journal-flush.service: Succeeded.
Nov 19 16:02:07 localhost systemd[1]: Stopped Flush Journal to Persistent Storage.
Nov 19 16:02:07 localhost systemd-journald[735]: Journal stopped
Nov 19 16:05:15 localhost systemd[1]: Stopping Journal Service...
Nov 19 16:05:15 localhost systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:05:15 localhost systemd[1]: Stopped Journal Service.
Nov 19 16:05:15 localhost systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 16:05:15 localhost systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 16:05:15 localhost systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 16:05:15 localhost systemd[1]: Closed Journal Socket.
Nov 19 16:05:15 localhost systemd[1]: Stopping System Logging Service...
Nov 19 16:05:15 localhost systemd[1]: rsyslog.service: Succeeded.
Nov 19 16:05:15 localhost systemd[1]: Stopped System Logging Service.
Nov 19 16:05:15 localhost systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 16:05:15 localhost systemd[1]: Listening on Journal Socket.
Nov 19 16:05:15 localhost systemd[1]: Starting Journal Service...
Nov 19 16:05:15 localhost systemd-journald[4070]: Journal started
Nov 19 16:05:15 localhost systemd-journald[4070]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:05:15 localhost systemd[1]: Started Journal Service.
Nov 19 16:06:06 localhost systemd[1]: Starting System Logging Service...
Nov 19 16:06:06 localhost rsyslogd[4073]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4073" x-info="https://www.rsyslog.com"] start
Nov 19 16:06:06 localhost systemd[1]: Started System Logging Service.
Nov 19 16:06:06 localhost rsyslogd[4073]: imjournal: journal files changed, reloading...  [v8.2102.0-10.el8 try https://www.rsyslog.com/e/0 ]
```

# rsysから起動
## rsys start
no messages
## journal start
### journal
```
Nov 19 16:08:42 localhost.localdomain systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:08:42 localhost.localdomain systemd[1]: Stopped Journal Service.
Nov 19 16:08:42 localhost.localdomain systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 16:08:42 localhost.localdomain systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 16:08:42 localhost.localdomain systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 16:08:42 localhost.localdomain systemd[1]: Closed Journal Socket.
Nov 19 16:08:42 localhost.localdomain systemd[1]: Stopping System Logging Service...
Nov 19 16:08:42 localhost.localdomain systemd[1]: rsyslog.service: Succeeded.
Nov 19 16:08:42 localhost.localdomain systemd[1]: Stopped System Logging Service.
Nov 19 16:08:42 localhost.localdomain systemd[1]: Starting System Logging Service...
Nov 19 16:08:42 localhost.localdomain systemd[1]: Started System Logging Service.
Nov 19 16:08:42 localhost.localdomain systemd[1]: Listening on Journal Socket.
Nov 19 16:08:42 localhost.localdomain systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 16:08:42 localhost.localdomain systemd[1]: Starting Journal Service...
Nov 19 16:08:42 localhost.localdomain systemd-journald[4123]: Journal started
Nov 19 16:08:42 localhost.localdomain systemd-journald[4123]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:08:42 localhost.localdomain systemd[1]: Started Journal Service.

```
### messages
```
Nov 19 16:08:42 localhost systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:08:42 localhost systemd[1]: Stopped Journal Service.
Nov 19 16:08:42 localhost systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 19 16:08:42 localhost systemd[1]: Closed Journal Socket (/dev/log).
Nov 19 16:08:42 localhost systemd[1]: systemd-journald.socket: Succeeded.
Nov 19 16:08:42 localhost systemd[1]: Closed Journal Socket.
Nov 19 16:08:42 localhost systemd[1]: Stopping System Logging Service...
Nov 19 16:08:42 localhost systemd[1]: rsyslog.service: Succeeded.
Nov 19 16:08:42 localhost systemd[1]: Stopped System Logging Service.
Nov 19 16:08:42 localhost systemd[1]: Starting System Logging Service...
Nov 19 16:08:42 localhost systemd[1]: Started System Logging Service.
Nov 19 16:08:42 localhost systemd[1]: Listening on Journal Socket.
Nov 19 16:08:42 localhost systemd[1]: Listening on Journal Socket (/dev/log).
Nov 19 16:08:42 localhost systemd[1]: Starting Journal Service...
Nov 19 16:08:42 localhost systemd-journald[4123]: Journal started
Nov 19 16:08:42 localhost systemd-journald[4123]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:08:42 localhost systemd[1]: Started Journal Service.

```
