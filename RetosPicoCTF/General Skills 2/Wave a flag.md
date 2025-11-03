## Descripción
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm) has extraordinarily helpful information...
## Solución
```
FRAY30-picoctf@webshell:~$ mkdir waf
FRAY30-picoctf@webshell:~$ cd waf/
FRAY30-picoctf@webshell:~/waf$ wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm
--2025-11-03 01:00:49--  https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm              100%[===========>]  10.68K  --.-KB/s    in 0s      

2025-11-03 01:00:49 (222 MB/s) - 'warm' saved [10936/10936]

FRAY30-picoctf@webshell:~/waf$ ls
warm
FRAY30-picoctf@webshell:~/waf$ ls -la
total 16
drwxrwxr-x 2 FRAY30-picoctf FRAY30-picoctf    26 Nov  3 01:00 .
drwxr-xr-x 9 FRAY30-picoctf FRAY30-picoctf  4096 Nov  3 00:59 ..
-rw-rw-r-- 1 FRAY30-picoctf FRAY30-picoctf 10936 Mar 16  2021 warm
FRAY30-picoctf@webshell:~/waf$ file warm
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=3aa19b2a9cc4e093d64025eab8f510679b523455, with debug_info, not stripped
FRAY30-picoctf@webshell:~/waf$ chmod +x warm
FRAY30-picoctf@webshell:~/waf$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_30e77291}
```
## Notas adicionales

## Referencias