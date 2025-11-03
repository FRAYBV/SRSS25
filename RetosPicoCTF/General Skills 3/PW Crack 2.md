## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.
## Solución
```
mkdir pwc2
FRAY30-picoctf@webshell:~$ cd pwc2/
FRAY30-picoctf@webshell:~/pwc2$ pwd
/home/FRAY30-picoctf/pwc2
FRAY30-picoctf@webshell:~/pwc2$ wget https://artifacts.picoctf.net/c/15/level2.py
--2025-11-03 04:20:46--  https://artifacts.picoctf.net/c/15/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.33, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py         100%[===========>]     914  --.-KB/s    in 0s      

2025-11-03 04:20:46 (263 MB/s) - 'level2.py' saved [914/914]

FRAY30-picoctf@webshell:~/pwc2$ wget https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
--2025-11-03 04:21:38--  https://artifacts.picoctf.net/c/15/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.72, 3.170.131.77, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.e 100%[===========>]      31  --.-KB/s    in 0s      

2025-11-03 04:21:38 (29.1 MB/s) - 'level2.flag.txt.enc' saved [31/31]

FRAY30-picoctf@webshell:~/pwc2$ ls
level2.flag.txt.enc  level2.py
FRAY30-picoctf@webshell:~/pwc2$ python level2.py 
Please enter correct password for flag: zi
That password is incorrect
FRAY30-picoctf@webshell:~/pwc2$ cat level2.py
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level2.flag.txt.enc', 'rb').read()



def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_2_pw_check()
FRAY30-picoctf@webshell:~/pwc2$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65))
39ce
>>> exit()
FRAY30-picoctf@webshell:~/pwc2$ python level2.py 
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
```
## Notas adicionales

## Referencias