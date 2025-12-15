## Descripción
Download this image and find the flag.

- [Download image](https://artifacts.picoctf.net/c/216/pico.flag.png)
## Solución
```
wget https://artifacts.picoctf.net/c/216/pico.flag.png
--2025-12-15 12:37:49--  https://artifacts.picoctf.net/c/216/pico.flag.png
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.18, 3.170.131.77, 3.170.131.33, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 13441 (13K) [application/octet-stream]
Saving to: 'pico.flag.png'

pico.flag.png     100%[===========>]  13.13K  --.-KB/s    in 0.001s  

2025-12-15 12:37:49 (16.5 MB/s) - 'pico.flag.png' saved [13441/13441]

FRAY30-picoctf@webshell:/tmp/...stego$ ls
pico.flag.png
FRAY30-picoctf@webshell:/tmp/...stego$ zsteg -h
Usage: zsteg [options] filename.png [param_string]

    -a, --all                        try all known methods
    -E, --extract NAME               extract specified payload, NAME is like '1b,rgb,lsb'

Iteration/extraction params:
    -o, --order X                    pixel iteration order (default: 'auto')
                                     valid values: ALL,xy,yx,XY,YX,xY,Xy,bY,...
    -c, --channels X                 channels (R/G/B/A) or any combination, comma separated
                                     valid values: r,g,b,a,rg,bgr,rgba,r3g2b3,...
    -b, --bits N                     number of bits, single int value or '1,3,5' or range '1-8'
                                     advanced: specify individual bits like '00001110' or '0x88'
        --lsb                        least significant bit comes first
        --msb                        most significant bit comes first
    -P, --prime                      analyze/extract only prime bytes/pixels
        --shift N                    prepend N zero bits
        --invert                     invert bits (XOR 0xff)
        --pixel-align                pixel-align hidden data

Analysis params:
    -l, --limit N                    limit bytes checked, 0 = no limit (default: 256)

        --[no-]file                  use 'file' command to detect data type (default: YES)
        --no-strings                 disable ASCII strings finding (default: enabled)
    -s, --strings X                  ASCII strings find mode: first, all, longest, none
                                     (default: first)
    -n, --min-str-len X              minimum string length (default: 8)

    -v, --verbose                    Run verbosely (can be used multiple times)
    -q, --quiet                      Silent any warnings (can be used multiple times)
    -C, --[no-]color                 Force (or disable) color output (default: auto)

PARAMS SHORTCUT
        zsteg fname.png 2b,b,lsb,xy  ==>  --bits 2 --channel b --lsb --order xy
FRAY30-picoctf@webshell:/tmp/...stego$ zsteg pico.flag.png 
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_a1062667}$t3g0"
b1,abgr,lsb,xy      .. text: "E2A5q4E%uSA"
b2,b,lsb,xy         .. text: "AAPAAQTAAA"
b2,b,msb,xy         .. text: "HWUUUUUU"
b2,a,lsb,xy         .. file: Matlab v4 mat-file (little endian) >\004<\305P, numeric, rows 0, columns 0
b2,a,msb,xy         .. file: Matlab v4 mat-file (little endian) | <\243, numeric, rows 0, columns 0
b3,r,lsb,xy         .. file: gfxboot compiled html help file
b4,r,lsb,xy         .. file: Targa image data (16-273) 65536 x 4097 x 1 +4352 +4369 - 1-bit alpha - right "\021\020\001\001\021\021\001\001\021\021\001"
b4,g,lsb,xy         .. file: 0420 Alliant virtual executable not stripped
b4,b,lsb,xy         .. file: Targa image data - Map 272 x 17 x 16 +257 +272 - 1-bit alpha "\020\001\021\001\021\020\020\001\020\001\020\001"
b4,bgr,lsb,xy       .. file: Targa image data - Map 273 x 272 x 16 +1 +4113 - 1-bit alpha "\020\001\001\001"
b4,rgba,lsb,xy      .. file: Novell LANalyzer capture file
b4,rgba,msb,xy      .. file: Applesoft BASIC program data, first line number 8
b4,abgr,lsb,xy      .. file: Novell LANalyzer capture file
```
## Notas adicionales

## Referencias
