## Descripción
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/176/challenge.zip)
## Solución
```
mkdir colve
FRAY30-picoctf@webshell:~$ cd colve
FRAY30-picoctf@webshell:~/colve$ wget https://artifacts.picoctf.net/c_titan/176/challenge.zip
--2025-11-03 12:38:11--  https://artifacts.picoctf.net/c_titan/176/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.33, 3.170.131.72, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 24474 (24K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip     100%[===========>]  23.90K  --.-KB/s    in 0.008s  

2025-11-03 12:38:11 (2.95 MB/s) - 'challenge.zip' saved [24474/24474]

FRAY30-picoctf@webshell:~/colve$ ls
challenge.zip
FRAY30-picoctf@webshell:~/colve$ unzip challenge.zip 
Archive:  challenge.zip
   creating: drop-in/
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/main  
   creating: drop-in/.git/refs/heads/feature/
 extracting: drop-in/.git/refs/heads/feature/part-1  
 extracting: drop-in/.git/refs/heads/feature/part-2  
 extracting: drop-in/.git/refs/heads/feature/part-3  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/77/
 extracting: drop-in/.git/objects/77/d6ceca6fe23b57d88cf16f20003e10d6715690  
   creating: drop-in/.git/objects/b9/
 extracting: drop-in/.git/objects/b9/32e8c048154a46d224cd7691c99dc8cb88164a  
   creating: drop-in/.git/objects/eb/
 extracting: drop-in/.git/objects/eb/19d0e3c28278752f0735c4451b885136a24105  
   creating: drop-in/.git/objects/6e/
 extracting: drop-in/.git/objects/6e/17fb3a35364b4f9bb8bef8b5e6a5af2d3e7dfa  
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/e44dd37ba0c0adc3d78d0b85d699859ec8d75c  
   creating: drop-in/.git/objects/0c/
 extracting: drop-in/.git/objects/0c/d57e0aedc31a1a92e0b79235c818de437cde8e  
   creating: drop-in/.git/objects/7a/
 extracting: drop-in/.git/objects/7a/b4e25c0cd108374b2275fdb1fcdf635e591833  
 extracting: drop-in/.git/objects/7a/7534d2ed05e1637c5ea21d0981646444c2c9f9  
   creating: drop-in/.git/objects/d1/
 extracting: drop-in/.git/objects/d1/f3407cee4479c075997b497fa290ca636fe258  
   creating: drop-in/.git/objects/70/
 extracting: drop-in/.git/objects/70/64732e2fd39d2247bd6ba2ccc4cf9576974d38  
   creating: drop-in/.git/objects/46/
 extracting: drop-in/.git/objects/46/72a5cadb0c545e90d476f0783c9d0874512b0e  
   creating: drop-in/.git/objects/83/
 extracting: drop-in/.git/objects/83/95824cc0ce486d1be9ab874bfedb2cec2ea398  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/main  
   creating: drop-in/.git/logs/refs/heads/feature/
  inflating: drop-in/.git/logs/refs/heads/feature/part-1  
  inflating: drop-in/.git/logs/refs/heads/feature/part-2  
  inflating: drop-in/.git/logs/refs/heads/feature/part-3  
  inflating: drop-in/flag.py         
FRAY30-picoctf@webshell:~/colve$ cd drop-in/
FRAY30-picoctf@webshell:~/colve/drop-in$ python flag.py 
Printing the flag...
FRAY30-picoctf@webshell:~/colve/drop-in$ git branch -a
FRAY30-picoctf@webshell:~/colve/drop-in$ git log 'feature/part-1'
FRAY30-picoctf@webshell:~/colve/drop-in$ git show 0cd57e0aedc31a1a92e0b79235c818de437cde8e
FRAY30-picoctf@webshell:~/colve/drop-in$ git log 'feature/part-2'
FRAY30-picoctf@webshell:~/colve/drop-in$ git show 7064732e2fd39d2247bd6ba2ccc4cf9576974d38
FRAY30-picoctf@webshell:~/colve/drop-in$ git log 'feature/part-3'
FRAY30-picoctf@webshell:~/colve/drop-in$ git show 8395824cc0ce486d1be9ab874bfedb2cec2ea398
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_2c91ca76}
```
## Notas adicionales

## Referencias
