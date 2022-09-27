## plumbing

# objetivo
- ## 2Warm

# objetivo
- Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 4427`.

# Hints
- Remember the flag format is picoCTF{XXXX}
- What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ nc jupiter.challenges.picoctf.org 4427 | grep pico
picoCTF{digital_plumb3r_5ea1fbd7}

```
# bandera
- picoCTF{digital_plumb3r_5ea1fbd7}

