--------------------->
|patarn|1|2|3|4|
|--|--|--|--|--|
|1|jounal stop<br><br>jornal_log:6<br>rsys_log:10|rsyslog stop<br><br>jornal_log:0<br>rsys_log:4|journal start<br><br>jornal_log:7<br>rsys_log:0|rsyslog start<br><br>jornal_log:7<br>rsys_log:16|
|2|jounal stop<br><br>jornal_log:6<br>rsys_log:10|rsyslog stop<br><br>jornal_log:0<br>rsys_log:4|rsyslog start<br><br>jornal_log:0<br>rsys_log:8|journal start<br><br>jornal_log:16<br>rsys_log:5|
|3|jounal change<br><br>jornal_log:1<br>rsys_log:6|rsyslog stop<br><br>jornal_log:0<br>rsys_log:0|rsyslog start<br><br>jornal_log:0<br>rsys_log:0|journal change<br><br>jornal_log:8+6<br>rsys_log:6|
|4|jounal change<br><br>jornal_log:1<br>rsys_log:6|rsyslog stop<br><br>jornal_log:0<br>rsys_log:0|journal change<br><br>jornal_log:8<br>rsys_log:0|rsyslog start<br><br>jornal_log:7<br>rsys_log:15|
|5|rsyslog stop<br><br>jornal_log:11<br>rsys_log:10|journal stop<br><br>jornal_log:1<br>rsys_log:0|journal start<br><br>jornal_log:105<br>rsys_log:0|rsyslog start<br><br>jornal_log:7<br>rsys_log:62|
|6|rsyslog stop<br><br>jornal_log:11<br>rsys_log:10|journal stop<br><br>jornal_log:1<br>rsys_log:0|rsyslog start<br><br>jornal_log:0<br>rsys_log:11|journal start<br><br>jornal_log:20<br>rsys_log:5|










n:none a:2 b:6 c:10~
