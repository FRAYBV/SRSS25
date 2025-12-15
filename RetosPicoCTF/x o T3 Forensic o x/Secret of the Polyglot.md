## Descripción
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/9/flag2of2-final.pdf).
## Solución
```
wget https://artifacts.picoctf.net/c_titan/9/flag2of2-final.pdf
--2025-12-15 11:55:37--  https://artifacts.picoctf.net/c_titan/9/flag2of2-final.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.18, 3.170.131.77, 3.170.131.72, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3362 (3.3K) [application/octet-stream]
Saving to: 'flag2of2-final.pdf'

flag2of2-final.pd 100%[===========>]   3.28K  --.-KB/s    in 0s      

2025-12-15 11:55:37 (1.04 GB/s) - 'flag2of2-final.pdf' saved [3362/3362]

FRAY30-picoctf@webshell:/tmp/...sepoly$ ls
flag2of2-final.pdf
FRAY30-picoctf@webshell:/tmp/...sepoly$ ls -la
total 4
drwxrwxr-x 2 FRAY30-picoctf FRAY30-picoctf   32 Dec 15 11:55 .
drwxrwxrwt 1 root           root             31 Dec 15 11:55 ..
-rw-rw-r-- 1 FRAY30-picoctf FRAY30-picoctf 3362 Feb  7  2024 flag2of2-final.pdf
FRAY30-picoctf@webshell:/tmp/...sepoly$ xdg-open flag2of2-final.pdf 
Error: no "view" mailcap rules found for type "application/pdf"
FRAY30-picoctf@webshell:/tmp/...sepoly$ xdg-open flag2of2-final.pdf 
Error: no "view" mailcap rules found for type "application/pdf"

Can't Access `file://localhost/tmp/...sepoly/flag2of2-final.pdf'
Alert!: Unable to access document.

lynx: Can't access startfile 
/usr/bin/xdg-open: 882: links2: not found
/usr/bin/xdg-open: 882: elinks: not found
/usr/bin/xdg-open: 882: links: not found

Can't Access `file://localhost/tmp/...sepoly/flag2of2-final.pdf'
Alert!: Unable to access document.

lynx: Can't access startfile 
/usr/bin/xdg-open: 882: w3m: not found
xdg-open: no method available for opening 'flag2of2-final.pdf'
FRAY30-picoctf@webshell:/tmp/...sepoly$ xdg-open flag2of2-final1.pdf 
Error: no "view" mailcap rules found for type "application/pdf"

Can't Access `file://localhost/tmp/...sepoly/flag2of2-final1.pdf'
Alert!: Unable to access document.

lynx: Can't access startfile 
/usr/bin/xdg-open: 882: links2: not found
/usr/bin/xdg-open: 882: elinks: not found
/usr/bin/xdg-open: 882: links: not found

Can't Access `file://localhost/tmp/...sepoly/flag2of2-final1.pdf'
Alert!: Unable to access document.

lynx: Can't access startfile 
/usr/bin/xdg-open: 882: w3m: not found
xdg-open: no method available for opening 'flag2of2-final1.pdf'
FRAY30-picoctf@webshell:/tmp/...sepoly$ sz flag2of2-final1.pdf 
FRAY30-picoctf@webshell:/tmp/...sepoly$  KB
FRAY30-picoctf@webshell:/tmp/...sepoly$ exiftool flag2of2-final      
flag2of2-final.pdf   flag2of2-final1.pdf  
FRAY30-picoctf@webshell:/tmp/...sepoly$ exiftool flag2of2-final.pdf
ExifTool Version Number         : 12.40
File Name                       : flag2of2-final.pdf
Directory                       : .
File Size                       : 3.3 KiB
File Modification Date/Time     : 2024:02:07 17:50:38+00:00
File Access Date/Time           : 2025:12:15 11:57:18+00:00
File Inode Change Date/Time     : 2025:12:15 11:55:37+00:00
File Permissions                : -rw-rw-r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 50
Image Height                    : 50
Bit Depth                       : 8
Color Type                      : RGB with Alpha
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Profile Name                    : ICC profile
Profile CMM Type                : Little CMS
Profile Version                 : 4.3.0
Profile Class                   : Display Device Profile
Color Space Data                : RGB
Profile Connection Space        : XYZ
Profile Date Time               : 2023:11:02 17:42:31
Profile File Signature          : acsp
Primary Platform                : Apple Computer Inc.
CMM Flags                       : Not Embedded, Independent
Device Manufacturer             : 
Device Model                    : 
Device Attributes               : Reflective, Glossy, Positive, Color
Rendering Intent                : Perceptual
Connection Space Illuminant     : 0.9642 1 0.82491
Profile Creator                 : Little CMS
Profile ID                      : 0
Profile Description             : GIMP built-in sRGB
Profile Copyright               : Public Domain
Media White Point               : 0.9642 1 0.82491
Chromatic Adaptation            : 1.04788 0.02292 -0.05022 0.02959 0.99048 -0.01707 -0.00925 0.01508 0.75168
Red Matrix Column               : 0.43604 0.22249 0.01392
Blue Matrix Column              : 0.14305 0.06061 0.71393
Green Matrix Column             : 0.38512 0.7169 0.09706
Red Tone Reproduction Curve     : (Binary data 32 bytes, use -b option to extract)
Green Tone Reproduction Curve   : (Binary data 32 bytes, use -b option to extract)
Blue Tone Reproduction Curve    : (Binary data 32 bytes, use -b option to extract)
Chromaticity Channels           : 3
Chromaticity Colorant           : Unknown (0)
Chromaticity Channel 1          : 0.64 0.33002
Chromaticity Channel 2          : 0.3 0.60001
Chromaticity Channel 3          : 0.15001 0.06
Device Mfg Desc                 : GIMP
Device Model Desc               : sRGB
Pixels Per Unit X               : 11811
Pixels Per Unit Y               : 11811
Pixel Units                     : meters
Modify Date                     : 2023:11:02 17:57:06
Comment                         : Created with GIMP
Warning                         : [minor] Trailer data after PNG IEND chunk
Image Size                      : 50x50
Megapixels                      : 0.003
FRAY30-picoctf@webshell:/tmp/...sepoly$ ls
flag2of2-final.pdf  flag2of2-final1.pdf
FRAY30-picoctf@webshell:/tmp/...sepoly$ foremost flag2of2-final.pdf
Processing: flag2of2-final.pdf
|*|
FRAY30-picoctf@webshell:/tmp/...sepoly$ ls -la
total 8
drwxrwxr-x 3 FRAY30-picoctf FRAY30-picoctf   73 Dec 15 12:02 .
drwxrwxrwt 1 root           root             31 Dec 15 11:57 ..
-rw-rw-r-- 1 FRAY30-picoctf FRAY30-picoctf 3362 Feb  7  2024 flag2of2-final.pdf
-rw-rw-r-- 1 FRAY30-picoctf FRAY30-picoctf 3362 Dec 15 11:57 flag2of2-final1.pdf
drwxrwxr-- 3 FRAY30-picoctf FRAY30-picoctf   34 Dec 15 12:02 output
FRAY30-picoctf@webshell:/tmp/...sepoly$ cd output
FRAY30-picoctf@webshell:/tmp/...sepoly/output$ ls
audit.txt  png
FRAY30-picoctf@webshell:/tmp/...sepoly/output$ cd png
FRAY30-picoctf@webshell:/tmp/...sepoly/output/png$ ls
00000000.png
FRAY30-picoctf@webshell:/tmp/...sepoly/output/png$ xdg-open flag2of2-final.pdf
xdg-open: file 'flag2of2-final.pdf' does not exist
FRAY30-picoctf@webshell:/tmp/...sepoly/output/png$ xdg-open 00000000.png 
Error: no "view" rule for type "image/png" passed its test case
       (for more information, add "--debug=1" on the command line)
FRAY30-picoctf@webshell:/tmp/...sepoly/output/png$ sz 00000000.png
```
picoCTF{f1u3n7_1n_pn9_&_pdf_7f9bccd1}
## Notas adicionales

## Referencias
