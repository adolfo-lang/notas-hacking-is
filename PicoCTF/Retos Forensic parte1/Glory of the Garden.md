## Glory of the Garden

# objetivo
- This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.

# Hints
- What is a hex editor?

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ cd Downloads
                                                          
┌──(kali㉿kali)-[~/Downloads]
└─$ ls                            
edenmine.txt  Obsidian-0.15.9.AppImage
garden.jpg    Pablito_Visits_Hubiku.png
KUKULKAN.jpg
                                                          
┌──(kali㉿kali)-[~/Downloads]
└─$ strings garden.png            
strings: 'garden.png': No such file
                                                          
┌──(kali㉿kali)-[~/Downloads]
└─$ strings garden.jpg | grep pico
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"

```
# bandera
- picoCTF{more_than_m33ts_the_3y33dd2eEF5}