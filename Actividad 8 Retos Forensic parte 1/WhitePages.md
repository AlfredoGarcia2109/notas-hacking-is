## Nombre del reto:
WhitePages

## Objetivo:
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt) is all blank!

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir white   
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd white 
                                                                             
``┌──(kali㉿kali)-[~/white]
└─$ wget https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt
--2022-11-24 13:07:19--  https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2982 (2.9K) [application/octet-stream]
Saving to: ‘whitepages.txt’

whitepages.txt      100%[================>]   2.91K  --.-KB/s    in 0s      

2022-11-24 13:07:20 (42.3 MB/s) - ‘whitepages.txt’ saved [2982/2982]

                                                                             
``┌──(kali㉿kali)-[~/white]
└─$ ls                
whitepages.txt
                                                                             
``┌──(kali㉿kali)-[~/white]
└─$ file whitepages.txt 
whitepages.txt: Unicode text, UTF-8 text, with very long lines (1376), with no line terminators
                                                                             
``┌──(kali㉿kali)-[~/white]
└─$ xxd whitepages.txt | head
00000000: e280 83e2 8083 e280 83e2 8083 20e2 8083  ............ ...
00000010: 20e2 8083 e280 83e2 8083 e280 83e2 8083   ...............
00000020: 20e2 8083 e280 8320 e280 83e2 8083 e280   ...... ........
00000030: 83e2 8083 20e2 8083 e280 8320 e280 8320  .... ...... ... 
00000040: 2020 e280 83e2 8083 e280 83e2 8083 e280    ..............
00000050: 8320 20e2 8083 20e2 8083 e280 8320 e280  .  ... ...... ..
00000060: 8320 20e2 8083 e280 83e2 8083 2020 e280  .  .........  ..
00000070: 8320 20e2 8083 2020 2020 e280 8320 e280  .  ...    ... ..
00000080: 83e2 8083 e280 83e2 8083 2020 e280 8320  ..........  ... 
00000090: e280 8320 e280 8320 e280 83e2 8083 e280  ... ... ........
                                                                             
``┌──(kali㉿kali)-[~/white]
└─$ python3 -m install pwntools
/usr/bin/python3: No module named install
                                                                             
``┌──(kali㉿kali)-[~/white]
└─$ python3 -m pip install pwntools
Defaulting to user installation because normal site-packages is not writeable
Collecting pwntools
  Downloading pwntools-4.8.0-py2.py3-none-any.whl (11.7 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 11.7/11.7 MB 161.0 kB/s eta 0:00:00
Requirement already satisfied: python-dateutil in /usr/lib/python3/dist-packages (from pwntools) (2.8.1)
Requirement already satisfied: mako>=1.0.0 in /usr/lib/python3/dist-packages (from pwntools) (1.1.3)
Requirement already satisfied: pip>=6.0.8 in /usr/lib/python3/dist-packages (from pwntools) (22.2)
Requirement already satisfied: paramiko>=1.15.2 in /usr/lib/python3/dist-packages (from pwntools) (2.10.4)
Collecting unicorn>=1.0.2rc1
  Downloading unicorn-2.0.1.post1-py2.py3-none-manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (16.1 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 16.1/16.1 MB 174.7 kB/s eta 0:00:00
Collecting rpyc
  Downloading rpyc-5.2.3-py3-none-any.whl (71 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 71.3/71.3 kB 128.3 kB/s eta 0:00:00
Collecting ropgadget>=5.3
  Downloading ROPGadget-7.1-py3-none-any.whl (31 kB)
Collecting intervaltree>=3.0
  Downloading intervaltree-3.1.0.tar.gz (32 kB)
  Preparing metadata (setup.py) ... done
Requirement already satisfied: pygments>=2.0 in /usr/lib/python3/dist-packages (from pwntools) (2.12.0)
Requirement already satisfied: sortedcontainers in /usr/lib/python3/dist-packages (from pwntools) (2.4.0)
Requirement already satisfied: packaging in /usr/lib/python3/dist-packages (from pwntools) (21.3)
Requirement already satisfied: pysocks in /usr/lib/python3/dist-packages (from pwntools) (1.7.1)
Requirement already satisfied: requests>=2.0 in /usr/lib/python3/dist-packages (from pwntools) (2.27.1)
Collecting pathlib2
  Downloading pathlib2-2.3.7.post1-py2.py3-none-any.whl (18 kB)
Requirement already satisfied: six>=1.12.0 in /usr/lib/python3/dist-packages (from pwntools) (1.16.0)
Collecting capstone>=3.0.5rc2
  Downloading capstone-5.0.0rc2-py3-none-manylinux1_x86_64.manylinux_2_5_x86_64.whl (2.8 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.8/2.8 MB 252.3 kB/s eta 0:00:00
Collecting psutil>=3.3.0
  Downloading psutil-5.9.4-cp36-abi3-manylinux_2_12_x86_64.manylinux2010_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (280 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 280.2/280.2 kB 156.1 kB/s eta 0:00:00
Collecting colored-traceback
  Downloading colored-traceback-0.3.0.tar.gz (3.8 kB)
  Preparing metadata (setup.py) ... done
Collecting pyelftools>=0.2.4
  Downloading pyelftools-0.29-py2.py3-none-any.whl (174 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 174.3/174.3 kB 125.7 kB/s eta 0:00:00
Requirement already satisfied: pyserial>=2.7 in /usr/lib/python3/dist-packages (from pwntools) (3.5)
Collecting plumbum
  Downloading plumbum-1.8.0-py3-none-any.whl (117 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 117.5/117.5 kB 4.3 kB/s eta 0:00:00
Building wheels for collected packages: intervaltree, colored-traceback
  Building wheel for intervaltree (setup.py) ... done
  Created wheel for intervaltree: filename=intervaltree-3.1.0-py2.py3-none-any.whl size=26119 sha256=6a3cf841c32fc2f2c319f476fc2ef82888e9f42d71726aef766de1ab2bde09f8
  Stored in directory: /home/kali/.cache/pip/wheels/fa/80/8c/43488a924a046b733b64de3fac99252674c892a4c3801c0a61
  Building wheel for colored-traceback (setup.py) ... done
  Created wheel for colored-traceback: filename=colored_traceback-0.3.0-py3-none-any.whl size=4622 sha256=d0677ca584e6e4b5732ff751d7c7e2e58ae1b4c860e4539d0d0bc43044b7ebcb
  Stored in directory: /home/kali/.cache/pip/wheels/10/49/bd/750e09783fb038570efede2d03819a7141fc2350de51daf575
Successfully built intervaltree colored-traceback
Installing collected packages: unicorn, pyelftools, psutil, plumbum, pathlib2, intervaltree, colored-traceback, capstone, rpyc, ropgadget, pwntools
  WARNING: The scripts rpyc_classic, rpyc_classic.py, rpyc_registry and rpyc_registry.py are installed in '/home/kali/.local/bin' which is not on PATH.   
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.                                       
  WARNING: The scripts asm, checksec, common, constgrep, cyclic, debug, disablenx, disasm, elfdiff, elfpatch, errno, hex, main, phd, pwn, pwnstrip, scramble, shellcraft, template, unhex, update and version are installed in '/home/kali/.local/bin' which is not on PATH.                                        
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.                                       
Successfully installed capstone-5.0.0rc2 colored-traceback-0.3.0 intervaltree-3.1.0 pathlib2-2.3.7.post1 plumbum-1.8.0 psutil-5.9.4 pwntools-4.8.0 pyelftools-0.29 ropgadget-7.1 rpyc-5.2.3 unicorn-2.0.1.post1
                                                                             
``┌──(kali㉿kali)-[~/white]
└─$ nano flag.py
                                                                             
``┌──(kali㉿kali)-[~/white]
└─$ python3 flag.py                
b'\n\t\tpicoCTF\n\n\t\tSEE PUBLIC RECORDS & BACKGROUND REPORT\n\t\t5000 Forbes Ave, Pittsburgh, PA 15213\n\t\t==picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}==\n\t\t'

## Referencias: