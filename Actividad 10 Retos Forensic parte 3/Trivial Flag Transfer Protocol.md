## Nombre del reto:
Trivial Flag Transfer Protocol

## Objetivo:
Figure out how they moved the [flag](https://mercury.picoctf.net/static/88553d672efbccbc5868002f4c6eb737/tftp.pcapng).

## Solución:
``┌──(kali㉿kali)-[~/trivialflag]
└─$ file tftp.pcapng       
tftp.pcapng: pcapng capture file - version 1.0
                                                                             
``┌──(kali㉿kali)-[~/trivialflag]
└─$ wireshark tftp.pcapng
 ** (wireshark:5024) 19:54:24.123083 [GUI WARNING] -- FIX Add drag reordering to UAT dialog
                                                                             
``┌──(kali㉿kali)-[~/trivialflag]
└─$ ls    
instructions.txt  picture2.bmp  plan         tftp.pcapng
picture1.bmp      picture3.bmp  program.deb
                                                                             
``┌──(kali㉿kali)-[~/trivialflag]
└─$ cat instructions.txt
GSGCQBRFAGRAPELCGBHEGENSSVPFBJRZHFGQVFTHVFRBHESYNTGENAFSRE.SVTHERBHGNJNLGBUVQRGURSYNTNAQVJVYYPURPXONPXSBEGURCYNA
                                                                             
``┌──(kali㉿kali)-[~/trivialflag]
└─$ cat plan                       
VHFRQGURCEBTENZNAQUVQVGJVGU-QHRQVYVTRAPR.PURPXBHGGURCUBGBF
                                                                             
``┌──(kali㉿kali)-[~/trivialflag]
└─$ dpkg -I program.deb 
 new Debian package, version 2.0.
 size 138310 bytes: control archive=1250 bytes.
     826 bytes,    18 lines      control              
    1184 bytes,    17 lines      md5sums              
 Package: steghide
 Source: steghide (0.5.1-9.1)
 Version: 0.5.1-9.1+b1
 Architecture: amd64
 Maintainer: Ola Lundqvist <opal@debian.org>
 Installed-Size: 426
 Depends: libc6 (>= 2.2.5), libgcc1 (>= 1:4.1.1), libjpeg62-turbo (>= 1:1.3.1), libmcrypt4, libmhash2, libstdc++6 (>= 4.9), zlib1g (>= 1:1.1.4)
 Section: misc
 Priority: optional
 Description: A steganography hiding tool
  Steghide is steganography program which hides bits of a data file
  in some of the least significant bits of another file in such a way
  that the existence of the data file is not visible and cannot be proven.
  .
  Steghide is designed to be portable and configurable and features hiding
  data in bmp, wav and au files, blowfish encryption, MD5 hashing of
  passphrases to blowfish keys, and pseudo-random distribution of hidden bits
  in the container data.
                                                                             
``┌──(kali㉿kali)-[~/trivialflag]
└─$ sudo dpkg -i program.deb
[sudo] password for kali: 
Selecting previously unselected package steghide.
(Reading database ... 338375 files and directories currently installed.)
Preparing to unpack program.deb ...
Unpacking steghide (0.5.1-9.1+b1) ...
       
               
``┌──(kali㉿kali)-[~/trivialflag]
└─$ cat flag.txt                
==picoCTF{h1dd3n_1n_pLa1n_51GHT_18375919}==

## Referencias: