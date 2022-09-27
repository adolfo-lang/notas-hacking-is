## pw crack1

# objetivo
- Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/53/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/53/level1.flag.txt.enc) in the same directory too.

# Hints
-To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.

# solucion
``` bash 
(kali㉿kali)-[~/Downloads]
└─$ nano level1.py   
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ python level1.py
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
```
# bandera
- picoCTF{545h_r1ng1ng_1b2fd683}