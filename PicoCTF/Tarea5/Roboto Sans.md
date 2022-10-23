## roboto sans

# objetivo
- The flag is somewhere on this web application not necessarily on the website. Find it. Check [this](http://saturn.picoctf.net:65352/) out.

# Hints
- 

# solucion
``` bash 
para este reto usabos robots agregamos a la ruta /robots.txt y nos regresa el resto cifrado en base 64
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/

kali㉿kali)-[~]
└─$ echo anMvbXlmaWxlLnR4dA== | base64 -d 
js/myfile.txt 
y lo agregamos a la ruta
picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}
```
# bandera
- picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}