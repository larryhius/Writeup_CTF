# Biohazard-SSH login expose&root login expose

```
export IP=10.10.96.31
```

# Material needed

1. Interesting directory: /diningRoom, /teaRoom, /artRoom, /barRoom, /diningRoom2F, /tigerStatusRoom, /galleryRoom, /studyRoom, /armorRoom, /attic

2. FTP user: hunter, FTP pass: you_cant_hide_forever

3. Reverse engineering

```
# 001-key.jpg
steghide --extract -sf 001-key.jpg

Result: cGxhbnQ0Ml9jYW

# 002-key.jpg
exiftool 002-key.jpg

Comment: 5fYmVfZGVzdHJveV9

# 003-key.jpg
binwalk 003-key.jpg -e

Result: 3aXRoX3Zqb2x0

# helmet-key.txt.gpg
gpg -d helmet-key.txt.gpg
passphrase: plant42_can_be_destroy_with_vjolt 
Result: helmet_key{458493193501d2b94bbab2e727f8db4b}
```                                                                               
4. SSH user: umbrella_guest, SSH password: T_virus_rules

# Tasks

1. How many open ports? 3

2. What is the team name in operation? STARS alpha team

3. What is the emblem flag

```
emblem{fec832623ea498e20bf4fe1821d58727}
```

4. What is the lock pick flag

```
lock_pick{037b35e2ff90916a9abf99129c8e1837}
```

5. What is the music sheet flag

```
music_sheet{362d72deaf65f5bdc63daece6a1f676e}
```

6. What is the gold emblem flag

```
gold_emblem{58a8c41a9d08b8a4e38d02a4d7ff4843}
```

7. What is the shield key flag

```
shield_key{48a7a9227cd7eb89f0a062590798cbac}
```

8. What is the blue gem flag

```
blue_jewel{e1d457e96cac640f863ec7bc475d48aa}
```

9. What is the FTP username

```
hunter
```

10. what is the FTP Password

```
you_cant_hide_forever
```

11. Where is the hidden directory mentioned by Barry

```
/hidden_closet/
```

12. Password for the encrypted file

```
plant42_can_be_destroy_with_vjolt
```

13. What is the helmet key flag

```
helmet_key{458493193501d2b94bbab2e727f8db4b}
```

14. What is the SSH login username

```
umbrella_guest
```

15. What is the SSH login password

```
T_virus_rules
```

16. Who the STARS bravo team leader

```
enrico
```

17. where you found Chris

```
jailcell
```

18. Who is the traitor

```
weasker
```

19. The login password for the traitor

```
stars_members_are_my_guinea_pig
```

20. The name of the ultimate form

```
Tyrant
```

21. The root flag

```
3c5794a00dc56c35f2bf096571edf3bf
```