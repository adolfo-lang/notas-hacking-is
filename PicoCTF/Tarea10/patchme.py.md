## patchme.py

# objetivo
- Can you get the flag? Run this [Python program](https://artifacts.picoctf.net/c/386/patchme.flag.py) in the same directory as this [encrypted flag](https://artifacts.picoctf.net/c/386/flag.txt.enc).

# Hints
- 

# solucion
``` bash 
(kali㉿kali)-[~/reversing]
└─$ wget https://artifacts.picoctf.net/c/386/patchme.flag.py                               
--2022-11-24 15:52:45--  https://artifacts.picoctf.net/c/386/patchme.flag.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.149.62, 65.9.149.123, 65.9.149.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.149.62|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 980 [application/octet-stream]
Saving to: ‘patchme.flag.py’

patchme.flag.p 100%     980  --.-KB/s    in 0s          

2022-11-24 15:52:46 (2.79 MB/s) - ‘patchme.flag.py’ saved [980/980]

                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ wget https://artifacts.picoctf.net/c/386/flag.txt.enc 
--2022-11-24 15:52:59--  https://artifacts.picoctf.net/c/386/flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.149.57, 65.9.149.85, 65.9.149.123, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.149.57|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 36 [application/octet-stream]
Saving to: ‘flag.txt.enc’

flag.txt.enc   100%      36  --.-KB/s    in 0s          

2022-11-24 15:52:59 (26.0 MB/s) - ‘flag.txt.enc’ saved [36/36]

                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ ls
flag.txt.enc  gdbme  patchme.flag.py
(kali㉿kali)-[~/reversing]
└─$ nano patchme.flag.py 

ak98" + \
                   "-=90" + \
                   "adfjhgj321" + \
                   "sleuth9000
(kali㉿kali)-[~/reversing]
└─$ python3 ./patchme.flag.py ./flag.txt.enc
Please enter correct password for flag: 
That password is incorrect
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ nano patchme.flag.py                    
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ python3 ./patchme.flag.py ./flag.txt.enc
Please enter correct password for flag: ak98-=90adfjhgj321sleuth9000
Welcome back... your flag, user:
picoCTF{p47ch1ng_l1f3_h4ck_c4a4688b}
```
# bandera
- picoCTF{p47ch1ng_l1f3_h4ck_c4a4688b}