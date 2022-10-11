## Irish-Name-Repo 3

# objetivo
- There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/29132/` ([link](https://jupiter.challenges.picoctf.org/problem/29132/)) or http://jupiter.challenges.picoctf.org:29132. Try to see if you can login as admin!

# Hints
- Seems like the password is encrypted.

# solucion
``` bash 
en este reto solo hace la consulta con el pasword, pero lo complejo
es que lo encripta, esta en root 13.
lo quisimos hacer fue que en la consulta fuera or 1==1,
pero con el rot 13 cambiaba y en la consulta con nel select concatenaba be 1=1;.
entonces lo que hicimos fue poner como lo insertaba con rot 13, para que al concatenarlo en la consulta lo concatenara de manera correcta 
(or 1=1;);
lo que ensertamos en la contraseña fue 'be 1=!;
Logged in!

Your flag is: picoCTF{3v3n_m0r3_SQL_06a9db19}
```
# bandera
- picoCTF{3v3n_m0r3_SQL_06a9db19}