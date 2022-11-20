# rsys stop jour change.md
## rsys stop
### jour
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
### sys
```
Nov 19 23:46:47 ubuntu systemd[1]: Reloading.
Nov 19 23:46:48 ubuntu kernel: [ 2524.441119] systemd-rc-local-generator[31618]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:46:48 ubuntu kernel: [ 2524.723578] systemd-rc-local-generator[31642]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:46:48 ubuntu kernel: [ 2525.012329] systemd-rc-local-generator[31664]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:46:48 ubuntu systemd[1]: message repeated 2 times: [ Reloading.]
```
## jour change
### jour
```
Nov 19 23:59:48 ubuntu systemd[1]: Reloading.
Nov 19 23:59:49 ubuntu systemd-rc-local-generator[31960]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:59:49 ubuntu systemd[1]: Reloading.
Nov 19 23:59:49 ubuntu systemd-rc-local-generator[31985]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:59:49 ubuntu systemd[1]: Reloading.
Nov 19 23:59:49 ubuntu systemd-rc-local-generator[32008]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:59:55 ubuntu systemd[1]: Stopping System Logging Service...
Nov 19 23:59:55 ubuntu rsyslogd[31930]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31930" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 19 23:59:55 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 19 23:59:55 ubuntu systemd[1]: Stopped System Logging Service.
Nov 20 00:00:00 ubuntu systemd[1]: Starting Rotate log files...
Nov 20 00:00:00 ubuntu systemd[1]: Starting Daily man-db regeneration...
Nov 20 00:00:00 ubuntu systemd[1]: Stopping Make remote CUPS printers available locally...
Nov 20 00:00:00 ubuntu systemd[1]: cups-browsed.service: Succeeded.
Nov 20 00:00:00 ubuntu systemd[1]: Stopped Make remote CUPS printers available locally.
Nov 20 00:00:00 ubuntu systemd[1]: Stopping CUPS Scheduler...
Nov 20 00:00:00 ubuntu systemd[1]: cups.service: Succeeded.
Nov 20 00:00:00 ubuntu systemd[1]: Stopped CUPS Scheduler.
Nov 20 00:00:00 ubuntu systemd[1]: cups.path: Succeeded.
Nov 20 00:00:00 ubuntu systemd[1]: Stopped CUPS Scheduler.
Nov 20 00:00:00 ubuntu systemd[1]: Stopping CUPS Scheduler.
Nov 20 00:00:00 ubuntu systemd[1]: Started CUPS Scheduler.
Nov 20 00:00:00 ubuntu systemd[1]: cups.socket: Succeeded.
Nov 20 00:00:00 ubuntu systemd[1]: Closed CUPS Scheduler.
Nov 20 00:00:00 ubuntu systemd[1]: Stopping CUPS Scheduler.
Nov 20 00:00:00 ubuntu systemd[1]: Listening on CUPS Scheduler.
Nov 20 00:00:00 ubuntu systemd[1]: Started CUPS Scheduler.
Nov 20 00:00:00 ubuntu systemd[1]: Started Make remote CUPS printers available locally.
Nov 20 00:00:00 ubuntu logrotate[32039]: Failed to kill unit rsyslog.service: Unit rsyslog.service not loaded.
Nov 20 00:00:00 ubuntu logrotate[32022]: error: error running non-shared postrotate script for /var/log/syslog of '/var/log/syslog
Nov 20 00:00:00 ubuntu logrotate[32022]: '
Nov 20 00:00:00 ubuntu logrotate[32042]: Failed to kill unit rsyslog.service: Unit rsyslog.service not loaded.
Nov 20 00:00:00 ubuntu logrotate[32022]: error: error running shared postrotate script for '/var/log/mail.info
Nov 20 00:00:00 ubuntu logrotate[32022]: /var/log/mail.warn
Nov 20 00:00:00 ubuntu logrotate[32022]: /var/log/mail.err
Nov 20 00:00:00 ubuntu logrotate[32022]: /var/log/mail.log
Nov 20 00:00:00 ubuntu logrotate[32022]: /var/log/daemon.log
Nov 20 00:00:00 ubuntu logrotate[32022]: /var/log/kern.log
Nov 20 00:00:00 ubuntu logrotate[32022]: /var/log/auth.log
Nov 20 00:00:00 ubuntu logrotate[32022]: /var/log/user.log
Nov 20 00:00:00 ubuntu logrotate[32022]: /var/log/lpr.log
Nov 20 00:00:00 ubuntu logrotate[32022]: /var/log/cron.log
Nov 20 00:00:00 ubuntu logrotate[32022]: /var/log/debug
Nov 20 00:00:00 ubuntu logrotate[32022]: /var/log/messages
Nov 20 00:00:00 ubuntu logrotate[32022]: '
Nov 20 00:00:00 ubuntu systemd[1]: logrotate.service: Main process exited, code=exited, status=1/FAILURE
Nov 20 00:00:00 ubuntu systemd[1]: logrotate.service: Failed with result 'exit-code'.
Nov 20 00:00:00 ubuntu systemd[1]: Failed to start Rotate log files.
Nov 20 00:00:00 ubuntu systemd[1]: man-db.service: Succeeded.
Nov 20 00:00:00 ubuntu systemd[1]: Finished Daily man-db regeneration.
Nov 20 00:00:00 ubuntu audit[32038]: AVC apparmor="DENIED" operation="capable" profile="/usr/sbin/cups-browsed" pid=32038 comm="cups-browsed" capability=23  capname="sys_nice"
Nov 20 00:00:00 ubuntu kernel: audit: type=1400 audit(1668931200.635:63): apparmor="DENIED" operation="capable" profile="/usr/sbin/cups-browsed" pid=32038 comm="cups-browsed" capability=23  capname="sys_nice"
Nov 20 00:00:44 ubuntu systemd-journald[31936]: Journal stopped
# error出てる
```
### sys
```
```

# rsys start to jour change
## sys start
### jour
```
```
### sys
```
Nov 19 23:59:48 ubuntu systemd[1]: Reloading.
Nov 19 23:59:49 ubuntu kernel: [ 3305.495137] systemd-rc-local-generator[31960]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:59:49 ubuntu kernel: [ 3305.789557] systemd-rc-local-generator[31985]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:59:49 ubuntu kernel: [ 3306.117429] systemd-rc-local-generator[32008]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:59:49 ubuntu systemd[1]: message repeated 2 times: [ Reloading.]

```
## jour change
### jour
```
Nov 20 00:04:17 ubuntu systemd-journald[32053]: Received SIGTERM from PID 1 (systemd).
Nov 20 00:04:17 ubuntu systemd[1]: Stopping Journal Service...
Nov 20 00:04:17 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 20 00:04:17 ubuntu systemd[1]: Stopped Journal Service.
Nov 20 00:04:17 ubuntu systemd[1]: Starting Journal Service...
Nov 20 00:04:17 ubuntu systemd-journald[32136]: Journal started
Nov 20 00:04:17 ubuntu systemd-journald[32136]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 20 00:04:17 ubuntu systemd[1]: Started Journal Service.

```
### sys
```
```
# jour change to rsys start
## jour change
### jour
```
Nov 20 00:08:10 ubuntu systemd[1]: Stopping Journal Service...
Nov 20 00:08:10 ubuntu systemd-journald[32234]: Received SIGTERM from PID 1 (systemd).
Nov 20 00:08:10 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 20 00:08:10 ubuntu systemd[1]: Stopped Journal Service.
Nov 20 00:08:10 ubuntu systemd[1]: Starting Journal Service...
Nov 20 00:08:10 ubuntu systemd-journald[32239]: Journal started
Nov 20 00:08:10 ubuntu systemd-journald[32239]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 20 00:08:10 ubuntu systemd[1]: Started Journal Service.

```
### sys
```
```
## sys start
### jour
```
Nov 20 00:08:37 ubuntu systemd[1]: Reloading.
Nov 20 00:08:37 ubuntu systemd-rc-local-generator[32260]: /etc/rc.local is not marked executable, skipping.
Nov 20 00:08:37 ubuntu systemd[1]: Starting Message of the Day...
Nov 20 00:08:37 ubuntu systemd[1]: motd-news.service: Succeeded.
Nov 20 00:08:37 ubuntu systemd[1]: Finished Message of the Day.
Nov 20 00:08:37 ubuntu systemd[1]: Reloading.
Nov 20 00:08:37 ubuntu systemd-rc-local-generator[32286]: /etc/rc.local is not marked executable, skipping.
Nov 20 00:08:38 ubuntu systemd[1]: Reloading.
Nov 20 00:08:38 ubuntu systemd-rc-local-generator[32308]: /etc/rc.local is not marked executable, skipping.
Nov 20 00:08:43 ubuntu systemd[1]: Starting System Logging Service...
Nov 20 00:08:43 ubuntu rsyslogd[32317]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 20 00:08:43 ubuntu rsyslogd[32317]: rsyslogd's groupid changed to 110
Nov 20 00:08:43 ubuntu rsyslogd[32317]: rsyslogd's userid changed to 104
Nov 20 00:08:43 ubuntu rsyslogd[32317]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="32317" x-info="https://www.rsyslog.com"] start
Nov 20 00:08:43 ubuntu systemd[1]: Started System Logging Service.

```
### sys
```
Nov 19 23:59:48 ubuntu systemd[1]: Reloading.
Nov 19 23:59:49 ubuntu kernel: [ 3305.495137] systemd-rc-local-generator[31960]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:59:49 ubuntu kernel: [ 3305.789557] systemd-rc-local-generator[31985]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:59:49 ubuntu kernel: [ 3306.117429] systemd-rc-local-generator[32008]: /etc/rc.local is not marked executable, skipping.
Nov 19 23:59:49 ubuntu systemd[1]: message repeated 2 times: [ Reloading.]

```
