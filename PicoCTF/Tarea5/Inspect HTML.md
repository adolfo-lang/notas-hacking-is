## Inspect HTML

# objetivo
- Can you get the flag? Go to this [website](http://saturn.picoctf.net:50920/) and see what you can discover.

# Hints
- How is the password checked on this website?

# solucion
``` bash 
inspeccionando el codigo fuente encontramos el archivo secure.js, en 
el cual esta el usuario y contraseña para logearnos, y al logearnos encontramos la bandera.
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```
# bandera
- picoCTF{j5_15_7r4n5p4r3n7_a8788e61}