## Irish-Name-Repo 1

# objetivo
- There is a website running at `https://jupiter.challenges.picoctf.org/problem/39720/` ([link](https://jupiter.challenges.picoctf.org/problem/39720/)) or http://jupiter.challenges.picoctf.org:39720. Do you think you can log us in? Try to see if you can login!

# Hints
- There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?
- Try to think about how the website verifies your login.

# solucion
``` bash 
al tratar de logearnos no podemos, ya que no tenemos un usuario
entonces inspeccionamos la pagina y al cambiar el value a 1, nos damos cuenta que hace una consulta a una base de datos, y hacemos una inyección, concatena el usuario y la contraseña que ingresamos en la consulta, por lo cual en la contraseña introduciomos 'or 1==1 para que y lo concatene en la consulta, nos regrese verdadero y nos muestre la bandera.'

```
# bandera
- picoCTF{s0m3_SQL_c218b685}