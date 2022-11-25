## Nombre del reto:
unpackme.py

## Objetivo:
Can you get the flag?Reverse engineer this [Python program](https://artifacts.picoctf.net/c/466/unpackme.flag.py).

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir unpackme
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd unpackme 
                                                                             
``┌──(kali㉿kali)-[~/unpackme]
└─$ wget https://artifacts.picoctf.net/c/466/unpackme.flag.py
--2022-11-25 13:22:32--  https://artifacts.picoctf.net/c/466/unpackme.flag.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.17, 13.249.74.69, 13.249.74.56, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.17|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 527 [application/octet-stream]
Saving to: ‘unpackme.flag.py’

unpackme.flag.py    100%[================>]     527  --.-KB/s    in 0s      

2022-11-25 13:22:35 (4.39 MB/s) - ‘unpackme.flag.py’ saved [527/527]

                                                                             
``┌──(kali㉿kali)-[~/unpackme]
└─$ ls -la
total 12
drwxr-xr-x  2 kali kali 4096 Nov 25 13:22 .
drwxr-xr-x 62 kali kali 4096 Nov 25 13:22 ..
-rw-r--r--  1 kali kali  527 Mar 15  2022 unpackme.flag.py
                                                                             
``┌──(kali㉿kali)-[~/unpackme]
└─$ python3 unpackme.flag.py                
What's the password? jg
That password is incorrect.
                                                                             
``┌──(kali㉿kali)-[~/unpackme]
└─$ nano unpackme.flag.py 
                                                                             
``┌──(kali㉿kali)-[~/unpackme]
└─$ python3 unpackme.flag.py

pw = input('What\'s the password? ')

if pw == 'batteryhorse':
  print('==picoCTF{175_chr157m45_85f5d0ac}==')
else:
  print('That password is incorrect.')

## Referencias: