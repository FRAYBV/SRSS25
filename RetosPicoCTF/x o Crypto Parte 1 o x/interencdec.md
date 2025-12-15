## Descripción
Can you get the real meaning from this file.Download the file [here](https://artifacts.picoctf.net/c_titan/111/enc_flag).
## Solución
```
mkdir /tmp/...interencdec/
FRAY30-picoctf@webshell:~$ cd /tmp/...interencdec/
FRAY30-picoctf@webshell:/tmp/...interencdec$ wget https://artifacts.picoctf.net/c_titan/111/enc_flag
--2025-12-15 10:10:21--  https://artifacts.picoctf.net/c_titan/111/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.18, 3.170.131.33, 3.170.131.77, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 73 [application/octet-stream]
Saving to: 'enc_flag'

enc_flag          100%[===========>]      73  --.-KB/s    in 0s      

2025-12-15 10:10:21 (17.3 MB/s) - 'enc_flag' saved [73/73]

FRAY30-picoctf@webshell:/tmp/...interencdec$ ls
enc_flag
FRAY30-picoctf@webshell:/tmp/...interencdec$ base64 -d enc_flag 
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg5MGsyMzc5fQ=='
```
base 64 decoder: wpjvJAM{jhlzhy_k3jy9wa3k_890k2379}
rot13caesarcipher: picoCTF{caesar_d3cr9pt3d_890d2379}
## Notas adicionales

## Referencias
