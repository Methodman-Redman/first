# cent jour change rsys stop
## jour change
### journal
```
Nov 19 16:20:43 localhost.localdomain systemd-journald[4227]: Journal stopped

```
### messages
```
Nov 19 16:20:43 localhost systemd-journald[4227]: Journal stopped

```
## rsys stop

no messages

# jour change to rsys start
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
Nov 19 16:16:27 localhost.localdomain systemd[1]: Starting System Logging Service...
Nov 19 16:16:27 localhost.localdomain rsyslogd[4239]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4239" x-info="https://www.rsyslog.com"] start
Nov 19 16:16:27 localhost.localdomain systemd[1]: Started System Logging Service.
Nov 19 16:16:27 localhost.localdomain rsyslogd[4239]: imjournal: journal files changed, reloading...  [v8.2102.0-10.el8 try https://www.rsyslog.com/e/0 ]
Nov 19 16:17:17 localhost.localdomain cent[4251]: test
Nov 19 16:20:43 localhost.localdomain systemd-journald[4227]: Journal stopped



```
## rsys start
### journal
```
Nov 19 16:33:48 localhost.localdomain systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:33:48 localhost.localdomain systemd[1]: Stopped Journal Service.
Nov 19 16:33:48 localhost.localdomain systemd[1]: Starting Journal Service...
Nov 19 16:33:48 localhost.localdomain systemd-journald[4752]: Journal started
Nov 19 16:33:48 localhost.localdomain systemd-journald[4752]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:33:48 localhost.localdomain systemd[1]: Started Journal Service.
```
### messages
```
```
## rsys start
### journal
```
Nov 19 16:35:05 localhost.localdomain systemd[1]: Starting System Logging Service...
Nov 19 16:35:05 localhost.localdomain rsyslogd[4763]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4763" x-info="https://www.rsyslog.com"] start
Nov 19 16:35:05 localhost.localdomain systemd[1]: Started System Logging Service.
Nov 19 16:35:05 localhost.localdomain rsyslogd[4763]: imjournal: journal files changed, reloading...  [v8.2102.0-10.el8 try https://www.rsyslog.com/e/0 ]

```
### messages
```
Nov 19 16:33:48 localhost systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:33:48 localhost systemd[1]: Stopped Journal Service.
Nov 19 16:33:48 localhost systemd[1]: Starting Journal Service...
Nov 19 16:33:48 localhost systemd-journald[4752]: Journal started
Nov 19 16:33:48 localhost systemd-journald[4752]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:33:48 localhost systemd[1]: Started Journal Service.
Nov 19 16:35:05 localhost systemd[1]: Starting System Logging Service...
Nov 19 16:35:05 localhost rsyslogd[4763]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4763" x-info="https://www.rsyslog.com"] start
Nov 19 16:35:05 localhost systemd[1]: Started System Logging Service.
Nov 19 16:35:05 localhost rsyslogd[4763]: imjournal: journal files changed, reloading...  [v8.2102.0-10.el8 try https://www.rsyslog.com/e/0 ]

```

# rsys start to jour change
## rsys start
no messages
## jour chage
### journal
```
Nov 19 16:38:20 localhost.localdomain systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:38:20 localhost.localdomain systemd[1]: Stopped Journal Service.
Nov 19 16:38:20 localhost.localdomain systemd[1]: Starting Journal Service...
Nov 19 16:38:20 localhost.localdomain systemd-journald[4853]: Journal started
Nov 19 16:38:20 localhost.localdomain systemd-journald[4853]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:38:20 localhost.localdomain systemd[1]: Started Journal Service.

```
### messages
```
Nov 19 16:38:20 localhost systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:38:20 localhost systemd[1]: Stopped Journal Service.
Nov 19 16:38:20 localhost systemd[1]: Starting Journal Service...
Nov 19 16:38:20 localhost systemd-journald[4853]: Journal started
Nov 19 16:38:20 localhost systemd-journald[4853]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:38:20 localhost systemd[1]: Started Journal Service.

```
