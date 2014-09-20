pyfetch
=======

prefetch/warm cache http requests based on squid log file

This is a initial commit and experimental, use it at your own risk.

This is a python based project, the instructions below assumes that you are familiar with python

You should have squid installed and running already.

I tested on an ubuntu 14.04 with squid as a transparent proxy

Install/run:

Add port 3129 to squid.conf:
http_port 3129
Since I am using squid as a trasnparent proxy, acessing the proxy from localhost was causing a loop and squid was returning 403

create a virtualenv and install the requirements on requirements.txt

run 'python pyfetch.py'

It assumes your squid logfile is /var/log/squid3/access.log

Configure:

edit the regex 'link_pattern', to determine what is a link
edit 'fetch_pattern' to determine whick links should be fetched

Any suggestion is appreciated
