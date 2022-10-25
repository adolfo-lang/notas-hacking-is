## extensions

# objetivo
- This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
# Hints
- How do operating systems know what kind of file it is? (It's not just the ending!
- Make sure to submit the flag as picoCTF{XXXXX}

# solucion
``` bash 
(kali㉿kali)-[~/Downloads]
└─$ mkdir ext 
                                                           
┌──(kali㉿kali)-[~/Downloads]
└─$ cd ext      
                                                           
┌──(kali㉿kali)-[~/Downloads/ext]
└─$ wget https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt
--2022-10-25 11:40:18--  https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9984 (9.8K) [application/octet-stream]
Saving to: ‘flag.txt’

flag.txt       100%   9.75K  --.-KB/s    in 0s            

2022-10-25 11:40:19 (63.4 MB/s) - ‘flag.txt’ saved [9984/9984]

                                                           
┌──(kali㉿kali)-[~/Downloads/ext]
└─$ ls
flag.txt
                                                           
┌──(kali㉿kali)-[~/Downloads/ext]
└─$ file flag.txt    
flag.txt: PNG image data, 1697 x 608, 8-bit/color RGB, non-interlaced
                                                           
┌──(kali㉿kali)-[~/Downloads/ext]
└─$ mv flag.txt flag.png
                                                           
┌──(kali㉿kali)-[~/Downloads/ext]
└─$ open flag.png


```
# bandera
- picoCTF{now_you_know_about_extensions}