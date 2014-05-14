This is ansible recipe to common configuration Debian.

It's include:

* set hostname from hosts file
* set locale from config
* set timezone from config
* set ntp
* create users with ssh-keys to automatic login
* disable login root by ssh
* setup iptables 
* set exim to send mail via gmail from config

Before run you need:

1) create secret file with email and password
```ansible-vault create vars/secret.yml```
 (example file vars/secret.yml.example)

2) create file with hosts in role common, like this:
```
[common]
test.example.com
```

3) change params hostfile to hosts file in ansible.cfg



Now you can run:
```ansible-playbook common.yml --ask-vault-pass```