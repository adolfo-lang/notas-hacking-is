## Scavenger Hunt

# objetivo
- There is some interesting information hidden around this site [http://mercury.picoctf.net:27278/](http://mercury.picoctf.net:27278/). Can you find it?

# Hints
- You should have enough hints to find the files, don't run a brute forcer.

# solucion
``` bash 
cheque el codigo fuente y en los comentarios encontre partes de la bandera
<!-- Heres the first part of the flag: picoCTF{t -->
/* CSS makes the page look nice, and yes, it also has part of the flag. Heres part 2: h4ts_4_l0 */
para la tercera parte de la bandera utilice robots, y me mostro la tercera parte, tambien decia que la otra parte de la bandera pudiera estar en un servidor apache y con .htacces entramos
User-agent: *
Disallow: /index.html
Part 3: t_0f_pl4c
I think this is an apache server... can you Access the next flag?
view-source:http://mercury.picoctf.net:27278/.htaccess
Part 4: 3s_2_lO0k
I love making websites on my Mac, I can Store a lot of information there.
para la ultima parte, en las Mac existe un archivo .DS_store el cual almacena configuración de una carpeta, donde este el archivo agregue .DS_store al link y muestra la ultima parte de la bandera.
Congrats! You completed the scavenger hunt. Part 5: _a69684fd}
```
# bandera
- picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_a69684fd}