#Use ddclient with no-ip.com

August 14, 2013

DynDns, no-ip.com, Pi, Raspberry


I wanted to use a Raspberry Pi to keep track of the IP address of a server running on a domestic internet connection which is frequently changed by the ISP. I’m a paying DynDns customer, but I don’t want my account password to be stored on the Pi in case it’s compromised. Previously, I used alternative free DynDns accounts for this purpose, but Dyn have recently withdrawn them.

I searched around for alternatives and found no-ip.com which has  it’s own dynamic update client. Apparently, their client is included in the source tree on some versions of Ubuntu. I’m running Debian “wheezy” on a Raspberry Pi, so there were two choices:

1. Attempt to build the no-ip update client from source. This is a maintenance headache, if a security update is released, I’m not going to know about it. Even if I did know about it, I still need to log in and rebuild the client.

2. Try and find a client in the debian source tree that works with no-ip.com

Fortunately, Dyndns and no-ip support the same protocol.  It was possible to use the same ddclient that I’ve previously used with DynDns. Here’s the config:



    # /etc/ddclient.conf

    protocol=dyndns2
    use=web, web=checkip.dyndns.com/, web-skip='IP Address'
    server=dynupdate.no-ip.com
    login=mylogin
    password='mypassword'
    myhost.no-ip.biz

