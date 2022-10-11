## where are the robots

# objetivo
- Can you find the robots? `https://jupiter.challenges.picoctf.org/problem/56830/` ([link](https://jupiter.challenges.picoctf.org/problem/56830/)) or http://jupiter.challenges.picoctf.org:56830

# Hints
- What part of the website could tell you where the creator doesn't want you to look?

# solucion
``` bash 
en el link agregamos robots.txt y nos muestra User-agent: *
Disallow: /1bb4c.html
el disallow loagregamos en el link y nos aparece la bandera
https://jupiter.challenges.picoctf.org/problem/56830/1bb4c.html
Guess you found the robots  
picoCTF{ca1cu1at1ng_Mach1n3s_1bb4c}
```
# bandera
- picoCTF{ca1cu1at1ng_Mach1n3s_1bb4c}