## Descripción
Find the flag in the Python script![Download Python script](https://artifacts.picoctf.net/c/35/serpentine.py)
## Solución
```
mkdir serpentine
FRAY30-picoctf@webshell:~$ cd serpentine/
FRAY30-picoctf@webshell:~/serpentine$ pwd
/home/FRAY30-picoctf/serpentine
FRAY30-picoctf@webshell:~/serpentine$ wget https://artifacts.picoctf.net/c/35/serpentine.py
--2025-11-03 03:52:16--  https://artifacts.picoctf.net/c/35/serpentine.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.18, 3.170.131.72, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2550 (2.5K) [application/octet-stream]
Saving to: 'serpentine.py'

serpentine.py     100%[===========>]   2.49K  --.-KB/s    in 0s      

2025-11-03 03:52:16 (113 MB/s) - 'serpentine.py' saved [2550/2550]

FRAY30-picoctf@webshell:~/serpentine$ ls
serpentine.py
FRAY30-picoctf@webshell:~/serpentine$ python serpentine.py 

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) a

-----------------------------------------------------
You can do it!
-----------------------------------------------------


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b

Oops! I must have misplaced the print_flag function! Check my source code!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) c
FRAY30-picoctf@webshell:~/serpentine$  nano serpentine.py

(En el codigo se modifica:
elif choice == 'b':
      print(print_flag())
)

FRAY30-picoctf@webshell:~/serpentine$ python serpentine.py 

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}
```
## Notas adicionales

## Referencias