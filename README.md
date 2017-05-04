# autossh-systemd
Systemd .service file for autossh (reverse tunneling)

How to setup persistent reverse tunnel with autossh:

Make sure first to create autossh user on remote (behind firewall) machine

[user@remote ~]$ sudo useradd -m -s /sbin/nologin autossh
[user@remote ~]$ sudo su autossh -s /bin/bash
[autossh@remote ~]$ ssh-keygen -t rsa

Make sure to create autossh user on home (in front of firewall) machine

[user@homeserver01 ~]$ useradd -m -s /bin/bash autossh
[user@homeserver01 ~]$ sudo passwd autossh



[autossh@remoteserver ~]$ ssh-copy-id -i ~/.ssh/id_rsa homeserver01
[autossh@remoteserver ~]$ 
