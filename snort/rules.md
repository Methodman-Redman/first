# detailes

## pass
`etc/snort/rules`

## example
`alert tcp $EXTERNAL_NET any -> $HTTP_SERVERS $HTTP_PORTS (msg:"WEB-CGI phf access";flags:A+; uricontent:"/phf"; nocase; )`  

```
alert = alert
tcp = tcp/udp/icmp
$EXTERNAL_NET any = external network
-> = <-/<>
$HTTP_SERVERS $HTTP_PORTS = web_server_address

()
msg:"WEB-CGI phf access"; = alert message
flags:A+; = ackflag fin/syn/rst/psh/urg
uricontent:"/phf"; = uri is match /phf 
nocase; = Large Langage and Small Langage
```
