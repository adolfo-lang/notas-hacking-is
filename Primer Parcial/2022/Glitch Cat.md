## Glitch Cat

# objetivo
- Our flag printing service has started glitching! `$ nc saturn.picoctf.net 65353`

# Hints
- ASCII is one of the most common encodings used in programming
- We know that the glitch output is valid Python, somehow!
- Press Ctrl and c on your keyboard to close your connection and return to the command prompt.

# solucion
``` bash 
(kali㉿kali)-[~/Downloads]
└─$ nc saturn.picoctf.net 65353
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ touch picoflag.py          
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ nano picoflag.py           
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ python picoflag.py                
picoCTF{gl17ch_m3_n07_9c42a45d}
cree un archivo python para que me decodifique 
```
# bandera
- picoCTF{gl17ch_m3_n07_9c42a45d}