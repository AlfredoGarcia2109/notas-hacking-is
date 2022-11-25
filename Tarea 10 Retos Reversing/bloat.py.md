## Nombre del reto:
bloat.py

## Objetivo:
Can you get the flag?Run this [Python program](https://artifacts.picoctf.net/c/430/bloat.flag.py) in the same directory as this [encrypted flag](https://artifacts.picoctf.net/c/430/flag.txt.enc).

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir bloat
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd bloat
                                                                             
``┌──(kali㉿kali)-[~/bloat]
└─$ wget https://artifacts.picoctf.net/c/430/bloat.flag.py
--2022-11-25 12:58:42--  https://artifacts.picoctf.net/c/430/bloat.flag.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.192.79, 99.84.192.17, 99.84.192.11, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.192.79|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1557 (1.5K) [application/octet-stream]
Saving to: ‘bloat.flag.py’

bloat.flag.py       100%[================>]   1.52K  --.-KB/s    in 0s      

2022-11-25 12:58:54 (21.5 MB/s) - ‘bloat.flag.py’ saved [1557/1557]

                                                                             
``┌──(kali㉿kali)-[~/bloat]
└─$ wget https://artifacts.picoctf.net/c/430/flag.txt.enc 
--2022-11-25 12:59:16--  https://artifacts.picoctf.net/c/430/flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.192.2, 99.84.192.79, 99.84.192.17, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.192.2|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 35 [application/octet-stream]
Saving to: ‘flag.txt.enc’

flag.txt.enc        100%[================>]      35  --.-KB/s    in 0s      

2022-11-25 12:59:17 (28.5 MB/s) - ‘flag.txt.enc’ saved [35/35]

                                                                             
``┌──(kali㉿kali)-[~/bloat]
└─$ ls    
bloat.flag.py  flag.txt.enc
                                                                             
``┌──(kali㉿kali)-[~/bloat]
└─$ python3 ./bloat.flag.py ./flag.txt.enc             
Please enter correct password for flag: jhdag
That password is incorrect
                                                                             
``┌──(kali㉿kali)-[~/bloat]
└─$ nano bloat.flag.py                              
  dentro del bloat solo comentamos el primer sys.exit(0)  
                                                                           
``┌──(kali㉿kali)-[~/bloat]
└─$ python3 ./bloat.flag.py ./flag.txt.enc
Please enter correct password for flag: dsgsfg
That password is incorrect
Welcome back... your flag, user:
==picoCTF{d30bfu5c4710n_f7w_5e14b257}==

## Referencias: