## Obedient Cat

# objetivo
- This file has a flag in plain sight (aka "in-the-clear").

# Hints
- Any hints about entering a command into the Terminal (such as the next one), will start with a '$'... everything after the dollar sign will be typed (or copy and pasted) into your Terminal.
- To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag

# solucion
``` bash wget https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
--2022-09-24 20:32:10--  https://mercury.picoctf.net/static/33996e32dce022205a6a36f69aba56f0/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: ‘flag’

flag                100%[================>]      34  --.-KB/s    in 0s      

2022-09-24 20:32:10 (22.8 MB/s) - ‘flag’ saved [34/34]

                                                                             
┌──(kali㉿kali)-[~]
└─$ cat flag
picoCTF{s4n1ty_v3r1f13d_2aa22101}

# bandera
picoCTF{s4n1ty_v3r1f13d_2aa22101}```
# bandera
- picoCTF{s4n1ty_v3r1f13d_2aa22101}