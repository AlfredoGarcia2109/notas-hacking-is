## Nombre del reto:
WebNet1

## Objetivo:
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir webnet1
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd webnet1
                                                                             
``┌──(kali㉿kali)-[~/webnet1]
└─$ wget https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap
--2022-11-24 18:16:03--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 92525 (90K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap        100%[================>]  90.36K   118KB/s    in 0.8s    

2022-11-24 18:16:06 (118 KB/s) - ‘capture.pcap’ saved [92525/92525]

                                                                             
``┌──(kali㉿kali)-[~/webnet1]
└─$ wget https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
--2022-11-24 18:16:22--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key’

picopico.key        100%[================>]   1.66K  --.-KB/s    in 0s      

2022-11-24 18:16:23 (25.8 MB/s) - ‘picopico.key’ saved [1704/1704]

                                                                             
``┌──(kali㉿kali)-[~/webnet1]
└─$ wireshark capture.pcap 
 ** (wireshark:18875) 18:17:08.815584 [GUI WARNING] -- FIX Add drag reordering to UAT dialog
                                                                             
``┌──(kali㉿kali)-[~/webnet1]
└─$ ls    
capture.pcap  picopico.key  vulture.jpg
 cargamos la llave en el protocolo tls, despues guardamos la imagen que esta dentro de los paquetes y le hacemos un strings
                                                                            
``┌──(kali㉿kali)-[~/webnet1]
└─$ strings vulture.jpg
JFIF
Exif
==picoCTF{honey.roasted.peanuts}==

## Referencias:
