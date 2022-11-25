## Nombre del reto:
caesar

## Objetivo:
Decrypt this [message](https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext).

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir caesar
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd caesar 
                                                                             
``┌──(kali㉿kali)-[~/caesar]
└─$ wget https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext
--2022-11-24 22:07:08--  https://jupiter.challenges.picoctf.org/static/49f31c8f17817dc2d367428c9e5ab0bc/ciphertext
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 35 [application/octet-stream]
Saving to: ‘ciphertext’

ciphertext          100%[================>]      35  --.-KB/s    in 0s      

2022-11-24 22:07:09 (19.6 MB/s) - ‘ciphertext’ saved [35/35]

                                                                             
``┌──(kali㉿kali)-[~/caesar]
└─$ file ciphertext             
ciphertext: ASCII text, with no line terminators
                                                                             
``┌──(kali㉿kali)-[~/caesar]
└─$ cat ciphertext 
picoCTF{ynkooejcpdanqxeykjrbdofgkq} 
*con ayuda de ciberchef encontramos la bandera:*
==picoCTF{crossingtherubiconvfhsjkou}==

## Referencias: