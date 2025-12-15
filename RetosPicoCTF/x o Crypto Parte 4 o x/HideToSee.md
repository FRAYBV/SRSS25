## Descripción
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/235/atbash.jpg).
## Solución
```
wget https://artifacts.picoctf.net/c/235/atbash.jpg
--2025-12-15 14:07:17--  https://artifacts.picoctf.net/c/235/atbash.jpg
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.18, 3.170.131.72, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 51499 (50K) [application/octet-stream]
Saving to: 'atbash.jpg'

atbash.jpg        100%[===========>]  50.29K  --.-KB/s    in 0.02s   

2025-12-15 14:07:17 (2.64 MB/s) - 'atbash.jpg' saved [51499/51499]

FRAY30-picoctf@webshell:/tmp/...hitosee$ strings atbash.jpg
FRAY30-picoctf@webshell:/tmp/...hitosee$ steghide extract -sf atbash.jpg 
Enter passphrase: 
wrote extracted data to "encrypted.txt".
FRAY30-picoctf@webshell:/tmp/...hitosee$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_92533667}
```
cyberchef atbash cipher: picoCTF{atbash_crack_92533667}
## Notas adicionales

## Referencias
