## Secrets

# objetivo
- We have several pages hidden. Can you find the one with the flag? The website is running [here](http://saturn.picoctf.net:61481/).


# Hints
- folders folders folders

# solucion
``` bash 
en este reto la banera estaba oculta en superi hidden, tuve que estar modificando la ruta hasta encontrar la bandera
view-source:http://saturn.picoctf.net:61481/secret/hidden/superhidden/
<html>
  <head>
    <title></title>
    <link rel="stylesheet" href="[mycss.css](view-source:http://saturn.picoctf.net:61481/secret/hidden/superhidden/mycss.css)" />
  </head>

  <body>
    <h1>Finally. You found me. But can you see me</h1>
    <h3 class="flag">picoCTF{succ3ss_@h3n1c@10n_39849bcf}</h3>
  </body>
</html>
```
# bandera
- picoCTF{succ3ss_@h3n1c@10n_39849bcf}