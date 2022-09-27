## Wave a flag

# objetivo
- There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 35652`, but it doesn't speak English...

# Hints
- This program will only work in the webshell or another Linux computer.
- To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm

# solucion
``` bash
(kali㉿kali)-[~]
└─$ nc mercury.picoctf.net 35652
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
57 
98 
51 
98 
55 
51 
57 
50 
125 
10
https://onlineasciitools.com/convert-decimal-to-ascii
picoCTF{g00d_k1tty!_n1c3_k1tty!_9b3b7392}
```

# bandera
- picoCTF{g00d_k1tty!_n1c3_k1tty!_9b3b7392}