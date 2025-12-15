## Descripción
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.[Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)Access checker program: `nc saturn.picoctf.net 59352`
## Solución
```
mkdir /tmp/...sle/ 
FRAY30-picoctf@webshell:~$ cd /tmp/...sle/
FRAY30-picoctf@webshell:/tmp/...sle$ wget https://artifacts.picoctf.net/c/164/disk.img.gz
--2025-12-15 05:32:43--  https://artifacts.picoctf.net/c/164/disk.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.77, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 29714372 (28M) [application/octet-stream]
Saving to: 'disk.img.gz'

disk.img.gz       100%[===========>]  28.34M  1.82MB/s    in 16s     

2025-12-15 05:32:58 (1.82 MB/s) - 'disk.img.gz' saved [29714372/29714372]

FRAY30-picoctf@webshell:/tmp/...sle$ gunzip disk.img.gz 
FRAY30-picoctf@webshell:/tmp/...sle$ ls
disk.img
FRAY30-picoctf@webshell:/tmp/...sle$ file disk.img 
disk.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0xc,190,50), startsector 2048, 202752 sectors
FRAY30-picoctf@webshell:/tmp/...sle$ mmls disk.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)
FRAY30-picoctf@webshell:/tmp/...sle$ nc saturn.picoctf.net 59352
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
picoCTF{mm15_f7w!}
```

## Notas adicionales

## Referencias
