## Descripción
Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/501/files.zip)
## Solución
```
FRAY30-picoctf@webshell:~$ mkdir firstfind
FRAY30-picoctf@webshell:~$ cd firstfind/
FRAY30-picoctf@webshell:~/firstfind$ pwd
/home/FRAY30-picoctf/firstfind
FRAY30-picoctf@webshell:~/firstfind$ wget https://artifacts.picoctf.net/c/501/files.zip
--2025-11-02 23:10:42--  https://artifacts.picoctf.net/c/501/files.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.72, 3.170.131.33, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 3995553 (3.8M) [application/octet-stream]
Saving to: 'files.zip'

files.zip                           100%[===================================================================>]   3.81M  1.83MB/s    in 2.1s    

2025-11-02 23:10:44 (1.83 MB/s) - 'files.zip' saved [3995553/3995553]

FRAY30-picoctf@webshell:~/firstfind$ ls -la
total 3908
drwxrwxr-x 2 FRAY30-picoctf FRAY30-picoctf      31 Nov  2 23:10 .
drwxr-xr-x 6 FRAY30-picoctf FRAY30-picoctf    4096 Nov  2 23:08 ..
-rw-rw-r-- 1 FRAY30-picoctf FRAY30-picoctf 3995553 Aug  4  2023 files.zip
FRAY30-picoctf@webshell:~/firstfind$ unzip files.zip 
Archive:  files.zip
   creating: files/
   creating: files/satisfactory_books/
   creating: files/satisfactory_books/more_books/
  inflating: files/satisfactory_books/more_books/37121.txt.utf-8  
  inflating: files/satisfactory_books/23765.txt.utf-8  
  inflating: files/satisfactory_books/16021.txt.utf-8  
  inflating: files/13771.txt.utf-8   
   creating: files/adequate_books/
   creating: files/adequate_books/more_books/
   creating: files/adequate_books/more_books/.secret/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/
   creating: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/
 extracting: files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt  
  inflating: files/adequate_books/more_books/1023.txt.utf-8  
  inflating: files/adequate_books/46804-0.txt  
  inflating: files/adequate_books/44578.txt.utf-8  
   creating: files/acceptable_books/
   creating: files/acceptable_books/more_books/
  inflating: files/acceptable_books/more_books/40723.txt.utf-8  
  inflating: files/acceptable_books/17880.txt.utf-8  
  inflating: files/acceptable_books/17879.txt.utf-8  
  inflating: files/14789.txt.utf-8   
FRAY30-picoctf@webshell:~/firstfind$ ls
files  files.zip
FRAY30-picoctf@webshell:~/firstfind$ ls -la
total 3908
drwxrwxr-x 3 FRAY30-picoctf FRAY30-picoctf      48 Nov  2 23:11 .
drwxr-xr-x 6 FRAY30-picoctf FRAY30-picoctf    4096 Nov  2 23:08 ..
drwxrwxr-x 5 FRAY30-picoctf FRAY30-picoctf     148 May 13  2022 files
-rw-rw-r-- 1 FRAY30-picoctf FRAY30-picoctf 3995553 Aug  4  2023 files.zip
FRAY30-picoctf@webshell:~/firstfind$ ls -la files
total 1924
drwxrwxr-x 5 FRAY30-picoctf FRAY30-picoctf     148 May 13  2022 .
drwxrwxr-x 3 FRAY30-picoctf FRAY30-picoctf      48 Nov  2 23:11 ..
-rw-rw-r-- 1 FRAY30-picoctf FRAY30-picoctf 1003806 May  7  2022 13771.txt.utf-8
-rw-rw-r-- 1 FRAY30-picoctf FRAY30-picoctf  960595 May  7  2022 14789.txt.utf-8
drwxrwxr-x 3 FRAY30-picoctf FRAY30-picoctf      86 May 13  2022 acceptable_books
drwxrwxr-x 3 FRAY30-picoctf FRAY30-picoctf      82 May 13  2022 adequate_books
drwxrwxr-x 3 FRAY30-picoctf FRAY30-picoctf      86 May 13  2022 satisfactory_books
FRAY30-picoctf@webshell:~/firstfind$ find . -name uber-secret.txt
./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
FRAY30-picoctf@webshell:~/firstfind$ cat ./files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
picoCTF{f1nd_15_f457_ab443fd1}
```
## Notas adicionales

## Referencias