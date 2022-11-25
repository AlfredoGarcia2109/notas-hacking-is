## Nombre del reto:
Mind your Ps and Qs

## Objetivo:
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/38f30029ab93478310e906d3d084a4c1/values)

## Solución:
``┌──(kali㉿kali)-[~/mind]
└─$ python3 flag.py -n 831416828080417866340504968188990032810316193533653516022175784399720141076262857 -e 65537 --uncipher 240986837130071017759137533082982207147971245672412893755780400885108149004760496


private argument is not set, the private key will not be displayed, even if recovered.

[*] Testing key /tmp/tmpezjg86am.
attack initialized...
[*] Performing smallq attack on /tmp/tmpezjg86am.
[*] Performing factordb attack on /tmp/tmpezjg86am.
[*] Attack success with factordb method !

Results for /tmp/tmpezjg86am:

Unciphered data :
HEX : 0x7069636f4354467b736d6131315f4e5f6e305f67306f645f32333534303336387d
INT (big endian) : 13016382529449106065927291425342535437996222135352905256639592405461024281868413
INT (little endian) : 14499436437215324629163244483024452477715848127212044465501836292547934115031408
utf-8 : ==picoCTF{sma11_N_n0_g0od_23540368}==

## Referencias: