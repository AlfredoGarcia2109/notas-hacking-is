## Nombre del reto:
morse-code

## Objetivo:
Morse code is well known. Can you decrypt this?Download the file [here](https://artifacts.picoctf.net/c/235/morse_chal.wav).Wrap your answer with picoCTF{}, put underscores in place of pauses, and use all lowercase.

## Solución:
``┌──(kali㉿kali)-[~/morse]
└─$ wget https://artifacts.picoctf.net/c/235/morse_chal.wav
--2022-11-23 13:42:46--  https://artifacts.picoctf.net/c/235/morse_chal.wav
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.17, 13.249.74.56, 13.249.74.69, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.17|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2549024 (2.4M) [application/octet-stream]
Saving to: ‘morse_chal.wav’

morse_chal.wav      100%[================>]   2.43M   361KB/s    in 7.1s    

2022-11-23 13:42:55 (350 KB/s) - ‘morse_chal.wav’ saved [2549024/2549024]

                                                                             
``┌──(kali㉿kali)-[~/morse]
└─$ python3        
Python 3.10.5 (main, Jun  8 2022, 09:26:22) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> "W H 4 7 H 4 7 H 9 0 D W 2 0 U 9 H 7".lower().replace(' ','')
'wh47h47h90dw20u9h7'
==picoCTF{wh47_h47h_90d_w20u9h7}==




## Referencias:
https://morsecode.world/international/decoder/audio-decoder-adaptive.html
