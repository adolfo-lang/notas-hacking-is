## Safe Opener

# objetivo
- Can you open this safe? I forgot the key to my safe but this [program](https://artifacts.picoctf.net/c/463/SafeOpener.java) is supposed to help me with retrieving the lost key. Can you help me unlock my safe? Put the password you recover into the picoCTF flag format like: `picoCTF{password}`

# Hints
- 

# solucion
``` bash 
kali㉿kali)-[~/reversing]
└─$ wget https://artifacts.picoctf.net/c/463/SafeOpener.java
--2022-11-24 16:05:14--  https://artifacts.picoctf.net/c/463/SafeOpener.java
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.69, 13.249.74.22, 13.249.74.56, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.69|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1258 (1.2K) [application/octet-stream]
Saving to: ‘SafeOpener.java’

SafeOpener.jav 100%   1.23K  --.-KB/s    in 0s          

2022-11-24 16:05:15 (21.6 MB/s) - ‘SafeOpener.java’ saved [1258/1258]

                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ nano SafeOpener.java
public static boolean openSafe(String password) {
        String encodedkey = "cGwzYXMzX2wzdF9tM18xbnQwX3RoM19zYWYz"
(kali㉿kali)-[~/reversing]
└─$ nano SafeOpener.java 
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ echo "cGwzYXMzX2wzdF9tM18xbnQwX3R"| base64 -d
pl3as3_l3t_m3_1nt0_tbase64: invalid input
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ echo cGwzYXMzX2wzdF9tM18xbnQwX3R | base64 -d 
pl3as3_l3t_m3_1nt0_tbase64: invalid input
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ code SafeOpener.java                     
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ echo cGwzYXMzX2wzdF9tM18xbnQwX3RoM19zYWYz | base64 -d
pl3as3_l3t_m3_1nt0_th3_saf3 
```
# bandera
- picoCTF{pl3as3_l3t_m3_1nt0_th3_saf3}