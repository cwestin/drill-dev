Setup for local test cluster. Some steps are for all hosts, and some only need
to be carried out on the cluster master/controller -- each step says.

(*) Create the directory /root/src/drill, and git clone your drill repo into it
- this will be where your repo is pulled
- do this on all cluster members (you'll need the config files on all members)

(*) Create /var/log/drill for logfiles
- do this on all the members of the cluster

(*) Set up ssh keys (without a passphrase) on the nodes in the cluster with
ssh-keygen, so that a password is not required when logging in from one node
to another in the cluster.
- do this on all cluster members
 - simple instructions here if you need them: https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2
   - make sure to give the master access to itself in this way as well

(*) Install maven
- simple instructions here: http://preilly.me/2013/05/10/how-to-install-maven-on-centos/
- only need to do this on the cluster master

(*) Steps for various directories from the git repo:
bin/cluster.conf
- modify this to list the IP addresses in your cluster
- other scripts in this directory refer to this

bin
- scripts for controlling your cluster
- link to from /root/bin on the cluster master

clustershell_conf/groups
- modify this file so that it contains the IP addresses of your cluster members
- link to from /etc/clustershell/groups on the cluster master

drill_conf/logback.xml
- modify this file to change the username (currently cwestin) to your username

drill_conf/runtests
- modify this file to change the username

drill_conf
- link to this directory from /etc/drill/conf
- do this on all the members of the cluster
