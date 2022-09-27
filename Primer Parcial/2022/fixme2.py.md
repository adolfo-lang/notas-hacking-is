## fixme2.py

# objetivo
- Fix the syntax error in the Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/66/fixme2.py)

# Hints
- To view the file in the webshell, do: `$ nano fixme2.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.

# solucion
``` bash 
(kali㉿kali)-[~/Downloads]
└─$ python fixme2.py
  File "/home/kali/Downloads/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ nano fixme2.py  
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ python fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
se corrigio el if
```
# bandera
- picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}