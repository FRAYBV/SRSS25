## Descripción
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
## Solución
```
mkdir rupy
FRAY30-picoctf@webshell:~$ cd rupy/
FRAY30-picoctf@webshell:~/rupy$ pwd
/home/FRAY30-picoctf/rupy
FRAY30-picoctf@webshell:~/rupy$ wget https://artifacts.picoctf.net/c/34/runme.py
--2025-11-03 04:04:01--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.18, 3.170.131.77, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py          100%[===========>]     270  --.-KB/s    in 0s      

2025-11-03 04:04:02 (11.9 MB/s) - 'runme.py' saved [270/270]

FRAY30-picoctf@webshell:~/rupy$ ls
runme.py
FRAY30-picoctf@webshell:~/rupy$ cat runme.py 
#!/usr/bin/python3
################################################################################
# Python script which just prints the flag
################################################################################

flag ='picoCTF{run_s4n1ty_run}'
print(flag)

FRAY30-picoctf@webshell:~/rupy$ python runme.py 
picoCTF{run_s4n1ty_run}
```
## Notas adicionales

## Referencias