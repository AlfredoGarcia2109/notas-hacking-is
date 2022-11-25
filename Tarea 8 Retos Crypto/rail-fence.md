## Nombre del reto:
rail-fence

## Objetivo:
A type of transposition cipher is the rail fence cipher, which is described [here](https://en.wikipedia.org/wiki/Rail_fence_cipher). Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it?Download the message [here](https://artifacts.picoctf.net/c/274/message.txt).Put the decoded message in the picoCTF flag format, `picoCTF{decoded_message}`.

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir rail 
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd rail 
                                                                             
``┌──(kali㉿kali)-[~/rail]
└─$ wget https://artifacts.picoctf.net/c/274/message.txt   
--2022-11-23 14:07:26--  https://artifacts.picoctf.net/c/274/message.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.56, 13.249.74.17, 13.249.74.69, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.56|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 56 [application/octet-stream]
Saving to: ‘message.txt’

message.txt         100%[================>]      56  --.-KB/s    in 0s      

2022-11-23 14:07:27 (25.3 MB/s) - ‘message.txt’ saved [56/56]

                                                                             
``┌──(kali㉿kali)-[~/rail]
└─$ ls
message.txt
                                                                             
``┌──(kali㉿kali)-[~/rail]
└─$ cat message.txt           
Ta _7N6DDDhlg:W3D_H3C31N__0D3ef sHR053F38N43D0F i33___NA

The flag is: WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_D00AFDD3
==picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_D00AFDD3}==

  


## Referencias:
https://www.boxentriq.com/code-breaking/rail-fence-cipher