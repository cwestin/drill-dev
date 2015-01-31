Setup for local test cluster. You only need to do this on the "main" machine,
which will control the others.

Create the directory /root/src/drill
- this will be where your repo is pulled

bin
- scripts for controlling your cluster
- link to from /root/bin

bin/cluster.conf
- modify this to list the IP addresses in your cluster
- other scripts in this directory refer to this

clustershell_conf/groups
- modify this file so that it contains the IP addresses of your cluster members
- link to from /etc/clustershell/groups

drill_conf
- link to this directory from /etc/drill/conf

drill_conf/logback.xml
- modify this file to change the username (currently cwestin) to your username

drill_conf/runtests
- modify this file to change the username
