## Descripción
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/626ea9c275fbd02dd3451b81f9c5e249/dds1-alpine.flag.img.gz)
## Solución
```
mkdir /tmp/...ddsl/
FRAY30-picoctf@webshell:~$ cd /tmp/...ddsl/
FRAY30-picoctf@webshell:/tmp/...ddsl$ wget https://mercury.picoctf.net/static/626ea9c275fbd02dd3451b81f9c5e249/dds1-alpine.flag.img.gz
--2025-12-15 05:46:39--  https://mercury.picoctf.net/static/626ea9c275fbd02dd3451b81f9c5e249/dds1-alpine.flag.img.gz
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29768910 (28M) [application/octet-stream]
Saving to: 'dds1-alpine.flag.img.gz'

dds1-alpine.flag. 100%[===========>]  28.39M  1.82MB/s    in 16s     

2025-12-15 05:46:55 (1.82 MB/s) - 'dds1-alpine.flag.img.gz' saved [29768910/29768910]

FRAY30-picoctf@webshell:/tmp/...ddsl$ ls
dds1-alpine.flag.img.gz
FRAY30-picoctf@webshell:/tmp/...ddsl$ gunzip dds1-alpine.flag.img.gz 
FRAY30-picoctf@webshell:/tmp/...ddsl$ ls
dds1-alpine.flag.img
FRAY30-picoctf@webshell:/tmp/...ddsl$ file dds1-alpine.flag.img 
dds1-alpine.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0x10,81,1), startsector 2048, 260096 sectors
FRAY30-picoctf@webshell:/tmp/...ddsl$ srch_strings dds1-alpine.flag.img | grep pico
ffffffff81399ccf t pirq_pico_get
ffffffff81399cee t pirq_pico_set
ffffffff820adb46 t pico_router_probe
  SAY picoCTF{f0r3ns1c4t0r_n30phyt3_a6f4cab5}
```
## Notas adicionales

## Referencias
