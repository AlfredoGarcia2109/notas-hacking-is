## Nombre del reto:
m00nwalk

## Objetivo:
Decode this [message](https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav) from the moon.

## Solución:
``┌──(kali㉿kali)-[~]
└─$ mkdir m00nwalk
                                                                             
``┌──(kali㉿kali)-[~]
└─$ cd m00nwalk 
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk]
└─$ wget https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav  
--2022-11-24 12:46:22--  https://jupiter.challenges.picoctf.org/static/14393e18d98fedbaedbc28896d7ef31a/message.wav
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 11066998 (11M) [application/octet-stream]
Saving to: ‘message.wav’

message.wav         100%[================>]  10.55M   187KB/s    in 80s     

2022-11-24 12:47:44 (134 KB/s) - ‘message.wav’ saved [11066998/11066998]

                                                                             
``┌──(kali㉿kali)-[~/m00nwalk]
└─$ ls
message.wav
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk]
└─$ open message.wav 
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk]
└─$ mkdir repo    
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk]
└─$ cd repo    
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk/repo]
└─$ sudo git clone https://github.com/colaclanth/sstv.git
[sudo] password for kali: 
Cloning into 'sstv'...
remote: Enumerating objects: 221, done.
remote: Total 221 (delta 0), reused 0 (delta 0), pack-reused 221
Receiving objects: 100% (221/221), 1.01 MiB | 161.00 KiB/s, done.
Resolving deltas: 100% (140/140), done.
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk/repo]
└─$ sudo python3 setup.py install
python3: can't open file '/home/kali/m00nwalk/repo/setup.py': [Errno 2] No such file or directory
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk/repo]
└─$ cd sstv 
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk/repo/sstv]
└─$ sudo python3 setup.py install
running install
/usr/lib/python3/dist-packages/setuptools/command/install.py:34: SetuptoolsDeprecationWarning: setup.py install is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
/usr/lib/python3/dist-packages/setuptools/command/easy_install.py:158: EasyInstallDeprecationWarning: easy_install command is deprecated. Use build and pip and other standards-based tools.
  warnings.warn(
running bdist_egg
running egg_info
creating sstv.egg-info
writing sstv.egg-info/PKG-INFO
writing dependency_links to sstv.egg-info/dependency_links.txt
writing entry points to sstv.egg-info/entry_points.txt
writing requirements to sstv.egg-info/requires.txt
writing top-level names to sstv.egg-info/top_level.txt
writing manifest file 'sstv.egg-info/SOURCES.txt'
reading manifest file 'sstv.egg-info/SOURCES.txt'
adding license file 'LICENSE'
writing manifest file 'sstv.egg-info/SOURCES.txt'
installing library code to build/bdist.linux-x86_64/egg
running install_lib
running build_py
creating build
creating build/lib
creating build/lib/sstv
copying sstv/common.py -> build/lib/sstv
copying sstv/command.py -> build/lib/sstv
copying sstv/__main__.py -> build/lib/sstv
copying sstv/decode.py -> build/lib/sstv
copying sstv/__init__.py -> build/lib/sstv
copying sstv/spec.py -> build/lib/sstv
creating build/bdist.linux-x86_64
creating build/bdist.linux-x86_64/egg
creating build/bdist.linux-x86_64/egg/sstv
copying build/lib/sstv/common.py -> build/bdist.linux-x86_64/egg/sstv
copying build/lib/sstv/command.py -> build/bdist.linux-x86_64/egg/sstv
copying build/lib/sstv/__main__.py -> build/bdist.linux-x86_64/egg/sstv
copying build/lib/sstv/decode.py -> build/bdist.linux-x86_64/egg/sstv
copying build/lib/sstv/__init__.py -> build/bdist.linux-x86_64/egg/sstv
copying build/lib/sstv/spec.py -> build/bdist.linux-x86_64/egg/sstv
byte-compiling build/bdist.linux-x86_64/egg/sstv/common.py to common.cpython-310.pyc
byte-compiling build/bdist.linux-x86_64/egg/sstv/command.py to command.cpython-310.pyc
byte-compiling build/bdist.linux-x86_64/egg/sstv/__main__.py to __main__.cpython-310.pyc
byte-compiling build/bdist.linux-x86_64/egg/sstv/decode.py to decode.cpython-310.pyc
byte-compiling build/bdist.linux-x86_64/egg/sstv/__init__.py to __init__.cpython-310.pyc
byte-compiling build/bdist.linux-x86_64/egg/sstv/spec.py to spec.cpython-310.pyc
creating build/bdist.linux-x86_64/egg/EGG-INFO
copying sstv.egg-info/PKG-INFO -> build/bdist.linux-x86_64/egg/EGG-INFO
copying sstv.egg-info/SOURCES.txt -> build/bdist.linux-x86_64/egg/EGG-INFO
copying sstv.egg-info/dependency_links.txt -> build/bdist.linux-x86_64/egg/EGG-INFO
copying sstv.egg-info/entry_points.txt -> build/bdist.linux-x86_64/egg/EGG-INFO
copying sstv.egg-info/requires.txt -> build/bdist.linux-x86_64/egg/EGG-INFO
copying sstv.egg-info/top_level.txt -> build/bdist.linux-x86_64/egg/EGG-INFO
zip_safe flag not set; analyzing archive contents...
creating dist
creating 'dist/sstv-0.1-py3.10.egg' and adding 'build/bdist.linux-x86_64/egg' to it
removing 'build/bdist.linux-x86_64/egg' (and everything under it)
Processing sstv-0.1-py3.10.egg
Copying sstv-0.1-py3.10.egg to /usr/local/lib/python3.10/dist-packages
Adding sstv 0.1 to easy-install.pth file
Installing sstv script to /usr/local/bin

Installed /usr/local/lib/python3.10/dist-packages/sstv-0.1-py3.10.egg
Processing dependencies for sstv=0.1
Searching for PySoundFile
Reading https://pypi.org/simple/PySoundFile/
/usr/lib/python3/dist-packages/pkg_resources/__init__.py:116: PkgResourcesDeprecationWarning:  is an invalid version and will not be supported in a future release
  warnings.warn(
Downloading https://files.pythonhosted.org/packages/2a/b3/0b871e5fd31b9a8e54b4ee359384e705a1ca1e2870706d2f081dc7cc1693/PySoundFile-0.9.0.post1-py2.py3-none-any.whl#sha256=db14f84f4af1910f54766cf0c0f19d52414fa80aa0e11cb338b5614946f39947
Best match: PySoundFile 0.9.0.post1
Processing PySoundFile-0.9.0.post1-py2.py3-none-any.whl
Installing PySoundFile-0.9.0.post1-py2.py3-none-any.whl to /usr/local/lib/python3.10/dist-packages
Adding PySoundFile 0.9.0.post1 to easy-install.pth file

Installed /usr/local/lib/python3.10/dist-packages/PySoundFile-0.9.0.post1-py3.10.egg
Searching for scipy=1.7.3
Best match: scipy 1.7.3
Adding scipy 1.7.3 to easy-install.pth file

Using /usr/lib/python3/dist-packages
Searching for numpy=1.21.5
Best match: numpy 1.21.5
Adding numpy 1.21.5 to easy-install.pth file
Installing f2py script to /usr/local/bin
Installing f2py3 script to /usr/local/bin
Installing f2py3.10 script to /usr/local/bin

Using /usr/lib/python3/dist-packages
Searching for Pillow=9.2.0
Best match: Pillow 9.2.0
Adding Pillow 9.2.0 to easy-install.pth file

Using /usr/lib/python3/dist-packages
Searching for cffi=1.15.1
Best match: cffi 1.15.1
Adding cffi 1.15.1 to easy-install.pth file

Using /usr/lib/python3/dist-packages
Finished processing dependencies for sstv=0.1
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk/repo/sstv]
└─$ cd .   
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk/repo/sstv]
└─$ cd ..
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk/repo]
└─$ sstv -d message.wav -o flag.png
usage: sstv [-h] [-d AUDIO_FILE] [-o OUTPUT_FILE] [-s SKIP] [-V]
            [--list-modes] [--list-audio-formats] [--list-image-formats]
sstv: error: argument -d/--decode: can't open 'message.wav': [Errno 2] No such file or directory: 'message.wav'
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk/repo]
└─$ ls
sstv
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk/repo]
└─$ cd sstv 
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk/repo/sstv]
└─$ ls
build  examples  README.md  sstv           test
dist   LICENSE   setup.py   sstv.egg-info
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk/repo/sstv]
└─$ cd ..  
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk/repo]
└─$ cd ..
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk]
└─$ ls
message.wav  repo
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk]
└─$ sstv -d message.wav -o flag.png
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [###########################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
                                                                             
``┌──(kali㉿kali)-[~/m00nwalk]
└─$ open flag.png  


==picoCTF{beep_boop_im_in_space}==

## Referencias: