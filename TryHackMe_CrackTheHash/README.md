# Crack The Hash


# Hash Identier

```
hashid -m <hash>
```

1. 48bb6e862e54f2a795ffc4e541caed4d 

```
Type: md5 
hashcat -m 0 hash1
Result: easy
```

2. CBFDAC6008F9CAB4083784CBD1874F76618D2A97

```
Type: sha1 
hashcat -m 100 hash2
Result: password123
```

3. 1C8BFE8F801D79745C4631D09FFF36C82AA37FC4CCE4FC946683D7B336B63032

```
Type: sha256
hashcat -m 1400 hash3
Result: letmein
```

4. $2y$12$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX1H68wsRom

```
Type: bcrypt $2*$, Blowfish (Unix) 
hashcat -m 3200 hash4
Result: 
```

5. 279412f945939ba78ce0758d3fd83daa

```
Tt
```