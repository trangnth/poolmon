Poolmon is a director mailserver pool monitoring script for Dovecot, meant to
roughly duplicate the functionality of node health monitors on dedicated load-
balancers like LVS or F5 BigIP LTM. This script can be safely run on more than
one director host simultaneously, although differences in node reachability may
result in mailserver vhost count flapping.

Consult the help text for more details on functionality.


## Install Dependency

* Centos 7

```sh
yum install perl -y
yum install perl-IO-Socket-INET6 perl-Socket6 -y
yum install perl-libwww-perl.noarch perl-Time-HiRes perl-core -y
rpm -qa | grep -i perl-5.16
perl -v
```

## Running script

```sh
perl poolmon
bash redhat/poolmon.init start
```

## Check status 

```sh
[root@trangnth-mailserver poolmon]# bash redhat/poolmon.init status
poolmon (pid  20086) is running...
```
