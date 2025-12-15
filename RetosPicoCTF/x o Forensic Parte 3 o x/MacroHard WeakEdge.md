## Descripción
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/52da699e0f203321c7c90ab56ea912d8/Forensics%20is%20fun.pptm)
## Solución
```
wget https://mercury.picoctf.net/static/52da699e0f203321c7c90ab56ea912d8/Forensics%20is%20fun.pptm
ls
olevba Forensics\ is\ fun.pptm
mv Forensics\ is\ fun.pptm  Forensics\ is\ fun.zip
ls
unzip Forensics\ is\ fun.zi
ls -alR Forensics\ is\ fun.zip | more
cd ppt
ls
cd slideMasters
ls
vi hidden
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q
```
Base64 decoder:
picoCTF{D1d_u_kn0w_ppts_r_z1p5}
## Notas adicionales

## Referencias
