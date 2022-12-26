`perl -mIO::Socket::INET -le 'print IO::Socket::INET->new(PeerAddr=>shift,PeerPort=>shift,Proto=>shift,Timeout=>5)?"open":"close"' 127.0.0.1 23`

https://coding-school.com/scan-network-port-with-perl/  

`perl -MIO::Socket -e '$socket=IO::Socket::INET->new(Proto=>tcp,PeerAddr=>$ARGV[0],PeerPort=>$ARGV[1]);if($@) { print "close:$ARGV[0] $ARGV[1]"; } else { print "open:$ARGV[0] $ARGV[1]";}' 127.0.0.1 23`
