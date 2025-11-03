## Descripción
Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/22/convertme.py)
## Solución
```
mkdir cvm
FRAY30-picoctf@webshell:~$ cd cvm/
FRAY30-picoctf@webshell:~/cvm$ wget https://artifacts.picoctf.net/c/22/convertme.py
--2025-11-03 05:00:13--  https://artifacts.picoctf.net/c/22/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.77, 3.170.131.33, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py      100%[===========>]   1.16K  --.-KB/s    in 0s      

2025-11-03 05:00:13 (43.5 MB/s) - 'convertme.py' saved [1189/1189]

FRAY30-picoctf@webshell:~/cvm$ python convertme.py 
If 25 is in decimal base, what is it in binary base?
Answer: 11001
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_762f748e}
```
## Notas adicionales

## Referencias