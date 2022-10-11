## logon

# objetivo
- The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/44573/` ([link](https://jupiter.challenges.picoctf.org/problem/44573/)) or http://jupiter.challenges.picoctf.org:44573

# Hints
- Hmm it doesn't seem to check anyone's password, except for Joe's?

# solucion
``` bash 
para este reto te valida cualquier usuario, pero no
te mustra las banderas, entonces checamos las cookies, y modificamos 
la cookie con la que nos logueamos y la ponemos en True y nos muestra la bandera
```
# bandera
- picoCTF{th3_c0nsp1r4cy_l1v3s_0c98aacc}