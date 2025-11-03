## Descripción
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin.

Additional details will be available after launching your challenge instance.
## Solución
```
ssh ctf-player@wily-courier.picoctf.net -p 51102
The authenticity of host '[wily-courier.picoctf.net]:51102 ([18.189.99.27]:51102)' can't be established.
ED25519 key fingerprint is SHA256:ErlUUvYlrAxfSW1tIdzfOnGTBSr5OFkZvz0nMN4Vodw.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[wily-courier.picoctf.net]:51102' (ED25519) to the list of known hosts.
ctf-player@wily-courier.picoctf.net's password: 
Permission denied, please try again.
ctf-player@wily-courier.picoctf.net's password: 
Welcome to Ubuntu 18.04.6 LTS (GNU/Linux 6.14.0-1012-aws x86_64)

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
ctf-player@pico-chall$ ls -la
total 8
drwxr-xr-x 1 ctf-player ctf-player 59 Sep 12 16:20 .
drwxr-xr-x 1 ctf-player ctf-player 20 Nov  3 00:11 ..
-rw-r--r-- 1 ctf-player ctf-player 14 Aug 14 18:35 1of3.flag.txt
-rw-r--r-- 1 ctf-player ctf-player 56 Aug 14 18:35 instructions-to-2of3.txt
ctf-player@pico-chall$ cat 1of3.flag.txt 
picoCTF{xxsh_
ctf-player@pico-chall$ cd instructions-to-2of3.txt 
-bash: cd: instructions-to-2of3.txt: Not a directory
ctf-player@pico-chall$ cat instructions-to-2of3.txt 
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ pwd
/
ctf-player@pico-chall$ ls -la
total 12
drwxr-xr-x   1 root   root      40 Nov  3 00:04 .
drwxr-xr-x   1 root   root      40 Nov  3 00:04 ..
-rwxr-xr-x   1 root   root       0 Nov  3 00:04 .dockerenv
-rw-r--r--   1 root   root      15 Aug 14 18:35 2of3.flag.txt
drwxr-xr-x   1 root   root    4096 Sep 12 16:19 bin
drwxr-xr-x   2 root   root       6 Apr 24  2018 boot
drwxr-xr-x   2 root   root      27 Sep 12 16:20 challenge
drwxr-xr-x   5 root   root     340 Nov  3 00:04 dev
drwxr-xr-x   1 root   root      66 Nov  3 00:04 etc
drwxr-xr-x   1 root   root      24 Sep 12 16:20 home
-rw-r--r--   1 root   root      51 Aug 14 18:35 instructions-to-3of3.txt
drwxr-xr-x   1 root   root      86 Sep 12 16:19 lib
drwxr-xr-x   2 root   root      34 May 30  2023 lib64
drwxr-xr-x   2 root   root       6 May 30  2023 media
drwxr-xr-x   2 root   root       6 May 30  2023 mnt
drwxr-xr-x   1 root   root      22 Sep 12 16:20 opt
dr-xr-xr-x 208 nobody nogroup    0 Nov  3 00:04 proc
drwx------   2 root   root      37 May 30  2023 root
drwxr-xr-x   1 root   root      66 Nov  3 00:11 run
drwxr-xr-x   1 root   root     158 Sep 12 16:19 sbin
drwxr-xr-x   2 root   root       6 May 30  2023 srv
dr-xr-xr-x  13 nobody nogroup    0 Nov  3 00:04 sys
drwxrwxrwt   1 root   root       6 Sep 12 16:20 tmp
drwxr-xr-x   1 root   root      66 May 30  2023 usr
drwxr-xr-x   1 root   root      17 May 30  2023 var
ctf-player@pico-chall$ cat 2of3.flag.txt 
0ut_0f_//4t3r_
ctf-player@pico-chall$ cat instructions-to-2of3.txt 
cat: instructions-to-2of3.txt: No such file or directory
ctf-player@pico-chall$ cat instructions-to-3of3.txt 
Lastly, ctf-player, go home... more succinctly `~`
ctf-player@pico-chall$ cd
ctf-player@pico-chall$ pwd
/home/ctf-player
ctf-player@pico-chall$ cd ~
ctf-player@pico-chall$ ls -la
total 8
drwxr-xr-x 1 ctf-player ctf-player 20 Nov  3 00:11 .
drwxr-xr-x 1 root       root       24 Sep 12 16:20 ..
drwx------ 2 ctf-player ctf-player 34 Nov  3 00:11 .cache
-rw-r--r-- 1 ctf-player ctf-player 80 Aug 14 18:35 .profile
drw------- 1 ctf-player ctf-player 61 Sep 12 16:20 .ssh
-rw-r--r-- 1 root       root        9 Sep 12 16:20 3of3.flag.txt
drwxr-xr-x 1 ctf-player ctf-player 59 Sep 12 16:20 drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt 
0b24fc4f}
picoCTF{xxsh_0ut_0f_//4t3r_0b24fc4f}
```
## Notas adicionales

## Referencias