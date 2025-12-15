## Descripción
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/212/disk.flag.img.gz)
## Solución
```
mkdir /tmp/...oporch/
FRAY30-picoctf@webshell:~/oporch$ cd /tmp/...oporch/
FRAY30-picoctf@webshell:/tmp/...oporch$ wget https://artifacts.picoctf.net/c/212/disk.flag.img.gz
--2025-12-15 05:51:59--  https://artifacts.picoctf.net/c/212/disk.flag.img.gz
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.18, 3.170.131.33, 3.170.131.77, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 44360923 (42M) [application/octet-stream]
Saving to: 'disk.flag.img.gz'

disk.flag.img.gz  100%[===========>]  42.31M  1.82MB/s    in 23s     

2025-12-15 05:52:22 (1.82 MB/s) - 'disk.flag.img.gz' saved [44360923/44360923]

FRAY30-picoctf@webshell:/tmp/...oporch$ ls
disk.flag.img.gz
FRAY30-picoctf@webshell:/tmp/...oporch$ gunzip disk.flag.img.gz 
FRAY30-picoctf@webshell:/tmp/...oporch$ ls
disk.flag.img
FRAY30-picoctf@webshell:/tmp/...oporch$ file disk.flag.img 
disk.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0xc,223,19), startsector 2048, 204800 sectors; partition 2 : ID=0x82, start-CHS (0xc,223,20), end-CHS (0x19,159,6), startsector 206848, 204800 sectors; partition 3 : ID=0x83, start-CHS (0x19,159,7), end-CHS (0x32,253,11), startsector 411648, 407552 sectors
FRAY30-picoctf@webshell:/tmp/...oporch$ mmls disk.flag.img 
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000206847   0000204800   Linux (0x83)
003:  000:001   0000206848   0000411647   0000204800   Linux Swap / Solaris x86 (0x82)
004:  000:002   0000411648   0000819199   0000407552   Linux (0x83)
FRAY30-picoctf@webshell:/tmp/...oporch$ fls disk.flag.img -o 2048
d/d 11: lost+found
r/r 12: ldlinux.sys
r/r 13: ldlinux.c32
r/r 15: config-virt
r/r 16: vmlinuz-virt
r/r 17: initramfs-virt
l/l 18: boot
r/r 20: libutil.c32
r/r 19: extlinux.conf
r/r 21: libcom32.c32
r/r 22: mboot.c32
r/r 23: menu.c32
r/r 14: System.map-virt
r/r 24: vesamenu.c32
V/V 25585:      $OrphanFiles
FRAY30-picoctf@webshell:/tmp/...oporch$ fls disk.flag.img -o 206848
Cannot determine file system type
FRAY30-picoctf@webshell:/tmp/...oporch$ fls disk.flag.img -o 411648
d/d 460:        home
d/d 11: lost+found
d/d 12: boot
d/d 13: etc
d/d 81: proc
d/d 82: dev
d/d 83: tmp
d/d 84: lib
d/d 87: var
d/d 96: usr
d/d 106:        bin
d/d 120:        sbin
d/d 466:        media
d/d 470:        mnt
d/d 471:        opt
d/d 472:        root
d/d 473:        run
d/d 475:        srv
d/d 476:        sys
d/d 2041:       swap
V/V 51001:      $OrphanFiles
FRAY30-picoctf@webshell:/tmp/...oporch$ fls disk.flag.img 472 -o 41164
8
r/r 1875:       .ash_history
r/r * 1876(realloc):    flag.txt
r/r 1782:       flag.txt.enc
FRAY30-picoctf@webshell:/tmp/...oporch$ icat -o 411648 1876
Missing image name and/or address
usage: icat [-hrRsvV] [-f fstype] [-i imgtype] [-b dev_sector_size] [-o imgoffset] image [images] inum[-typ[-id]]
        -h: Do not display holes in sparse files
        -r: Recover deleted file
        -R: Recover deleted file and suppress recovery errors
        -s: Display slack space at end of file
        -i imgtype: The format of the image file (use '-i list' for supported types)
        -b dev_sector_size: The size (in bytes) of the device sectors
        -f fstype: File system type (use '-f list' for supported types)
        -o imgoffset: The offset of the file system in the image (in sectors)
        -P pooltype: Pool container type (use '-P list' for supported types)
        -B pool_volume_block: Starting block (for pool volumes only)
        -S snap_id: Snapshot ID (for APFS only)
        -v: verbose to stderr
        -V: Print version
        -k password: Decryption password for encrypted volumes
FRAY30-picoctf@webshell:/tmp/...oporch$ icat -o 411648 disk.flag.img 1
876
           -0.881573            34.311733
FRAY30-picoctf@webshell:/tmp/...oporch$ icat -o 411648 disk.flag.img 1782
Salted__0!-6V0Ul&:pj_10|h
FRAY30-picoctf@webshell:/tmp/...oporch$ icat -o 411648 disk.flag.img 1875
touch flag.txt
nano flag.txt 
apk get nano
apk --help
apk add nano
nano flag.txt 
openssl
openssl aes256 -salt -in flag.txt -out flag.txt.enc -k unbreakablepassword1234567
shred -u flag.txt
ls -al
halt
FRAY30-picoctf@webshell:/tmp/...oporch$ icat -o 411648 disk.flag.img 1782 > flag.txt.enc
FRAY30-picoctf@webshell:/tmp/...oporch$ ls
disk.flag.img  flag.txt.enc
FRAY30-picoctf@webshell:/tmp/...oporch$ openssl aes256 -d -salt -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
80AB42B5CF7F0000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:124:
FRAY30-picoctf@webshell:/tmp/...oporch$ ls
disk.flag.img  flag.txt  flag.txt.enc
FRAY30-picoctf@webshell:/tmp/...oporch$ cat flag.txt
picoCTF{h4un71ng_p457_0a710765}
```
## Notas adicionales

## Referencias
