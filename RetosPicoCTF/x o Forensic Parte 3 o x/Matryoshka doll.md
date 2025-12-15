## Descripción
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/1b70cffdd2f05427fff97d13c496963f/dolls.jpg)
## Solución
```
mkdir matryoshka
FRAY30-picoctf@webshell:~$ cd matryoshka/
FRAY30-picoctf@webshell:~/matryoshka$ wget https://mercury.picoctf.net/static/1b70cffdd2f05427fff97d13c496963f/dolls.jpg
--2025-12-15 03:22:53--  https://mercury.picoctf.net/static/1b70cffdd2f05427fff97d13c496963f/dolls.jpg
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 651634 (636K) [application/octet-stream]
Saving to: 'dolls.jpg'

dolls.jpg         100%[===========>] 636.36K  1.87MB/s    in 0.3s    

2025-12-15 03:22:53 (1.87 MB/s) - 'dolls.jpg' saved [651634/651634]

FRAY30-picoctf@webshell:~/matryoshka$ ls
dolls.jpg
FRAY30-picoctf@webshell:~/matryoshka$ file dolls.jpg 
dolls.jpg: PNG image data, 594 x 1104, 8-bit/color RGBA, non-interlaced
FRAY30-picoctf@webshell:~/matryoshka$ exiftool dolls.jpg 
ExifTool Version Number         : 12.40
File Name                       : dolls.jpg
Directory                       : .
File Size                       : 636 KiB
File Modification Date/Time     : 2021:03:16 00:23:04+00:00
File Access Date/Time           : 2025:12:15 03:23:14+00:00
File Inode Change Date/Time     : 2025:12:15 03:22:53+00:00
File Permissions                : -rw-rw-r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 594
Image Height                    : 1104
Bit Depth                       : 8
Color Type                      : RGB with Alpha
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Profile Name                    : ICC Profile
Profile CMM Type                : Apple Computer Inc.
Profile Version                 : 2.1.0
Profile Class                   : Display Device Profile
Color Space Data                : RGB
Profile Connection Space        : XYZ
Profile Date Time               : 2020:06:09 12:08:45
Profile File Signature          : acsp
Primary Platform                : Apple Computer Inc.
CMM Flags                       : Not Embedded, Independent
Device Manufacturer             : Apple Computer Inc.
Device Model                    : 
Device Attributes               : Reflective, Glossy, Positive, Color
Rendering Intent                : Perceptual
Connection Space Illuminant     : 0.9642 1 0.82491
Profile Creator                 : Apple Computer Inc.
Profile ID                      : 0
Profile Description             : Display
Profile Description ML (hr-HR)  : LCD u boji
Profile Description ML (ko-KR)  : 컬러 LCD
Profile Description ML (nb-NO)  : Farge-LCD
Profile Description ML (hu-HU)  : Színes LCD
Profile Description ML (cs-CZ)  : Barevný LCD
Profile Description ML (da-DK)  : LCD-farveskærm
Profile Description ML (nl-NL)  : Kleuren-LCD
Profile Description ML (fi-FI)  : Väri-LCD
Profile Description ML (it-IT)  : LCD colori
Profile Description ML (es-ES)  : LCD color
Profile Description ML (ro-RO)  : LCD color
Profile Description ML (fr-CA)  : ACL couleur
Profile Description ML (uk-UA)  : Кольоровий LCD
Profile Description ML (he-IL)  : ‏LCD צבעוני
Profile Description ML (zh-TW)  : 彩色LCD
Profile Description ML (vi-VN)  : LCD Màu
Profile Description ML (sk-SK)  : Farebný LCD
Profile Description ML (zh-CN)  : 彩色LCD
Profile Description ML (ru-RU)  : Цветной ЖК-дисплей
Profile Description ML (en-GB)  : Colour LCD
Profile Description ML (fr-FR)  : LCD couleur
Profile Description ML (hi-IN)  : रंगीन LCD
Profile Description ML (th-TH)  : LCD สี
Profile Description ML (ca-ES)  : LCD en color
Profile Description ML (en-AU)  : Colour LCD
Profile Description ML (es-XL)  : LCD color
Profile Description ML (de-DE)  : Farb-LCD
Profile Description ML          : Color LCD
Profile Description ML (pt-BR)  : LCD Colorido
Profile Description ML (pl-PL)  : Kolor LCD
Profile Description ML (el-GR)  : Έγχρωμη οθόνη LCD
Profile Description ML (sv-SE)  : Färg-LCD
Profile Description ML (tr-TR)  : Renkli LCD
Profile Description ML (pt-PT)  : LCD a Cores
Profile Description ML (ja-JP)  : カラーLCD
Profile Copyright               : Copyright Apple Inc., 2020
Media White Point               : 0.94955 1 1.08902
Red Matrix Column               : 0.51099 0.23955 -0.00104
Green Matrix Column             : 0.29517 0.69981 0.04224
Blue Matrix Column              : 0.15805 0.06064 0.78369
Red Tone Reproduction Curve     : (Binary data 2060 bytes, use -b option to extract)
Video Card Gamma                : (Binary data 48 bytes, use -b option to extract)
Native Display Info             : (Binary data 62 bytes, use -b option to extract)
Chromatic Adaptation            : 1.04861 0.02332 -0.05034 0.03018 0.99002 -0.01714 -0.00922 0.01503 0.75172
Make And Model                  : (Binary data 40 bytes, use -b option to extract)
Blue Tone Reproduction Curve    : (Binary data 2060 bytes, use -b option to extract)
Green Tone Reproduction Curve   : (Binary data 2060 bytes, use -b option to extract)
Exif Byte Order                 : Big-endian (Motorola, MM)
X Resolution                    : 144
Y Resolution                    : 144
Resolution Unit                 : inches
User Comment                    : Screenshot
Exif Image Width                : 594
Exif Image Height               : 1104
Pixels Per Unit X               : 5669
Pixels Per Unit Y               : 5669
Pixel Units                     : meters
XMP Toolkit                     : XMP Core 5.4.0
Apple Data Offsets              : (Binary data 28 bytes, use -b option to extract)
Warning                         : [minor] Trailer data after PNG IEND chunk
Image Size                      : 594x1104
Megapixels                      : 0.656
FRAY30-picoctf@webshell:~/matryoshka$ binwalk dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378954, uncompressed size: 383938, name: base_images/2_c.jpg
651612        0x9F15C         End of Zip archive, footer length: 22

FRAY30-picoctf@webshell:~/matryoshka$ binwalk -e dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378954, uncompressed size: 383938, name: base_images/2_c.jpg
651612        0x9F15C         End of Zip archive, footer length: 22

FRAY30-picoctf@webshell:~/matryoshka$ ls -la
total 644
drwxrwxr-x  3 FRAY30-picoctf FRAY30-picoctf     63 Dec 15 03:24 .
drwxr-xr-x 36 FRAY30-picoctf FRAY30-picoctf   4096 Dec 15 03:23 ..
drwxrwxr-x  3 FRAY30-picoctf FRAY30-picoctf     54 Dec 15 03:24 _dolls.jpg.extracted
-rw-rw-r--  1 FRAY30-picoctf FRAY30-picoctf 651634 Mar 16  2021 dolls.jpg
FRAY30-picoctf@webshell:~/matryoshka$ cd _dolls.jpg.extracted/
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted$ ls -la
total 372
drwxrwxr-x 3 FRAY30-picoctf FRAY30-picoctf     54 Dec 15 03:24 .
drwxrwxr-x 3 FRAY30-picoctf FRAY30-picoctf     63 Dec 15 03:24 ..
-rw-rw-r-- 1 FRAY30-picoctf FRAY30-picoctf 379142 Dec 15 03:24 4286C.zip
drwxrwxr-x 2 FRAY30-picoctf FRAY30-picoctf     29 Dec 15 03:24 base_images
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted$ cd base_images/
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images$
 ls
2_c.jpg
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images$
 bin
bind     binwalk  
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images$
 binwalk 2_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196043, uncompressed size: 201445, name: base_images/3_c.jpg
383805        0x5DB3D         End of Zip archive, footer length: 22
383916        0x5DBAC         End of Zip archive, footer length: 22

FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images$
 binwalk -e 2_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196043, uncompressed size: 201445, name: base_images/3_c.jpg
383805        0x5DB3D         End of Zip archive, footer length: 22
383916        0x5DBAC         End of Zip archive, footer length: 22

FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images$
 ls
2_c.jpg  _2_c.jpg.extracted
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images$
 cd _2_c.jpg.extracted/
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted$ ls
2DD3B.zip  base_images
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted$ cd base_images/
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images$ ls
3_c.jpg
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images$ binwalk 3_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77651, uncompressed size: 79807, name: base_images/4_c.jpg
201423        0x312CF         End of Zip archive, footer length: 22

FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images$ binwalk -e 3_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77651, uncompressed size: 79807, name: base_images/4_c.jpg
201423        0x312CF         End of Zip archive, footer length: 22

FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images$ ls
3_c.jpg  _3_c.jpg.extracted
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images$ cd _3_c.jpg.extracted/
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images/_3_c.jpg.extracted$ ls
1E2D6.zip  base_images
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images/_3_c.jpg.extracted$ cd base_images/
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ ls
4_c.jpg
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ binwalk 4_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 63, uncompressed size: 81, name: flag.txt
79785         0x137A9         End of Zip archive, footer length: 22

FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ binwalk -e 4_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 63, uncompressed size: 81, name: flag.txt
79785         0x137A9         End of Zip archive, footer length: 22

FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ ls
4_c.jpg  _4_c.jpg.extracted
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ cd _4_c.jpg.extracted/
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ ls                    
136DA.zip  flag.txt
FRAY30-picoctf@webshell:~/matryoshka/_dolls.jpg.extracted/base_images/
_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ cat flag.txt
picoCTF{bf6acf878dcbd752f4721e41b1b1b66b}
```
## Notas adicionales

## Referencias
