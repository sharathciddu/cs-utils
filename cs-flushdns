#!/bin/bash 
if [[ "$OSTYPE" == 'linux-gnu' ]]; then
	service nscd reload
	service dnsmasq restart
	rndc restart
	echo "Flushed DNS cache on your Linux"
elif [[ "$OSTYPE" == 'darwin'* ]]; then
	dscacheutil -flushcache
	echo "Flushed DNS cache on your OSX"
fi
