## Descripción
Download this disk image and find the flag.Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/137/disk.flag.img.gz)
## Solución
```
icat -f ext4 -o 360448 disk.flag.img  2082
            3.449677            13.056403
FRAY30-picoctf@webshell:/tmp/...sleapp$ icat -f ext4 -o 360448 disk.flag.img  2371
picoCTF{by73_5urf3r_adac6cb4}
```
## Notas adicionales

## Referencias
