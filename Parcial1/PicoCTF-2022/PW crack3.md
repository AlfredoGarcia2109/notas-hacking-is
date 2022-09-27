# Nombre del reto:
PW Crack 3

# Objetivo:
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/23/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/23/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/23/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
# Solución:
"6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"

                                                                             
┌──(kali㉿kali)-[~/Downloads]
``└─$ nano level3.py 
                                                                             
┌──(kali㉿kali)-[~/Downloads]
``└─$ python level3.py 
Traceback (most recent call last):
  File "/home/kali/Downloads/level3.py", line 14, in module>
    flag_enc = open('level3.flag.txt.enc', 'rb').read()
FileNotFoundError: [Errno 2] No such file or directory: 'level3.flag.txt.enc'
                                                                             
┌──(kali㉿kali)-[~/Downloads]
``└─$ python level3.py
Please enter correct password for flag: 6997
That password is incorrect
                                                                             
┌──(kali㉿kali)-[~/Downloads]
``└─$ python level3.py
Please enter correct password for flag:  
That password is incorrect
                                                                             
┌──(kali㉿kali)-[~/Downloads]
``└─$ 
                                                                             
┌──(kali㉿kali)-[~/Downloads]
``└─$ python level3.py
Please enter correct password for flag: f0ac
That password is incorrect
                                                                             
┌──(kali㉿kali)-[~/Downloads]
``└─$ python level3.py
Please enter correct password for flag: 4b17
Welcome back... your flag, user:
==picoCTF{m45h_fl1ng1ng_2b072a90}

# Referencias: