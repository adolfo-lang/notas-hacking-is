## pw crack2

# objetivo
- Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/16/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level2.flag.txt.enc) in the same directory too.

# Hints
- Does that encoding look familiar?
- The `str_xor` function does not need to be reverse engineered for this challenge.

# solucion
``` bash 
(kali㉿kali)-[~/Downloads]
└─$ nano level2.py
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ python          
Python 3.10.7 (main, Sep  8 2022, 14:34:29) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36)
'de76'
>>> 
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ python level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
```
# bandera
- picoCTF{tr45h_51ng1ng_489dea9a}