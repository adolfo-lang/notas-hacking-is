## reverse_cipher

# objetivo
- We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this). Can you reverse the flag.

# Hints
- objdump and Gihdra are some tools that could assist with this

# solucion
``` bash 
(kali㉿kali)-[~/binary]
└─$ wget https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev
--2022-11-25 12:39:02--  https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16856 (16K) [application/octet-stream]
Saving to: ‘rev’

rev            100%  16.46K  --.-KB/s    in 0s          

2022-11-25 12:39:02 (102 MB/s) - ‘rev’ saved [16856/16856]

                                                         
┌──(kali㉿kali)-[~/binary]
└─$ wget https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this
--2022-11-25 12:39:17--  https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
(kali㉿kali)-[~/binary]
└─$ ghidra & 
[1] 26771
                                                         
┌──(kali㉿kali)-[~/binary]
└─$ Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true

[1]  + done       ghidra
(kali㉿kali)-[~/binary]
└─$ nano scpt.py

cifrado = open('rev_this','r').read()
print(cifrado)

flag = ""

for i in range(8, len(cifrado)-1):
    if i & 1 == 0:
        flag += chr(ord(cifrado[i])-5)
    else:
        flag += chr(ord(cifrado[i])+2)

print(flag)

(kali㉿kali)-[~/binary]
└─$ python3 scpt.py
picoCTF{w1{1wq8/7376j.:}
r3v3rs312528e05

```
# bandera
- picoCTF{r3v3rs312528e05}