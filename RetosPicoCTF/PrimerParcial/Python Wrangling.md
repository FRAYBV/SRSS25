## Descripción
Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/ende.py) using [this password](https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/pw.txt) to get [the flag](https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/flag.txt.en)?
## Solución
```
wget https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/ende.py
--2025-10-09 20:54:11--  https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/ende.py
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1328 (1.3K) [application/octet-stream]
Saving to: 'ende.py'

ende.py                             100%[===================================================================>]   1.30K  --.-KB/s    in 0s      

2025-10-09 20:54:11 (773 MB/s) - 'ende.py' saved [1328/1328]

FRAY30-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/pw.txt 
--2025-10-09 20:55:17--  https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/pw.txt
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 33 [application/octet-stream]
Saving to: 'pw.txt'

pw.txt                              100%[===================================================================>]      33  --.-KB/s    in 0s      

2025-10-09 20:55:17 (12.6 MB/s) - 'pw.txt' saved [33/33]

FRAY30-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/flag.txt.en
--2025-10-09 20:57:43--  https://mercury.picoctf.net/static/325a52d249be0bd3811421eacd2c877a/flag.txt.en
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 140 [application/octet-stream]
Saving to: 'flag.txt.en'

flag.txt.en                         100%[===================================================================>]     140  --.-KB/s    in 0s      

2025-10-09 20:57:43 (125 MB/s) - 'flag.txt.en' saved [140/140]

FRAY30-picoctf@webshell:~$ cat pw.txt
ac9bd0ffac9bd0ffac9bd0ffac9bd0ff
FRAY30-picoctf@webshell:~$ python3 ende.py
Usage: ende.py (-e/-d) [file]
FRAY30-picoctf@webshell:~$ -d flag.txt.en
-bash: -d: command not found
FRAY30-picoctf@webshell:~$ python3 ende.py -d flag.txt.en
Please enter the password:ac9bd0ffac9bd0ffac9bd0ffac9bd0ff
picoCTF{4p0110_1n_7h3_h0us3_ac9bd0ff}
```
## Notas adicionales

## Referencias
