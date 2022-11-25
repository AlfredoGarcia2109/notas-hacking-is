## Nombre del reto:
extensions

## Objetivo:
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir extensions
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd extensions 
                                                                             
``┌──(kali㉿kali)-[~/extensions]
└─$ wget https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt    
--2022-11-24 12:35:48--  https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9984 (9.8K) [application/octet-stream]
Saving to: ‘flag.txt’

flag.txt            100%[================>]   9.75K  --.-KB/s    in 0s      

2022-11-24 12:35:50 (67.6 MB/s) - ‘flag.txt’ saved [9984/9984]

                                                                             
``┌──(kali㉿kali)-[~/extensions]
└─$ ls
flag.txt
                                                                             
``┌──(kali㉿kali)-[~/extensions]
└─$ file flag.txt    
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
                                                                             
``┌──(kali㉿kali)-[~/extensions]
└─$ mv flag.txt flag.png
                                                                             
``┌──(kali㉿kali)-[~/extensions]
└─$ open flag.png 

==picoCTF{now_you_know_about_extensions}==

## Referencias: