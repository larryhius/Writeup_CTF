# CTF Collection Vol 1

# Tasks

1. Can you decode the following?

VEhNe2p1NTdfZDNjMGQzXzdoM19iNDUzfQ==

```
THM{ju57_d3c0d3_7h3_b453}
```

2. Meta! meta! meta! meta...................................

I'm hungry, I need the flag

```
exiftool Findme.jpg

THM{3x1f_0r_3x17}
```

3. Something is hiding. That's all you need to know.

It is sad. Feed me the flag.

```
steghide --extract -sf Extinction.jpg

THM{500n3r_0r_l473r_17_15_0ur_7urn}
```

4. Huh, where is the flag? THM{wh173_fl46}
Answer the questions below

Did you find the flag?

```
# Flag with white color font

THM{wh173_fl46}
```

5. Such technology is quite reliable.

More flag please!

```
# QR scanner

THM{qr_m4k3_l1f3_345y}
```

6. Both works, it's all up to you.

Found the flag?

```
strings hello.hello

THM{345y_f1nd_345y_60}
```

7. Can you decode it?

3agrSy1CewF9v8ukcSkPSYm3oKUoByUpKG4L

Oh, Oh, Did you get it?

```
# base58 decrypt

THM{17_h45_l3553r_l3773r5}
```

8. Left, right, left, right... Rot 13 is too mainstream. Solve this

MAF{atbe_max_vtxltk}

What did you get?

```
# ROT7

THM{hail_the_caesar}
```

9. No downloadable file, no ciphered or encoded text. Huh .......

I'm hungry now... I need the flag

```
# comment line

THM{4lw4y5_ch3ck_7h3_c0m3mn7}
```

10. I accidentally messed up with this PNG file. Can you help me fix it? Thanks, ^^

What is the content?

```
# Change file to hex
xxd -p spoil.png > spoil_hex.txt

# Magic number of png file
89504E47

# Replace the 8 first digits in header with magic number

89504E470d0a1a0a0000000d4948445200000320000003200806000000db
700668000000017352474200aece1ce9000000097048597300000ec40000
0ec401952b0e1b0000200049444154789cecdd799c9c559deff1cf799e5a
bb7a5f927477f640480209201150c420bba288a8805c19067c5d64c079e9
752e03ce38e30e8e2f75e63a23ea8c0ce8308e036470c191cd80880c4b20
0909184c42b64ed2e9f4bed7f23ce7fe51559dea4e27a4bbaaf7effbf5ea
57d2d5554f9daa7abafa7ceb9cf33bc65a6b1111111111111907ce443740
4444444444660e0510111111111119370a202222222222326e1440444444
444464dc28808888888888c8b8510011111111119171a300222222222222
e34601444444444444c68d028888888888888c1b0510111111111119370a
```
11. Some hidden flag inside Tryhackme social account.

Did you found the hidden flag?

```
THM{50c14l_4cc0un7_15_p4r7_0f_051n7}
```

12. What is this?

++++++++++[>+>+++>+++++++>++++++++++<<<<-]>>>++++++++++++++.------------.+++++.>+++++++++++++++++++++++.<<++++++++++++++++++.>>-------------------.---------.++++++++++++++.++++++++++++.<++++++++++++++++++.+++++++++.<+++.+.>----.>++++.

Can you decode it?

```
# Brainfuck decode

THM{0h_my_h34d}
```

13. Exclusive strings for everyone!

S1: 44585d6b2368737c65252166234f20626d
S2: 1010101010101010101010101010101010

Did you crack it? Feed me now!

```
# s1XORs2
```