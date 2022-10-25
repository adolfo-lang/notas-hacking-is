## what lies within

# objetivo
- There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?

# Hints
- There is data encoded somewhere... there might be an online decoder.

# solucion
``` bash 
(kali㉿kali)-[~/Downloads/img]
└─$ ls
buildings.png
                                                           
┌──(kali㉿kali)-[~/Downloads/img]
└─$ file buildings.png
buildings.png: PNG image data, 657 x 438, 8-bit/color RGBA, non-interlaced
                                                           
┌──(kali㉿kali)-[~/Downloads/img]
└─$ open flag.png
                                                           
┌──(kali㉿kali)-[~/Downloads/img]
└─$ open buildings.png
                                                           
┌──(kali㉿kali)-[~/Downloads/img]
└─$ sudo gem install zsteg                          
[sudo] password for kali: 
Successfully installed zsteg-0.2.11
Parsing documentation for zsteg-0.2.11
Done installing documentation for zsteg after 2 seconds
1 gem installed
                                                           
┌──(kali㉿kali)-[~/Downloads/img]
└─$ zsteg -a buildings.png | grep pico
b1,rgb,lsb,xy       .. text: "picoCTF{h1d1ng_1n_th3_b1t5}"
```
# bandera
- picoCTF{h1d1ng_1n_th3_b1t5}