## Nombre del reto:
The Numbers

## Objetivo:
The [numbers](https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png)... what do they mean?

## Solución:
The Numbers
-----------------------------------------
``┌──(kali㉿kali)-[~]
└─$ mkdir number  
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd number   
                                                                             
``┌──(kali㉿kali)-[~/number]
└─$ wget https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png
--2022-11-24 21:49:48--  https://jupiter.challenges.picoctf.org/static/f209a32253affb6f547a585649ba4fda/the_numbers.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 100721 (98K) [application/octet-stream]
Saving to: ‘the_numbers.png’

the_numbers.png     100%[================>]  98.36K   136KB/s    in 0.7s    

2022-11-24 21:49:50 (136 KB/s) - ‘the_numbers.png’ saved [100721/100721]

                                                                             
``┌──(kali㉿kali)-[~/number]
└─$ open the_numbers.png 

se utiliza a1z26 en ciberchef para la encriptacion: picoctf.thenumbersmason.
==picoCTF{thenumbersmason}==
## Referencias: