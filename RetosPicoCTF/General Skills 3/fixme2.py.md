## Descripción
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/4/fixme2.py)
## Solución
```
mkdir fxm2
FRAY30-picoctf@webshell:~$ cdfxm2/
-bash: cdfxm2/: No such file or directory
FRAY30-picoctf@webshell:~$ pwd
/home/FRAY30-picoctf
FRAY30-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/4/fixme2.py
--2025-11-03 04:27:46--  https://artifacts.picoctf.net/c/4/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.33, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py         100%[===========>]   1.00K  --.-KB/s    in 0s      

2025-11-03 04:27:46 (991 MB/s) - 'fixme2.py' saved [1029/1029]

FRAY30-picoctf@webshell:~$  python f
firstfind/ fixme2.py  fxm1/      fxm2/      
FRAY30-picoctf@webshell:~$ python fixme2.py
  File "/home/FRAY30-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
FRAY30-picoctf@webshell:~$ nano fixme2.py

(Se corrige:
if flag == "":
)

FRAY30-picoctf@webshell:~$ python fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
```
## Notas adicionales

## Referencias