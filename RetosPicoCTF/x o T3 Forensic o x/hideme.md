## Descripción
Every file gets a flag.The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/262/flag.png).
## Solución
```
wget https://artifacts.picoctf.net/c/262/flag.png
--2025-12-15 11:38:51--  https://artifacts.picoctf.net/c/262/flag.png
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.18, 3.170.131.33, 3.170.131.72, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 42945 (42K) [application/octet-stream]
Saving to: 'flag.png'

flag.png          100%[===========>]  41.94K  --.-KB/s    in 0.01s   

2025-12-15 11:38:51 (2.77 MB/s) - 'flag.png' saved [42945/42945]

FRAY30-picoctf@webshell:/tmp/...hideme$ ls
flag.png
FRAY30-picoctf@webshell:/tmp/...hideme$ file flag.png 
flag.png: PNG image data, 512 x 504, 8-bit/color RGBA, non-interlaced
FRAY30-picoctf@webshell:/tmp/...hideme$ exiftool flag.png 
ExifTool Version Number         : 12.40
File Name                       : flag.png
Directory                       : .
File Size                       : 42 KiB
File Modification Date/Time     : 2023:03:16 03:16:06+00:00
File Access Date/Time           : 2025:12:15 11:39:54+00:00
File Inode Change Date/Time     : 2025:12:15 11:38:51+00:00
File Permissions                : -rw-rw-r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 512
Image Height                    : 504
Bit Depth                       : 8
Color Type                      : RGB with Alpha
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Warning                         : [minor] Trailer data after PNG IEND chunk
Image Size                      : 512x504
Megapixels                      : 0.258
FRAY30-picoctf@webshell:/tmp/...hideme$ binwalk flag.png 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2884, uncompressed size: 3038, name: secret/flag.png
42923         0xA7AB          End of Zip archive, footer length: 22

FRAY30-picoctf@webshell:/tmp/...hideme$ binwalk -e flag.png 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2884, uncompressed size: 3038, name: secret/flag.png
42923         0xA7AB          End of Zip archive, footer length: 22

FRAY30-picoctf@webshell:/tmp/...hideme$ ls
_flag.png.extracted  flag.png
FRAY30-picoctf@webshell:/tmp/...hideme$ cd _flag.png.extracted/
FRAY30-picoctf@webshell:/tmp/...hideme/_flag.png.extracted$ ls
29  29.zlib  9B3B.zip  secret
FRAY30-picoctf@webshell:/tmp/...hideme/_flag.png.extracted$ cd secret/
FRAY30-picoctf@webshell:/tmp/...hideme/_flag.png.extracted/secret$ ls
flag.png
FRAY30-picoctf@webshell:/tmp/...hideme/_flag.png.extracted/secret$ sz flag.png
```
picoCTF{Hiddinng_An_imag3_within_@n_ima9e_82101824}
## Notas adicionales

## Referencias
