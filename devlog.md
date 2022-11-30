root@ubuntu:/run/systemd/journal# ls -la /dev/log
lrwxrwxrwx 1 root root 28 Nov 18 05:07 /dev/log -> /run/systemd/journal/dev-log
root@ubuntu:/run/systemd/journal# 

root@ubuntu:/run/systemd/journal# ls -la /run/systemd/journal/dev-log
srw-rw-rw- 1 root root 0 Nov 30 03:53 /run/systemd/journal/dev-log
root@ubuntu:/run/systemd/journal# 

root@ubuntu:/sys/kernel/tracing# systemctl stop systemd-journald.service systemd-journald-audit.socket systemd-journald-dev-log.socket systemd-journald.socket
root@ubuntu:/sys/kernel/tracing# systemctl status systemd-journald.service
● systemd-journald.service - Journal Service
     Loaded: loaded (/lib/systemd/system/systemd-journald.service; static; vend>
     Active: inactive (dead) since Wed 2022-11-30 03:52:18 PST; 16s ago
TriggeredBy: ● systemd-journald-audit.socket
             ● systemd-journald-dev-log.socket
             ● systemd-journald.socket
       Docs: man:systemd-journald.service(8)
             man:journald.conf(5)
    Process: 47824 ExecStart=/lib/systemd/systemd-journald (code=exited, status>
   Main PID: 47824 (code=exited, status=0/SUCCESS)
     Status: "Processing requests..."

Nov 30 03:33:31 ubuntu systemd-journald[47824]: Journal started
Nov 30 03:33:31 ubuntu systemd-journald[47824]: System Journal (/var/log/journa>
Nov 30 03:52:18 ubuntu systemd-journald[47824]: Journal stopped
root@ubuntu:/sys/kernel/tracing# systemctl stop apache2
root@ubuntu:/sys/kernel/tracing# systemctl start apache2
root@ubuntu:/sys/kernel/tracing# systemctl stop apache2
root@ubuntu:/sys/kernel/tracing# systemctl start apache2
root@ubuntu:/sys/kernel/tracing# systemctl stop apache2
root@ubuntu:/sys/kernel/tracing# systemctl start apache2
root@ubuntu:/sys/kernel/tracing# systemctl stop apache2
root@ubuntu:/sys/kernel/tracing# systemctl start apache2
root@ubuntu:/sys/kernel/tracing# systemctl start systemd-journald.service


root@ubuntu:/run/systemd/journal# journalctl -f
Nov 30 03:53:45 ubuntu systemd-journald[47824]: Received SIGTERM from PID 1 (systemd).
Nov 30 03:53:45 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 30 03:53:45 ubuntu systemd[1]: Stopped Journal Service.
Nov 30 03:53:45 ubuntu systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 30 03:53:45 ubuntu systemd[1]: Closed Journal Audit Socket.
Nov 30 03:53:45 ubuntu systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 30 03:53:45 ubuntu systemd[1]: Closed Journal Socket (/dev/log).
Nov 30 03:53:45 ubuntu systemd[1]: systemd-journald.socket: Succeeded.
Nov 30 03:53:45 ubuntu systemd[1]: Closed Journal Socket.
Nov 30 03:53:45 ubuntu systemd[1]: Stopping The Apache HTTP Server...
Nov 30 03:53:45 ubuntu systemd[48016]: apache2.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 30 03:53:45 ubuntu systemd[1]: apache2.service: Succeeded.
Nov 30 03:53:45 ubuntu systemd[1]: Stopped The Apache HTTP Server.
Nov 30 03:53:45 ubuntu systemd[1]: Starting The Apache HTTP Server...
Nov 30 03:53:45 ubuntu systemd[48023]: apache2.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 30 03:53:45 ubuntu systemd[1]: Started The Apache HTTP Server.
Nov 30 03:53:45 ubuntu systemd[1]: Stopping The Apache HTTP Server...
Nov 30 03:53:45 ubuntu systemd[48086]: apache2.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 30 03:53:45 ubuntu systemd[1]: apache2.service: Succeeded.
Nov 30 03:53:45 ubuntu systemd[1]: Stopped The Apache HTTP Server.
Nov 30 03:53:45 ubuntu systemd[1]: Starting The Apache HTTP Server...
Nov 30 03:53:45 ubuntu systemd[48093]: apache2.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 30 03:53:45 ubuntu systemd[1]: Started The Apache HTTP Server.
Nov 30 03:53:45 ubuntu systemd[1]: Stopping The Apache HTTP Server...
Nov 30 03:53:45 ubuntu systemd[48159]: apache2.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 30 03:53:45 ubuntu systemd[1]: apache2.service: Succeeded.
Nov 30 03:53:45 ubuntu systemd[1]: Stopped The Apache HTTP Server.
Nov 30 03:53:45 ubuntu systemd[1]: Starting The Apache HTTP Server...
Nov 30 03:53:45 ubuntu systemd[48166]: apache2.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 30 03:53:45 ubuntu systemd[1]: Started The Apache HTTP Server.
Nov 30 03:53:45 ubuntu systemd[1]: Stopping The Apache HTTP Server...
Nov 30 03:53:45 ubuntu systemd[48229]: apache2.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 30 03:53:45 ubuntu systemd[1]: apache2.service: Succeeded.
Nov 30 03:53:45 ubuntu systemd[1]: Stopped The Apache HTTP Server.
Nov 30 03:53:45 ubuntu systemd[1]: Starting The Apache HTTP Server...
Nov 30 03:53:45 ubuntu systemd[48236]: apache2.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 30 03:53:45 ubuntu systemd[1]: Started The Apache HTTP Server.
Nov 30 03:53:45 ubuntu systemd[1]: Listening on Journal Audit Socket.
Nov 30 03:53:45 ubuntu systemd[1]: Listening on Journal Socket (/dev/log).
Nov 30 03:53:45 ubuntu systemd[1]: Listening on Journal Socket.
Nov 30 03:53:45 ubuntu systemd[1]: Starting Journal Service...
Nov 30 03:53:45 ubuntu systemd-journald[48300]: Journal started
Nov 30 03:53:45 ubuntu systemd-journald[48300]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 40.0M, max 2.8G, 2.8G free.
Nov 30 03:53:45 ubuntu systemd[1]: Started Journal Service.


