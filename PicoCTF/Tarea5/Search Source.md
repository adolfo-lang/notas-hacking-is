## search source

# objetivo
- The developer of this website mistakenly left an important artifact in the website source, can you find it? The website is [here](http://saturn.picoctf.net:58133/)

# Hints
- How could you mirror the website on your local machine so you could use more powerful tools for searching?

# solucion
``` bash 
inspeccione el codigo fuente de la pagina y encontré la bandera en uno de los archivos .css, en el archivo style.css
 /** banner_main picoCTF{1nsp3ti0n_0f_w3bpag3s_587d12b8} **/
```
# bandera
- picoCTF{1nsp3ti0n_0f_w3bpag3s_587d12b8}