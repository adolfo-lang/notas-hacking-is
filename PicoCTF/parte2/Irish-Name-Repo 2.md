## Irish-Name-Repo 2

# objetivo
- There is a website running at `https://jupiter.challenges.picoctf.org/problem/52849/` ([link](https://jupiter.challenges.picoctf.org/problem/52849/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:52849

# Hints
- The password is being filtered.

# solucion
``` bash 
para este reto volvimos a cambiar a uno el value, para que nos muestre la consulta, pero ya nos detecta la inyeccion que hicimos anteriormente
y ahora para entrar de nuevo omitimos la parte de pasword y solo usar el usuario en la consulta, por lo cual despues del usuario pusimos ; para hacer la consulta solo con el usuario admin';
```
# bandera
- picoCTF{m0R3_SQL_plz_fa983901}