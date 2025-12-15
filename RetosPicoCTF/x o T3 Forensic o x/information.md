## Descripción
Files can always be changed in a secret way. Can you find the flag?[cat.jpg](https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg)
## Solución
```
wget https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg
--2025-12-15 11:51:26--  https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.18, 3.160.5.64, 3.160.5.95, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 878136 (858K) [application/octet-stream]
Saving to: 'cat.jpg'

cat.jpg           100%[===========>] 857.55K  1.83MB/s    in 0.5s    

2025-12-15 11:51:27 (1.83 MB/s) - 'cat.jpg' saved [878136/878136]

FRAY30-picoctf@webshell:/tmp/...infot$ ls
cat.jpg
FRAY30-picoctf@webshell:/tmp/...infot$ file cat.jpg 
cat.jpg: JPEG image data, JFIF standard 1.02, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 2560x1598, components 3
FRAY30-picoctf@webshell:/tmp/...infot$ exiftool cat.jpg 
ExifTool Version Number         : 12.40
File Name                       : cat.jpg
Directory                       : .
File Size                       : 858 KiB
File Modification Date/Time     : 2025:12:12 19:21:14+00:00
File Access Date/Time           : 2025:12:15 11:51:49+00:00
File Inode Change Date/Time     : 2025:12:15 11:51:27+00:00
File Permissions                : -rw-rw-r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
FRAY30-picoctf@webshell:/tmp/...infot$ echo 'cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9k' | base64 -d
picoCTF{the_m3tadata_1s_modified}
```

## Notas adicionales

## Referencias
