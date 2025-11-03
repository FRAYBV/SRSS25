## Descripción
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)
## Solución
```
mkdir cbok
FRAY30-picoctf@webshell:~$ cd cbok/
FRAY30-picoctf@webshell:~/cbok$ wget https://artifacts.picoctf.net/c/2/code.py
--2025-11-03 04:55:18--  https://artifacts.picoctf.net/c/2/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.72, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py           100%[===========>]   1.25K  --.-KB/s    in 0s      

2025-11-03 04:55:18 (1.13 GB/s) - 'code.py' saved [1278/1278]

FRAY30-picoctf@webshell:~/cbok$ wget https://artifacts.picoctf.net/c/2/codebook.txt
--2025-11-03 04:55:39--  https://artifacts.picoctf.net/c/2/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.18, 3.170.131.77, 3.170.131.33, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt      100%[===========>]      27  --.-KB/s    in 0s      

2025-11-03 04:55:40 (30.9 MB/s) - 'codebook.txt' saved [27/27]

FRAY30-picoctf@webshell:~/cbok$ ls
code.py  codebook.txt
FRAY30-picoctf@webshell:~/cbok$ python code.py codebook.txt
picoCTF{c0d3b00k_455157_7d102d7a}
```
## Notas adicionales

## Referencias