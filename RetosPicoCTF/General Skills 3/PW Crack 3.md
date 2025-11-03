## Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución
```
mkdir pwc3
FRAY30-picoctf@webshell:~$ cd pwc3/
FRAY30-picoctf@webshell:~/pwc3$ pwd
/home/FRAY30-picoctf/pwc3
FRAY30-picoctf@webshell:~/pwc3$ wget https://artifacts.picoctf.net/c/18/level3.py
--2025-11-03 04:34:17--  https://artifacts.picoctf.net/c/18/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.72, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py         100%[===========>]   1.31K  --.-KB/s    in 0s      

2025-11-03 04:34:17 (971 MB/s) - 'level3.py' saved [1337/1337]

FRAY30-picoctf@webshell:~/pwc3$ wget https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
--2025-11-03 04:34:32--  https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.72, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.e 100%[===========>]      31  --.-KB/s    in 0s      

2025-11-03 04:34:32 (13.3 MB/s) - 'level3.flag.txt.enc' saved [31/31]

FRAY30-picoctf@webshell:~/pwc3$ wget https://artifacts.picoctf.net/c/18/level3.hash.bin
--2025-11-03 04:34:46--  https://artifacts.picoctf.net/c/18/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.77, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin   100%[===========>]      16  --.-KB/s    in 0s      

2025-11-03 04:34:46 (5.80 MB/s) - 'level3.hash.bin' saved [16/16]

FRAY30-picoctf@webshell:~/pwc3$ ls
level3.flag.txt.enc  level3.hash.bin  level3.py
FRAY30-picoctf@webshell:~/pwc3$ nano level3.py

(Se modifica:
def level_3_pw_check():
    for pw in pos_pw_list:
        user_pw_hash = hash_pw(pw)

        if( user_pw_hash == correct_pw_hash ):
            print("Welcome back... your flag, user:")
            decryption = str_xor(flag_enc.decode(), pw)
            print(decryption)
            return
    print("That password is incorrect")

# The strings below are 7 possibilities for the correct password. 
#   (Only 1 is correct)
pos_pw_list = ["8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"]

level_3_pw_check()
)

FRAY30-picoctf@webshell:~/pwc3$ python level3.py
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
```
## Notas adicionales

## Referencias