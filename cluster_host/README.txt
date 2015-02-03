Setup for local test cluster. Except for the ssh key setup, you only need to
do this on the "main" machine, which will control the others.

(*) Create the directory /root/src/drill, and git clone your drill repo into it
- this will be where your repo is pulled

(*) Install maven
- simple instructions here: http://preilly.me/2013/05/10/how-to-install-maven-on-centos/

(*) Set up ssh keys (without a passphrase) on the nodes in the cluster with
ssh-keygen, so that a password is not required when logging in from one node
to another in the cluster.
 - simple instructions here if you need them: https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2

(*) Steps for various directories:
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
