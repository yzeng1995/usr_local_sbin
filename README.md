# Network Security System Scripts

Author:Yan Zeng

E-mail:zengyan16@mails.ucas.edu.cn

License:MIT

This is a set of system scripts, which is used to
ensure server security in the public internet.

The scripts can run on Centos7 system.

# Functions
## deny_ssh_hosts.sh

This script analysis /var/log/secure file to find the
ip address whose the number of failed times is greater
than 5.

Then the script add the ipaddress to /etc/hosts.deny
to reject ssh connection.

## drop_ssh_hosts_local.sh
This script find the ip do the following things

1.Add the ip to firewall drop zone.<br>
2.Add the ip to firewall ipset ssh_drop --permanent<br>
3.This script will NOT add the ip which is already in ipset ssh_drop.<br>

## drop_ssh_hosts_public.sh
If you have a ip list from internet and you want to
drop them, then you can save the ip address in a file
at /var/log/drop_ssh_hosts_public.

Run this script you can add the ip address in
the drop zone in firewall.

This script will NOT add the ip which is already in firewall drop zone.



