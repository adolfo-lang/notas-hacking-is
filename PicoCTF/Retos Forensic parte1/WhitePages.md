## whitepages

# objetivo
- I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/95be9526e162185c741259a75dffa0ab/whitepages.txt) is all blank!

# Hints
- 
# solucion
``` bash 

(kali㉿kali)-[~/Downloads]
└─$ cat whitepages.txt
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads]
└─$ file whitepages.txt
whitepages.txt: Unicode text, UTF-8 text, with very long lines (1376), with no line terminators
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads]
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
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads]
└─$ python3 -m pip install pwntools                     
Defaulting to user installation because normal site-packages is not writeable
Collecting pwntools
  Downloading pwntools-4.8.0-py2.py3-none-any.whl (11.7 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 11.7/11.7 MB 4.2 MB/s eta 0:00:00
Requirement already satisfied: pip>=6.0.8 in /usr/lib/python3/dist-packages (from pwntools) (22.2)
Requirement already satisfied: pysocks in /usr/lib/python3/dist-packages (from pwntools) (1.7.1)
Collecting unicorn>=1.0.2rc1
  Downloading unicorn-2.0.0-py2.py3-none-manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (16.1 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 16.1/16.1 MB 3.7 MB/s eta 0:00:00
Collecting capstone>=3.0.5rc2
  Downloading capstone-5.0.0rc2-py3-none-manylinux1_x86_64.manylinux_2_5_x86_64.whl (2.8 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2.8/2.8 MB 5.7 MB/s eta 0:00:00
Collecting colored-traceback
  Downloading colored-traceback-0.3.0.tar.gz (3.8 kB)
  Preparing metadata (setup.py) ... done
Collecting rpyc
  Downloading rpyc-5.2.3-py3-none-any.whl (71 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 71.3/71.3 kB 2.3 MB/s eta 0:00:00
Requirement already satisfied: pyserial>=2.7 in /usr/lib/python3/dist-packages (from pwntools) (3.5)
Requirement already satisfied: pygments>=2.0 in /usr/lib/python3/dist-packages (from pwntools) (2.12.0)
Collecting pathlib2
  Downloading pathlib2-2.3.7.post1-py2.py3-none-any.whl (18 kB)
Requirement already satisfied: python-dateutil in /usr/lib/python3/dist-packages (from pwntools) (2.8.1)
Requirement already satisfied: packaging in /usr/lib/python3/dist-packages (from pwntools) (21.3)
Requirement already satisfied: mako>=1.0.0 in /usr/lib/python3/dist-packages (from pwntools) (1.2.2)
Collecting pyelftools>=0.2.4
  Downloading pyelftools-0.29-py2.py3-none-any.whl (174 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 174.3/174.3 kB 1.6 MB/s eta 0:00:00
Requirement already satisfied: requests>=2.0 in /usr/lib/python3/dist-packages (from pwntools) (2.27.1)
Requirement already satisfied: six>=1.12.0 in /usr/lib/python3/dist-packages (from pwntools) (1.16.0)
Collecting psutil>=3.3.0
  Downloading psutil-5.9.3-cp310-cp310-manylinux_2_12_x86_64.manylinux2010_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (292 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 292.3/292.3 kB 2.6 MB/s eta 0:00:00
Collecting intervaltree>=3.0
  Downloading intervaltree-3.1.0.tar.gz (32 kB)
  Preparing metadata (setup.py) ... done
Requirement already satisfied: paramiko>=1.15.2 in /usr/lib
Collecting ropgadget>=5.3
  Downloading ROPGadget-7.1-py3-none-any.whl (31 kB)
Requirement already satisfied: sortedcontainers in /usr/lib
Collecting plumbum
  Downloading plumbum-1.8.0-py3-none-any.whl (117 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 117.5/117.5 k
Building wheels for collected packages: intervaltree, color
  Building wheel for intervaltree (setup.py) ... done
                                                           
┌──(kali㉿kali)-[~/Downloads]
└─$ nano exp.py
--------
ffrom pwn import *
file = open('whitepages.txt','rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83',b'0')
data = data.replace(b'\x20',b'1')
data = data.decode('ascii')
data = unbits(data)
print(data)

(kali㉿kali)-[~/Downloads]
└─$ python3 exp.py
b'\n\t\tpicoCTF\n\n\t\tSEE PUBLIC RECORDS & BACKGROUND REPORT\n\t\t5000 Forbes Ave, Pittsburgh, PA 15213\n\t\tpicoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}\n\t\t'
```
# bandera
- picoCTF{not_all_spaces_are_created_equal_7100860b0fa779a5bd8ce29f24f586dc}