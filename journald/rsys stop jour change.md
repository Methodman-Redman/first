# rsys stop jour change
## rsys stop
### journal
```
Nov 19 16:43:52 localhost.localdomain systemd[1]: Stopping System Logging Service...
Nov 19 16:43:52 localhost.localdomain rsyslogd[4837]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4837" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 19 16:43:52 localhost.localdomain systemd[1]: rsyslog.service: Succeeded.
Nov 19 16:43:52 localhost.localdomain systemd[1]: Stopped System Logging Service.

```
### messages
```

```
## jour change
### journal
```
Nov 19 16:45:00 localhost.localdomain systemd[1]: Stopping Journal Service...
Nov 19 16:45:00 localhost.localdomain systemd-journald[4853]: Journal stopped

```

# rsys start jour change
### messages(ここで来る)
```
Nov 19 16:43:52 localhost systemd[1]: Stopping System Logging Service...
Nov 19 16:43:52 localhost rsyslogd[4837]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4837" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 19 16:43:52 localhost systemd[1]: rsyslog.service: Succeeded.
Nov 19 16:43:52 localhost systemd[1]: Stopped System Logging Service.
Nov 19 16:45:00 localhost systemd[1]: Stopping Journal Service...
Nov 19 16:45:00 localhost systemd-journald[4853]: Journal stopped

```
### journal
```
Nov 19 16:46:53 localhost.localdomain systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:46:53 localhost.localdomain systemd[1]: Stopped Journal Service.
Nov 19 16:46:53 localhost.localdomain systemd[1]: Starting Journal Service...
Nov 19 16:46:53 localhost.localdomain systemd-journald[4994]: Journal started
Nov 19 16:46:53 localhost.localdomain systemd-journald[4994]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:46:53 localhost.localdomain systemd[1]: Started Journal Service.

```
### messages
```
Nov 19 16:46:53 localhost systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:46:53 localhost systemd[1]: Stopped Journal Service.
Nov 19 16:46:53 localhost systemd[1]: Starting Journal Service...
Nov 19 16:46:53 localhost systemd-journald[4994]: Journal started
Nov 19 16:46:53 localhost systemd-journald[4994]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:46:53 localhost systemd[1]: Started Journal Service.

```
# jour change rsys start 
### journal
```
Nov 19 16:49:15 localhost.localdomain systemd[1]: Stopping Journal Service...
Nov 19 16:49:15 localhost.localdomain systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:49:15 localhost.localdomain systemd[1]: Stopped Journal Service.
Nov 19 16:49:15 localhost.localdomain systemd[1]: Starting Journal Service...
Nov 19 16:49:15 localhost.localdomain systemd-journald[5032]: Journal started
Nov 19 16:49:15 localhost.localdomain systemd-journald[5032]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:49:15 localhost.localdomain systemd[1]: Started Journal Service.
```
### messages
```
```
## rsys start
### journal
```
Nov 19 16:49:53 localhost.localdomain systemd[1]: Starting System Logging Service...
Nov 19 16:49:53 localhost.localdomain rsyslogd[5035]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="5035" x-info="https://www.rsyslog.com"] start
Nov 19 16:49:53 localhost.localdomain systemd[1]: Started System Logging Service.
Nov 19 16:49:53 localhost.localdomain rsyslogd[5035]: imjournal: journal files changed, reloading...  [v8.2102.0-10.el8 try https://www.rsyslog.com/e/0 ]

```
### messages
```
Nov 19 16:48:22 localhost systemd[1]: Stopping System Logging Service...
Nov 19 16:48:22 localhost rsyslogd[4977]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="4977" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 19 16:48:22 localhost systemd[1]: rsyslog.service: Succeeded.
Nov 19 16:48:22 localhost systemd[1]: Stopped System Logging Service.
Nov 19 16:48:48 localhost systemd[1]: Stopping Journal Service...
Nov 19 16:48:48 localhost systemd-journald[4994]: Journal stopped
Nov 19 16:49:15 localhost systemd[1]: Stopping Journal Service...
Nov 19 16:49:15 localhost systemd[1]: systemd-journald.service: Succeeded.
Nov 19 16:49:15 localhost systemd[1]: Stopped Journal Service.
Nov 19 16:49:15 localhost systemd[1]: Starting Journal Service...
Nov 19 16:49:15 localhost systemd-journald[5032]: Journal started
Nov 19 16:49:15 localhost systemd-journald[5032]: Runtime journal (/run/log/journal/ba762de275444cb3b8a8f3418c5b9d8e) is 4.8M, max 38.8M, 34.0M free.
Nov 19 16:49:15 localhost systemd[1]: Started Journal Service.
Nov 19 16:49:53 localhost systemd[1]: Starting System Logging Service...
Nov 19 16:49:53 localhost rsyslogd[5035]: [origin software="rsyslogd" swVersion="8.2102.0-10.el8" x-pid="5035" x-info="https://www.rsyslog.com"] start
Nov 19 16:49:53 localhost systemd[1]: Started System Logging Service.
Nov 19 16:49:53 localhost rsyslogd[5035]: imjournal: journal files changed, reloading...  [v8.2102.0-10.el8 try https://www.rsyslog.com/e/0 ]

```
### journal
```
```
### messages
```
```
### journal
```
```
### messages
```
```
