## Descripción
This is a really weird text file. Can you find the flag?Get the flag from [TXT](https://challenge-files.picoctf.net/c_fickle_tempest/31fe772e6a4c71e867af0b2a93818e06d8f8ebf8af2a9615495d00356ff576da/flag.txt).
## Solución
```
mkdir extensions
FRAY30-picoctf@webshell:~$ cd extensions/
FRAY30-picoctf@webshell:~/extensions$ wget https://challenge-files.picoctf.net/c_fickle_tempest/31fe772e6a4c71e867af0b2a93818e06d8f8ebf8af2a9615495d00356ff576da/flag.txt
--2025-12-14 20:07:53--  https://challenge-files.picoctf.net/c_fickle_tempest/31fe772e6a4c71e867af0b2a93818e06d8f8ebf8af2a9615495d00356ff576da/flag.txt
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.18, 3.160.5.40, 3.160.5.64, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9984 (9.8K) [application/octet-stream]
Saving to: 'flag.txt'

flag.txt          100%[===========>]   9.75K  --.-KB/s    in 0s      

2025-12-14 20:07:53 (342 MB/s) - 'flag.txt' saved [9984/9984]

FRAY30-picoctf@webshell:~/extensions$ ls
flag.txt
FRAY30-picoctf@webshell:~/extensions$ file flag.txt 
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
FRAY30-picoctf@webshell:~/extensions$ mv flag.txt flag.png
FRAY30-picoctf@webshell:~/extensions$ ls
flag.png
FRAY30-picoctf@webshell:~/extensions$ file flag.png 
flag.png: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
FRAY30-picoctf@webshell:~/extensions$ sz flag.png
```

picoCTF{now_you_know_about_extensions}
## Notas adicionales

## Referencias
