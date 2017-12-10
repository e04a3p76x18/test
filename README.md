# sedna
Linux c gtk packet filtering firewall 


For the application to receive queued packets from the kernel iptables rules need to be added, for example to filter incoming and outgoing udp packets from userspace application add the following iptables rules 

iptables -I OUTPUT -p udp  -j NFQUEUE -v

iptables -I INPUT -p udp  -j NFQUEUE -v

## Features ##

Application level firewall for blocking packets at network level includes support for filtering packets by protocol, process, domain, ip, port 

When a process attempts to open a incoming or outgoing connection on the network, the application will display a connection alert, allowing the user to allow or block the connection.

<p>
<img src="/screenshot.png" />
</p>

## Build ##
requires libnetfilter_queue
