## Nombre del reto:
patchme.py

## Objetivo:
Can you get the flag?Run this [Python program](https://artifacts.picoctf.net/c/388/patchme.flag.py) in the same directory as this [encrypted flag](https://artifacts.picoctf.net/c/388/flag.txt.enc).

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir patch  
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd patch  
                                                                             
``┌──(kali㉿kali)-[~/patch]
└─$ wget https://artifacts.picoctf.net/c/388/patchme.flag.py
--2022-11-25 13:13:03--  https://artifacts.picoctf.net/c/388/patchme.flag.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.56, 13.249.74.17, 13.249.74.22, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.56|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 980 [application/octet-stream]
Saving to: ‘patchme.flag.py’

patchme.flag.py     100%[================>]     980  --.-KB/s    in 0s      

2022-11-25 13:13:04 (12.2 MB/s) - ‘patchme.flag.py’ saved [980/980]

                                                                             
``┌──(kali㉿kali)-[~/patch]
└─$ wget https://artifacts.picoctf.net/c/388/flag.txt.enc   
--2022-11-25 13:13:20--  https://artifacts.picoctf.net/c/388/flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.69, 13.249.74.22, 13.249.74.17, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.69|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 36 [application/octet-stream]
Saving to: ‘flag.txt.enc’

flag.txt.enc        100%[================>]      36  --.-KB/s    in 0s      

2022-11-25 13:13:21 (27.4 MB/s) - ‘flag.txt.enc’ saved [36/36]

                                                                             
``┌──(kali㉿kali)-[~/patch]
└─$ ls -la
total 16
drwxr-xr-x  2 kali kali 4096 Nov 25 13:13 .
drwxr-xr-x 61 kali kali 4096 Nov 25 13:12 ..
-rw-r--r--  1 kali kali   36 Mar 15  2022 flag.txt.enc
-rw-r--r--  1 kali kali  980 Mar 15  2022 patchme.flag.py
                                                                             
``┌──(kali㉿kali)-[~/patch]
└─$ nano patchme.flag.py 
                                                                             
``┌──(kali㉿kali)-[~/patch]
└─$ python3 ./patchme.flag.py ./flag.txt.enc 
  File "/home/kali/patch/./patchme.flag.py", line 19
    '''   if( user_pw == "ak98" + \
                                   ^
IndentationError: unindent does not match any outer indentation level
                                                                             
``┌──(kali㉿kali)-[~/patch]
└─$ nano patchme.flag.py                    
                                                                             
``┌──(kali㉿kali)-[~/patch]
└─$ python3 ./patchme.flag.py ./flag.txt.enc
  File "/home/kali/patch/./patchme.flag.py", line 19
    ''' if( user_pw == "ak98" + \
                                 ^
IndentationError: unindent does not match any outer indentation level
                                                                             
``┌──(kali㉿kali)-[~/patch]
└─$ nano patchme.flag.py                    
                                                                             
``┌──(kali㉿kali)-[~/patch]
└─$ python3 ./patchme.flag.py ./flag.txt.enc
  File "/home/kali/patch/./patchme.flag.py", line 26
    return
IndentationError: unexpected indent
                                                                             
``┌──(kali㉿kali)-[~/patch]
└─$ nano patchme.flag.py   
dentro del nano comentamos esta parte:                 
''' if( user_pw == "ak98" + \
                   "-=90" + \
                   "adfjhgj321" + \
                   "sleuth9000"):'''
  e identamos lo demas de manera correcta 
                                                                             
``┌──(kali㉿kali)-[~/patch]
└─$ python3 ./patchme.flag.py ./flag.txt.enc
Please enter correct password for flag: dsdg
Welcome back... your flag, user:
==picoCTF{p47ch1ng_l1f3_h4ck_21d62e33}==

## Referencias: