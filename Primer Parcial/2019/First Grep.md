## First Grep

# objetivo
- Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file)? This would be really tedious to look through manually, something tells me there is a better way.

# Hints
- grep [tutorial](https://ryanstutorials.net/linuxtutorial/grep.php)

# solucion
``` bash 
kali㉿kali)-[~]
└─$ cd Downloads
(kali㉿kali)-[~/Downloads]
└─$ cat file | grep pico
picoCTF{grep_is_good_to_find_things_5af9d829}
```
# bandera
- picoCTF{grep_is_good_to_find_things_5af9d829}