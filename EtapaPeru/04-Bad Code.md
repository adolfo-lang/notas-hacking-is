# Bad Code

## Objetivo
help us review this code in this [file](https://drive.google.com/file/d/1gLEsMvKICvOyu1DsnKGLiKWujdbgYeIz/view?usp=sharing)

## Solucion
Inspeccione el codigo y lo hiba ejecutando para corregir los errores que tenia, los cuales eran problema de identacion y que habia una coma de mas.

```bash
                                                                                                                                                                      
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/Bad code]
└─$ python3 badcode.py 
  File "/home/kali/Desktop/Seguridad en Redes/seguridad-en-redes/Notas_hacking_IS/Meta/Etapa Peru/archivos/Bad code/badcode.py", line 13
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
                                                                                                         ^
IndentationError: unindent does not match any outer indentation level
                                                                                                                                                                      
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/Bad code]
└─$ 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/Bad code]
└─$ python3 badcode.py
  File "/home/kali/Desktop/Seguridad en Redes/seguridad-en-redes/Notas_hacking_IS/Meta/Etapa Peru/archivos/Bad code/badcode.py", line 13
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
TabError: inconsistent use of tabs and spaces in indentation
                                                                                                                                                                      
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/Bad code]
└─$ python3 badcode.py
  File "/home/kali/Desktop/Seguridad en Redes/seguridad-en-redes/Notas_hacking_IS/Meta/Etapa Peru/archivos/Bad code/badcode.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
                                                                                                                                                                      
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/Bad code]
└─$ python3 badcode.py
  File "/home/kali/Desktop/Seguridad en Redes/seguridad-en-redes/Notas_hacking_IS/Meta/Etapa Peru/archivos/Bad code/badcode.py", line 13
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
SyntaxError: 'return' outside function
                                                                                                                                                                      
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/Bad code]
└─$ python3 badcode.py
Traceback (most recent call last):
  File "/home/kali/Desktop/Seguridad en Redes/seguridad-en-redes/Notas_hacking_IS/Meta/Etapa Peru/archivos/Bad code/badcode.py", line 19, in <module>
    flag = str_xor(flag_enc, 'enkidu')
  File "/home/kali/Desktop/Seguridad en Redes/seguridad-en-redes/Notas_hacking_IS/Meta/Etapa Peru/archivos/Bad code/badcode.py", line 13, in str_xor
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
  File "/home/kali/Desktop/Seguridad en Redes/seguridad-en-redes/Notas_hacking_IS/Meta/Etapa Peru/archivos/Bad code/badcode.py", line 13, in <listcomp>
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
TypeError: ord() expected a character, but string of length 16 found
                                                                                                                                                                      
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/Bad code]
└─$ python3 badcode.py
That is correct! Here's your flag: dOcpE$9.QM9TEiam
                                                                                                                                                                      
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/Bad code]
└─$ 

```

```bandera
dOcpE$9.QM9TEiam
```
