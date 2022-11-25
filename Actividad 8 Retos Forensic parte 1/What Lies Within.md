## Nombre del reto:
What Lies Within

## Objetivo:
There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir whatlies      
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd whatlies  
                                                                             
``┌──(kali㉿kali)-[~/whatlies]
└─$ wget https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png
--2022-11-24 12:40:55--  https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 625219 (611K) [application/octet-stream]
Saving to: ‘buildings.png’

buildings.png       100%[================>] 610.57K   152KB/s    in 4.0s    

2022-11-24 12:41:00 (152 KB/s) - ‘buildings.png’ saved [625219/625219]

                                                                             
``┌──(kali㉿kali)-[~/whatlies]
└─$ ls
buildings.png
                                                                             
``┌──(kali㉿kali)-[~/whatlies]
└─$ file buildings.png 
buildings.png: PNG image data, 657 x 438, 8-bit/color RGBA, non-interlaced
                                                                             
``┌──(kali㉿kali)-[~/whatlies]
└─$ open buildings.png 
                                                                             
``┌──(kali㉿kali)-[~/whatlies]
└─$ zsteg -a buildings.png | grep pico
b1,rgb,lsb,xy       .. text: "==picoCTF{h1d1ng_1n_th3_b1t5}=="

## Referencias: