`perl -mIO::Socket::INET -le 'print IO::Socket::INET->new(PeerAddr=>shift,PeerPort=>shift,Proto=>shift,Timeout=>5)?"open":"close"' 127.0.0.1 23`
