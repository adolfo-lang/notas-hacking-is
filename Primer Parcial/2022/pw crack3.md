## pw crack3

# objetivo
- Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/25/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/25/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/25/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

# Hints
- To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`
- To exit `bvi` type `:q` and press enter.
- The `str_xor` function does not need to be reverse engineered for this challenge.

# solucion
``` bash 
"8799", "d3ab", "1ea2", "acaf", "2295", "a9de", "6f3d"
(kali㉿kali)-[~/Downloads]
└─$ nano level3.py
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads]
└─$ python level3.py
Please enter correct password for flag: 8799
That password is incorrect
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads]
└─$ python level3.py
Please enter correct password for flag: d3ab
That password is incorrect
                                                                                                                                                                       
┌──(kali㉿kali)-[~/Downloads]
└─$ python level3.py 
Please enter correct password for flag: 1ea2
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
```
# bandera
- picoCTF{m45h_fl1ng1ng_6f98a49f}
