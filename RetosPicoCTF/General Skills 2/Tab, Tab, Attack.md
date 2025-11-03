## Descripción
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/e38f6a5b69b45d21e33cf7281d8c2531/Addadshashanammu.zip)
## Solución
```
FRAY30-picoctf@webshell:~$ pwd
/home/FRAY30-picoctf
FRAY30-picoctf@webshell:~$ mkdir tabtab
FRAY30-picoctf@webshell:~$ cd tabtab
FRAY30-picoctf@webshell:~/tabtab$ pwd
/home/FRAY30-picoctf/tabtab
FRAY30-picoctf@webshell:~/tabtab$ wget https://mercury.picoctf.net/static/e38f6a5b69b45d21e33cf7281d8c2531/Addadshashanammu.zip
--2025-11-02 22:50:20--  https://mercury.picoctf.net/static/e38f6a5b69b45d21e33cf7281d8c2531/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4521 (4.4K) [application/octet-stream]
Saving to: 'Addadshashanammu.zip'

Addadshashanammu.zip                100%[===================================================================>]   4.42K  --.-KB/s    in 0s      

2025-11-02 22:50:20 (2.15 GB/s) - 'Addadshashanammu.zip' saved [4521/4521]

FRAY30-picoctf@webshell:~/tabtab$ pwd
/home/FRAY30-picoctf/tabtab
FRAY30-picoctf@webshell:~/tabtab$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
FRAY30-picoctf@webshell:~/tabtab$ cd Addadshashanammu/
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu$ ls
Almurbalarammi
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu$ cd Almurbalarammi/
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi$ ls
Ashalmimilkala
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi$ cd Ashalmimilkala/
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala$ ls
Assurnabitashpi
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala$ cd Assurnabitashpi/
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi$ ls
Maelkashishi
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi$ cd Maelkashishi/
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi$ ls
Onnissiralis
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi$ cd Onnissiralis/
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ ls
Ularradallaku
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis$ cd Ularradallaku/
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls -la
total 12
drwxr-xr-x 2 FRAY30-picoctf FRAY30-picoctf   35 Mar 16  2021 .
drwxr-xr-x 3 FRAY30-picoctf FRAY30-picoctf   27 Mar 16  2021 ..
-rwxr-xr-x 1 FRAY30-picoctf FRAY30-picoctf 8320 Mar 16  2021 fang-of-haynekhtnamet
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ cat fang-of-haynekhtnamet 
 HH/lib64/ld-linux-x86-64.so.2GNUGNUUTg(ї.X= 
8#TT 1tt$DN                                  Y h "libc.so.6puts__cxa_finalize__libc_start_mainGLIBC_2.2.5_ITM_deregisterTMCloneTable__gmon_start
0)@    H(;FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ 
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ 
FRAY30-picoctf@webshell:~/tabtab/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_f3553887}
```
## Notas adicionales

## Referencias