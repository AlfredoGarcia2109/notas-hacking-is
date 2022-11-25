## Nombre del reto:
Glory of the Garden

## Objetivo:
This [garden](https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg) contains more than it seems.

## Solución:
``
``┌──(kali㉿kali)-[~]
└─$ mkdir garden 
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd garden
                                                                             
``┌──(kali㉿kali)-[~/garden]
└─$ wget https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg
--2022-11-24 12:11:09--  https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2295192 (2.2M) [application/octet-stream]
Saving to: ‘garden.jpg’

garden.jpg          100%[================>]   2.19M   158KB/s    in 11s     

2022-11-24 12:11:28 (203 KB/s) - ‘garden.jpg’ saved [2295192/2295192]

                                                                             
``┌──(kali㉿kali)-[~/garden]
└─$ ls
garden.jpg
                                                                             
``┌──(kali㉿kali)-[~/garden]
└─$ strings garden.jpg | grep pico        
Here is a flag "==picoCTF{more_than_m33ts_the_3y3eBdBd2cc}=="

## Referencias: