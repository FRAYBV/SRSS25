## Descripción
How about some hide and seek?Download this file [here](https://artifacts.picoctf.net/c_titan/6/unknown.zip).
## Solución
```
wget https://artifacts.picoctf.net/c_titan/6/unknown.zip
--2025-12-15 12:26:43--  https://artifacts.picoctf.net/c_titan/6/unknown.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.18, 3.170.131.72, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2252298 (2.1M) [application/octet-stream]
Saving to: 'unknown.zip'

unknown.zip       100%[===========>]   2.15M  1.82MB/s    in 1.2s    

2025-12-15 12:26:44 (1.82 MB/s) - 'unknown.zip' saved [2252298/2252298]

FRAY30-picoctf@webshell:/tmp/...cysee$ ls
unknown.zip
FRAY30-picoctf@webshell:/tmp/...cysee$ unzip unknown.zip 
Archive:  unknown.zip
  inflating: ukn_reality.jpg         
FRAY30-picoctf@webshell:/tmp/...cysee$ ls -la
total 4412
drwxrwxr-x 2 FRAY30-picoctf FRAY30-picoctf      60 Dec 15 12:27 .
drwxrwxrwt 1 root           root                30 Dec 15 12:26 ..
-rw-r--r-- 1 FRAY30-picoctf FRAY30-picoctf 2263768 Feb 15  2024 ukn_reality.jpg
-rw-rw-r-- 1 FRAY30-picoctf FRAY30-picoctf 2252298 Feb 15  2024 unknown.zip
FRAY30-picoctf@webshell:/tmp/...cysee$ strings -10 ukn_reality.jpg 
7http://ns.adobe.com/xap/1.0/
<?xpacket begin='
' id='W5M0MpCehiHzreSzNTczkc9d'?>
<x:xmpmeta xmlns:x='adobe:ns:meta/' x:xmptk='Image::ExifTool 11.88'>
<rdf:RDF xmlns:rdf='http://www.w3.org/1999/02/22-rdf-syntax-ns#'>
 <rdf:Description rdf:about=''
  xmlns:cc='http://creativecommons.org/ns#'>
  <cc:attributionURL rdf:resource='cGljb0NURntNRTc0RDQ3QV9ISUREM05fYTZkZjhkYjh9Cg=='/>
 </rdf:Description>
</rdf:RDF>
</x:xmpmeta>
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
                                                                                                    
<?xpacket end='w'?>
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
]qQH>cRB~cL
&tn85NE+DG
"<SqD})KU%
|TInTv$R1M-M
1INjmxRGhQE
0=EqW.KWN.
>6U!YOI?4\6%-V"n
2bCW0erycVco
iFII_Tg^3t
=-Q`V~K3c*}
chqjJVCF1KV
M(QK&Eo[xb
wio}o{x5$fH
<Sb8cN5,'M5
-l_|>k4Fy7n
e>qpNKg5G?
s]ti7IKMnr
0+9av<)5q-
M4SoPHvM%-6
4Tjr3. jnv
*KgPNzUWpV
 S6r*t^EmN6fs
]:6s]<s UH
]%eqfqR_-OA
5v$RzSOJBsO
c.piUF9=h$(j
]=,Mk3!l6*
p_]$2\?DV5
Y]jyx&uL[8
O;8!    $/@OJ
$dpzQunD}:q_
[q6Nvy\5~fk
 FrN\"w _S
+n5_& r]KH
%P89 WM ic
#z_D\)%9TQ
w}SI/Tjx+J
}u92xBJjo^
.ZEeR9(Ez7
_MY[dyx:If8
X4WrS*#v|.
ZT'UF/kEv$
g|/e}C{]8S p
0+LtcZuT%uy;
{ewqi{  2Cy
R"{W&.P5v^ 
jkcz;3R8AL
j:Pkjz4&lF
<V]Y{nNEm7^
Y\YKk3y~fK0"
u1.ThYs)5fy
#e~DxCW[mZ
Gq1'9*s__|1
UiMs9Z6GLay\
?A^SpN95~Y
/t]A4[mBh$
D0z)88`q]U
lLX/,eU=sV<h
b).oD6KpeU
 8n95vU-N@
D3LgO.[0P<o$m
='u>I]s]jv,ElFcZ
U Lw(FCdWu
Zu)IINwiti
1U%`QMe)Y4
,u7[e   M&yX
y'sOi[PI'-
)5Fd*#fR7/
sUFnNWKrq1QT
OSW5[kx.'[yL
@b;[q'=MszS
v*3M+E+itA
J1sURqkfqb
3^g,!dq^6>
{4j_1SOI7c
}Mkr[T{U3i
Ya0j    JRvWv
Uya%m.k1&(
O:XjX*XJSr
_GsB=NPb@@\
9'9,s^?z?y!
9aoleB3*}k
\YiVmqp!yB.3
%^G~K>l-/$z
T'<Vumcj/Q
aRwjM%mw<'9
) utt%YYNCdw
!S)*x5@C_=^
W!MEiq,S+E##
.z-'d:D"6'
YR*)[ T^e($
hneI7'}5ED
l%,U9*u/;]-
_ UiG=jxqXE
RCUSnCsXI;#
==li-#rx'm
G$+7$W=*.X
^gyE+tV2bQ
=Ta_7ST}-"*a4
s+3&ppGsXL95
k{,Dj5~W{3L
j3KIE2:)E+W
FRAY30-picoctf@webshell:/tmp/...cysee$ ls                   
ukn_reality.jpg  unknown.zip
FRAY30-picoctf@webshell:/tmp/...cysee$ exiftool ukn_reality.jpg 
ExifTool Version Number         : 12.40
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.2 MiB
File Modification Date/Time     : 2024:02:15 22:40:21+00:00
File Access Date/Time           : 2025:12:15 12:28:35+00:00
File Inode Change Date/Time     : 2025:12:15 12:27:39+00:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fYTZkZjhkYjh9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
FRAY30-picoctf@webshell:/tmp/...cysee$ echo -n 'cGljb0NURntNRTc0RDQ3QV9ISUREM05fYTZkZjhkYjh9Cg==' | base64 -d
picoCTF{ME74D47A_HIDD3N_a6df8db8}
```
## Notas adicionales

## Referencias
