## Bases

# objetivo
- What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.

# Hints
- Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ echo "bDNhcm5fdGgzX3IwcDM1" |base64 -d -
l3arn_th3_r0p35
```
# bandera
- picoCTF{l3arn_th3_r0p35}