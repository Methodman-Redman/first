# ubuntu20.04
## rsyslogstop
### jounal
```
Nov 18 19:21:10 ubuntu systemd[1]: fprintd.service: Succeeded.
Nov 18 19:21:16 ubuntu systemd[1]: Stopping System Logging Service...
Nov 18 19:21:16 ubuntu rsyslogd[31410]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31410" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 18 19:21:16 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 18 19:21:16 ubuntu systemd[1]: Stopped System Logging Service.
Nov 18 19:21:16 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 19:21:16 ubuntu rsyslogd[31499]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 18 19:21:16 ubuntu systemd[1]: Started System Logging Service.
Nov 18 19:21:16 ubuntu rsyslogd[31499]: rsyslogd's groupid changed to 110
Nov 18 19:21:16 ubuntu rsyslogd[31499]: rsyslogd's userid changed to 104
Nov 18 19:21:16 ubuntu rsyslogd[31499]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31499" x-info="https://www.rsyslog.com"] start

```
### rsyslog
```
Nov 18 19:21:16 ubuntu systemd[1]: Stopping System Logging Service...
Nov 18 19:21:16 ubuntu rsyslogd: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31410" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 18 19:21:16 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 18 19:21:16 ubuntu systemd[1]: Stopped System Logging Service.
Nov 18 19:21:16 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 19:21:16 ubuntu rsyslogd: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 18 19:21:16 ubuntu systemd[1]: Started System Logging Service.
Nov 18 19:21:16 ubuntu rsyslogd: rsyslogd's groupid changed to 110
Nov 18 19:21:16 ubuntu rsyslogd: rsyslogd's userid changed to 104
Nov 18 19:21:16 ubuntu rsyslogd: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31499" x-info="https://www.rsyslog.com"] start

```
## journalstop
### jounal
```
Nov 18 19:23:35 ubuntu systemd-journald[31416]: Journal stopped

```
### rsyslog(systemctl stop syslog.socketを止めないと出る　止めたら出ない)
```
Nov 18 19:23:35 ubuntu kernel: [ 4485.721459] systemd[1]: Stopping Journal Service...
Nov 18 19:23:35 ubuntu kernel: [ 4485.721748] systemd-journald[31416]: Received SIGTERM from PID 1 (systemd).
Nov 18 19:23:35 ubuntu kernel: [ 4485.727287] systemd[1]: systemd-journald.service: Succeeded.
Nov 18 19:23:35 ubuntu kernel: [ 4485.729613] systemd[1]: Stopped Journal Service.
Nov 18 19:23:44 ubuntu kernel: [ 4494.835391] systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 18 19:23:44 ubuntu kernel: [ 4494.835589] systemd[1]: Closed Journal Socket (/dev/log).
Nov 18 19:24:13 ubuntu kernel: [ 4523.884484] systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 18 19:24:13 ubuntu kernel: [ 4523.884792] systemd[1]: Closed Journal Audit Socket.
Nov 18 19:24:13 ubuntu kernel: [ 4523.890969] systemd[1]: systemd-journald.socket: Succeeded.
Nov 18 19:24:13 ubuntu kernel: [ 4523.891284] systemd[1]: Closed Journal Socket.

```
##  journal start
### jounal
```
Nov 18 19:25:45 ubuntu systemd[1]: Stopping System Logging Service...
Nov 18 19:25:45 ubuntu rsyslogd[31499]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31499" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 18 19:25:45 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 18 19:25:45 ubuntu systemd[1]: Stopped System Logging Service.
Nov 18 19:25:45 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 19:25:45 ubuntu rsyslogd[31520]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 18 19:25:45 ubuntu rsyslogd[31520]: rsyslogd's groupid changed to 110
Nov 18 19:25:45 ubuntu systemd[1]: Started System Logging Service.
Nov 18 19:25:45 ubuntu rsyslogd[31520]: rsyslogd's userid changed to 104
Nov 18 19:25:45 ubuntu rsyslogd[31520]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31520" x-info="https://www.rsyslog.com"] start
Nov 18 19:25:53 ubuntu systemd[1]: Stopping System Logging Service...
Nov 18 19:25:53 ubuntu rsyslogd[31520]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31520" x-info="https://www.rsyslog.com"] exiting on signal 15.
Nov 18 19:25:53 ubuntu systemd[1]: rsyslog.service: Succeeded.
Nov 18 19:25:53 ubuntu systemd[1]: Stopped System Logging Service.
Nov 18 19:25:53 ubuntu systemd[1]: syslog.socket: Succeeded.
Nov 18 19:25:53 ubuntu systemd[1]: Closed Syslog Socket.
Nov 18 19:26:02 ubuntu systemd-journald[31517]: Journal stopped
Nov 18 19:27:08 ubuntu systemd[1]: Stopping Journal Service...
Nov 18 19:27:08 ubuntu systemd-journald[31517]: Received SIGTERM from PID 1 (systemd).
Nov 18 19:27:08 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 18 19:27:08 ubuntu systemd[1]: Stopped Journal Service.
Nov 18 19:27:08 ubuntu systemd[1]: Starting Journal Service...
Nov 18 19:27:08 ubuntu systemd[1]: Starting Network Manager Script Dispatcher Service...
Nov 18 19:27:08 ubuntu systemd[1]: Started Network Manager Script Dispatcher Service.
Nov 18 19:27:08 ubuntu systemd-journald[31528]: Journal started
Nov 18 19:27:08 ubuntu systemd-journald[31528]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 18 19:27:08 ubuntu dbus-daemon[733]: [system] Activating via systemd: service name='org.freedesktop.nm_dispatcher' unit='dbus-org.freedesktop.nm-dispatcher.service' requested by ':1.11' (uid=0 pid=734 comm="/usr/sbin/NetworkManager --no-daemon " label="unconfined")
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2736] dhcp4 (ens33): option dhcp_lease_time      => '1800'
Nov 18 19:27:08 ubuntu dbus-daemon[733]: [system] Successfully activated service 'org.freedesktop.nm_dispatcher'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2736] dhcp4 (ens33): option domain_name          => 'localdomain'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2736] dhcp4 (ens33): option domain_name_servers  => '192.168.19.2'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2736] dhcp4 (ens33): option expiry               => '1668830228'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option ip_address           => '192.168.19.135'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option next_server          => '192.168.19.254'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option requested_broadcast_address => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option requested_domain_name => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option requested_domain_name_servers => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option requested_domain_search => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option requested_host_name  => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option requested_interface_mtu => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option requested_ms_classless_static_routes => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option requested_nis_domain => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option requested_nis_servers => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option requested_ntp_servers => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2737] dhcp4 (ens33): option requested_rfc3442_classless_static_routes => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2738] dhcp4 (ens33): option requested_root_path  => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2738] dhcp4 (ens33): option requested_routers    => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2738] dhcp4 (ens33): option requested_static_routes => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2738] dhcp4 (ens33): option requested_subnet_mask => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2738] dhcp4 (ens33): option requested_time_offset => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2738] dhcp4 (ens33): option requested_wpad       => '1'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2738] dhcp4 (ens33): option routers              => '192.168.19.2'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2738] dhcp4 (ens33): option subnet_mask          => '255.255.255.0'
Nov 18 19:27:08 ubuntu NetworkManager[734]: <info>  [1668828428.2738] dhcp4 (ens33): state changed extended -> extended
Nov 18 19:27:08 ubuntu systemd[1]: Started Journal Service.
Nov 18 19:27:08 ubuntu systemd-journald[31528]: Journal stopped
Nov 18 22:02:26 ubuntu systemd[1]: Stopping Journal Service...
Nov 18 22:02:26 ubuntu systemd-journald[31528]: Received SIGTERM from PID 1 (systemd).
Nov 18 22:02:26 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 18 22:02:26 ubuntu systemd[1]: Stopped Journal Service.
Nov 18 22:02:26 ubuntu systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 18 22:02:26 ubuntu systemd[1]: Closed Journal Socket (/dev/log).
Nov 18 22:02:26 ubuntu systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 18 22:02:26 ubuntu systemd[1]: Closed Journal Audit Socket.
Nov 18 22:02:26 ubuntu systemd[1]: systemd-journald.socket: Succeeded.
Nov 18 22:02:26 ubuntu systemd[1]: Closed Journal Socket.
Nov 18 22:02:26 ubuntu systemd[1]: NetworkManager-dispatcher.service: Succeeded.
Nov 18 22:02:26 ubuntu systemd[1]: Starting Fingerprint Authentication Daemon...
Nov 18 22:02:26 ubuntu systemd[31550]: fprintd.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 18 22:02:26 ubuntu systemd[1]: Started Fingerprint Authentication Daemon.
Nov 18 22:02:26 ubuntu systemd[1]: Starting Network Manager Script Dispatcher Service...
Nov 18 22:02:26 ubuntu systemd[31624]: NetworkManager-dispatcher.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 18 22:02:26 ubuntu systemd[1]: Started Network Manager Script Dispatcher Service.
Nov 18 22:02:26 ubuntu kernel: usb 2-2.1: USB disconnect, device number 6
Nov 18 22:02:26 ubuntu systemd[1]: Started Run anacron jobs.
Nov 18 22:02:26 ubuntu systemd[31642]: anacron.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 18 22:02:26 ubuntu kernel: usb 2-2.1: new full-speed USB device number 7 using uhci_hcd
Nov 18 22:02:26 ubuntu systemd[1]: Starting Refresh fwupd metadata and update motd...
Nov 18 22:02:26 ubuntu systemd[1]: anacron.service: Succeeded.
Nov 18 22:02:26 ubuntu systemd[31654]: fwupd-refresh.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 18 22:02:26 ubuntu systemd[1]: Stopped target Bluetooth.
Nov 18 22:02:26 ubuntu systemd[1]: Starting Load/Save RF Kill Switch Status...
Nov 18 22:02:26 ubuntu kernel: usb 2-2.1: New USB device found, idVendor=0e0f, idProduct=0008, bcdDevice= 1.00
Nov 18 22:02:26 ubuntu kernel: usb 2-2.1: New USB device strings: Mfr=1, Product=2, SerialNumber=3
Nov 18 22:02:26 ubuntu kernel: usb 2-2.1: Product: Virtual Bluetooth Adapter
Nov 18 22:02:26 ubuntu kernel: usb 2-2.1: Manufacturer: VMware
Nov 18 22:02:26 ubuntu kernel: usb 2-2.1: SerialNumber: 000650268328
Nov 18 22:02:26 ubuntu systemd[1]: Reached target Bluetooth.
Nov 18 22:02:26 ubuntu systemd[31666]: systemd-rfkill.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 18 22:02:26 ubuntu systemd[1]: Started Load/Save RF Kill Switch Status.
Nov 18 22:02:26 ubuntu kernel: e1000: ens33 NIC Link is Up 1000 Mbps Full Duplex, Flow Control: None
Nov 18 22:02:26 ubuntu kernel: IPv6: ADDRCONF(NETDEV_CHANGE): ens33: link becomes ready
Nov 18 22:02:26 ubuntu systemd[1]: fwupd-refresh.service: Main process exited, code=exited, status=1/FAILURE
Nov 18 22:02:26 ubuntu systemd[1]: fwupd-refresh.service: Failed with result 'exit-code'.
Nov 18 22:02:26 ubuntu systemd[1]: Failed to start Refresh fwupd metadata and update motd.
Nov 18 22:02:26 ubuntu systemd[1]: systemd-rfkill.service: Succeeded.
Nov 18 22:02:26 ubuntu systemd[1]: NetworkManager-dispatcher.service: Succeeded.
Nov 18 22:02:26 ubuntu systemd[1]: fprintd.service: Succeeded.
Nov 18 22:02:26 ubuntu systemd[1]: Listening on Journal Audit Socket.
Nov 18 22:02:26 ubuntu systemd[1]: Listening on Journal Socket (/dev/log).
Nov 18 22:02:26 ubuntu systemd[1]: Listening on Journal Socket.
Nov 18 22:02:26 ubuntu systemd[1]: Starting Journal Service...
Nov 18 22:02:26 ubuntu systemd-journald[31764]: Journal started
Nov 18 22:02:26 ubuntu systemd-journald[31764]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 18 22:02:26 ubuntu systemd[1]: Started Journal Service.

```
### rsyslog
```
```

## rsyslog start
### jounal
```
Nov 18 22:04:38 ubuntu systemd[1]: Listening on Syslog Socket.
Nov 18 22:04:38 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 22:04:38 ubuntu rsyslogd[31767]: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 18 22:04:38 ubuntu systemd[1]: Started System Logging Service.
Nov 18 22:04:38 ubuntu rsyslogd[31767]: rsyslogd's groupid changed to 110
Nov 18 22:04:38 ubuntu rsyslogd[31767]: rsyslogd's userid changed to 104
Nov 18 22:04:38 ubuntu rsyslogd[31767]: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31767" x-info="https://www.rsyslog.com"] start

```
### rsyslog
```
Nov 18 22:04:38 ubuntu systemd[1]: Listening on Syslog Socket.
Nov 18 22:04:38 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 22:04:38 ubuntu rsyslogd: imuxsock: Acquired UNIX socket '/run/systemd/journal/syslog' (fd 3) from systemd.  [v8.2001.0]
Nov 18 22:04:38 ubuntu kernel: [ 4633.001951] systemd[1]: Stopping Journal Service...
Nov 18 22:04:38 ubuntu kernel: [ 4633.002683] systemd-journald[31517]: Received SIGTERM from PID 1 (systemd).
Nov 18 22:04:38 ubuntu kernel: [ 4633.007037] systemd[1]: systemd-journald.service: Succeeded.
Nov 18 22:04:38 ubuntu kernel: [ 4633.007489] systemd[1]: Stopped Journal Service.
Nov 18 22:04:38 ubuntu kernel: [ 4698.518160] systemd[1]: Starting Journal Service...
Nov 18 22:04:38 ubuntu kernel: [ 4698.523186] systemd[1]: Starting Network Manager Script Dispatcher Service...
Nov 18 22:04:38 ubuntu kernel: [ 4698.536428] systemd[1]: Started Network Manager Script Dispatcher Service.
Nov 18 22:04:38 ubuntu kernel: [ 4698.552444] systemd[1]: Started Journal Service.
Nov 18 22:04:38 ubuntu kernel: [ 4698.850810] systemd[1]: Stopping Journal Service...
Nov 18 22:04:38 ubuntu kernel: [ 4698.852010] systemd-journald[31528]: Received SIGTERM from PID 1 (systemd).
Nov 18 22:04:38 ubuntu kernel: [ 4698.867389] systemd[1]: systemd-journald.service: Succeeded.
Nov 18 22:04:38 ubuntu kernel: [ 4698.867789] systemd[1]: Stopped Journal Service.
Nov 18 22:04:38 ubuntu kernel: [ 4698.876312] systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 18 22:04:38 ubuntu kernel: [ 4698.876464] systemd[1]: Closed Journal Socket (/dev/log).
Nov 18 22:04:38 ubuntu systemd[1]: Started System Logging Service.
Nov 18 22:04:38 ubuntu rsyslogd: rsyslogd's groupid changed to 110
Nov 18 22:04:38 ubuntu rsyslogd: rsyslogd's userid changed to 104
Nov 18 22:04:38 ubuntu rsyslogd: [origin software="rsyslogd" swVersion="8.2001.0" x-pid="31767" x-info="https://www.rsyslog.com"] start
Nov 18 22:04:38 ubuntu kernel: [ 4698.882466] systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 18 22:04:38 ubuntu kernel: [ 4698.882596] systemd[1]: Closed Journal Audit Socket.
Nov 18 22:04:38 ubuntu kernel: [ 4698.890561] systemd[1]: systemd-journald.socket: Succeeded.
Nov 18 22:04:38 ubuntu kernel: [ 4698.890901] systemd[1]: Closed Journal Socket.
Nov 18 22:04:38 ubuntu kernel: [ 4708.520341] systemd[1]: NetworkManager-dispatcher.service: Succeeded.
Nov 18 22:04:38 ubuntu kernel: [ 5129.585152] systemd[1]: Starting Fingerprint Authentication Daemon...
Nov 18 22:04:38 ubuntu kernel: [ 5129.586127] systemd[31550]: fprintd.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 18 22:04:38 ubuntu kernel: [ 5129.638547] systemd[1]: Started Fingerprint Authentication Daemon.
Nov 18 22:04:38 ubuntu kernel: [ 5135.740138] systemd[1]: Starting Network Manager Script Dispatcher Service...
Nov 18 22:04:38 ubuntu kernel: [ 5135.741102] systemd[31624]: NetworkManager-dispatcher.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 18 22:04:38 ubuntu kernel: [ 5135.838856] systemd[1]: Started Network Manager Script Dispatcher Service.
Nov 18 22:04:38 ubuntu kernel: [ 5135.872964] usb 2-2.1: USB disconnect, device number 6
Nov 18 22:04:38 ubuntu kernel: [ 5136.623392] systemd[1]: Started Run anacron jobs.
Nov 18 22:04:38 ubuntu kernel: [ 5136.663986] systemd[31642]: anacron.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 18 22:04:38 ubuntu kernel: [ 5136.680122] usb 2-2.1: new full-speed USB device number 7 using uhci_hcd
Nov 18 22:04:38 ubuntu kernel: [ 5136.692161] systemd[1]: Starting Refresh fwupd metadata and update motd...
Nov 18 22:04:38 ubuntu kernel: [ 5136.743891] systemd[1]: anacron.service: Succeeded.
Nov 18 22:04:38 ubuntu kernel: [ 5136.756208] systemd[31654]: fwupd-refresh.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 18 22:04:38 ubuntu kernel: [ 5136.786231] systemd[1]: Stopped target Bluetooth.
Nov 18 22:04:38 ubuntu kernel: [ 5136.807402] systemd[1]: Starting Load/Save RF Kill Switch Status...
Nov 18 22:04:38 ubuntu kernel: [ 5136.816401] usb 2-2.1: New USB device found, idVendor=0e0f, idProduct=0008, bcdDevice= 1.00
Nov 18 22:04:38 ubuntu kernel: [ 5136.816406] usb 2-2.1: New USB device strings: Mfr=1, Product=2, SerialNumber=3
Nov 18 22:04:38 ubuntu kernel: [ 5136.816426] usb 2-2.1: Product: Virtual Bluetooth Adapter
Nov 18 22:04:38 ubuntu kernel: [ 5136.816445] usb 2-2.1: Manufacturer: VMware
Nov 18 22:04:38 ubuntu kernel: [ 5136.816446] usb 2-2.1: SerialNumber: 000650268328
Nov 18 22:04:38 ubuntu kernel: [ 5136.913389] systemd[1]: Reached target Bluetooth.
Nov 18 22:04:38 ubuntu kernel: [ 5136.924628] systemd[31666]: systemd-rfkill.service: Failed to connect stdout to the journal socket, ignoring: Connection refused
Nov 18 22:04:38 ubuntu kernel: [ 5136.964201] systemd[1]: Started Load/Save RF Kill Switch Status.
Nov 18 22:04:38 ubuntu kernel: [ 5137.073876] e1000: ens33 NIC Link is Up 1000 Mbps Full Duplex, Flow Control: None
Nov 18 22:04:38 ubuntu kernel: [ 5137.075155] IPv6: ADDRCONF(NETDEV_CHANGE): ens33: link becomes ready
Nov 18 22:04:38 ubuntu kernel: [ 5137.265457] systemd[1]: fwupd-refresh.service: Main process exited, code=exited, status=1/FAILURE
Nov 18 22:04:38 ubuntu kernel: [ 5137.265664] systemd[1]: fwupd-refresh.service: Failed with result 'exit-code'.
Nov 18 22:04:38 ubuntu kernel: [ 5137.269945] systemd[1]: Failed to start Refresh fwupd metadata and update motd.
Nov 18 22:04:38 ubuntu kernel: [ 5141.971837] systemd[1]: systemd-rfkill.service: Succeeded.
Nov 18 22:04:38 ubuntu kernel: [ 5147.518349] systemd[1]: NetworkManager-dispatcher.service: Succeeded.
Nov 18 22:04:38 ubuntu kernel: [ 5159.545500] systemd[1]: fprintd.service: Succeeded.
Nov 18 22:04:38 ubuntu kernel: [ 5202.643780] systemd[1]: Listening on Journal Audit Socket.
Nov 18 22:04:38 ubuntu kernel: [ 5202.644323] systemd[1]: Listening on Journal Socket (/dev/log).
Nov 18 22:04:38 ubuntu kernel: [ 5202.644838] systemd[1]: Listening on Journal Socket.
Nov 18 22:04:38 ubuntu kernel: [ 5202.657618] systemd[1]: Starting Journal Service...
Nov 18 22:04:38 ubuntu kernel: [ 5202.705382] systemd[1]: Started Journal Service.
```
# rsyslogaからstart
## rsyslog strat

### jounal
```
```
### rsyslog
```
Nov 18 22:10:21 ubuntu kernel: [ 5583.165257] systemd[1]: Stopping Journal Service...
Nov 18 22:10:21 ubuntu kernel: [ 5583.165435] systemd-journald[31764]: Received SIGTERM from PID 1 (systemd).
Nov 18 22:10:21 ubuntu kernel: [ 5583.171530] systemd[1]: systemd-journald.service: Succeeded.
Nov 18 22:10:21 ubuntu kernel: [ 5583.175500] systemd[1]: Stopped Journal Service.
Nov 18 22:10:21 ubuntu kernel: [ 5583.181951] systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 18 22:10:21 ubuntu kernel: [ 5583.182288] systemd[1]: Closed Journal Socket (/dev/log).
Nov 18 22:10:21 ubuntu kernel: [ 5583.188360] systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 18 22:10:21 ubuntu kernel: [ 5583.188839] systemd[1]: Closed Journal Audit Socket.
Nov 18 22:10:21 ubuntu kernel: [ 5583.200126] systemd[1]: systemd-journald.socket: Succeeded.
Nov 18 22:10:21 ubuntu kernel: [ 5583.200492] systemd[1]: Closed Journal Socket.
Nov 18 22:10:21 ubuntu kernel: [ 5678.050005] systemd[1]: Listening on Syslog Socket.
Nov 18 22:10:21 ubuntu kernel: [ 5678.056312] systemd[1]: Starting System Logging Service...
Nov 18 22:10:21 ubuntu kernel: [ 5678.061613] systemd[1]: Started System Logging Service.

```
journalstart
### jounal
```
Nov 18 22:10:59 ubuntu systemd[1]: Stopping Journal Service...
Nov 18 22:10:59 ubuntu systemd-journald[31764]: Received SIGTERM from PID 1 (systemd).
Nov 18 22:10:59 ubuntu systemd[1]: systemd-journald.service: Succeeded.
Nov 18 22:10:59 ubuntu systemd[1]: Stopped Journal Service.
Nov 18 22:10:59 ubuntu systemd[1]: systemd-journald-dev-log.socket: Succeeded.
Nov 18 22:10:59 ubuntu systemd[1]: Closed Journal Socket (/dev/log).
Nov 18 22:10:59 ubuntu systemd[1]: systemd-journald-audit.socket: Succeeded.
Nov 18 22:10:59 ubuntu systemd[1]: Closed Journal Audit Socket.
Nov 18 22:10:59 ubuntu systemd[1]: systemd-journald.socket: Succeeded.
Nov 18 22:10:59 ubuntu systemd[1]: Closed Journal Socket.
Nov 18 22:10:59 ubuntu systemd[1]: Listening on Syslog Socket.
Nov 18 22:10:59 ubuntu systemd[1]: Starting System Logging Service...
Nov 18 22:10:59 ubuntu systemd[1]: Started System Logging Service.
Nov 18 22:10:59 ubuntu systemd[1]: Listening on Journal Audit Socket.
Nov 18 22:10:59 ubuntu systemd[1]: Listening on Journal Socket (/dev/log).
Nov 18 22:10:59 ubuntu systemd[1]: Listening on Journal Socket.
Nov 18 22:10:59 ubuntu systemd[1]: Starting Journal Service...
Nov 18 22:10:59 ubuntu systemd-journald[31805]: Journal started
Nov 18 22:10:59 ubuntu systemd-journald[31805]: System Journal (/var/log/journal/43fb6dabeb8542328e5565d470031153) is 16.0M, max 2.8G, 2.8G free.
Nov 18 22:10:59 ubuntu systemd[1]: Started Journal Service.

```
### rsyslog
```
Nov 18 22:10:59 ubuntu kernel: [ 5715.366808] systemd[1]: Listening on Journal Audit Socket.
Nov 18 22:10:59 ubuntu kernel: [ 5715.367162] systemd[1]: Listening on Journal Socket (/dev/log).
Nov 18 22:10:59 ubuntu kernel: [ 5715.367440] systemd[1]: Listening on Journal Socket.
Nov 18 22:10:59 ubuntu kernel: [ 5715.373113] systemd[1]: Starting Journal Service...
Nov 18 22:10:59 ubuntu kernel: [ 5715.412159] systemd[1]: Started Journal Service.

```
