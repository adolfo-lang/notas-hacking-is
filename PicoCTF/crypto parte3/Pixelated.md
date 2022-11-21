## Pixelated

# objetivo
- I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/c9593d1d2ac9d850da95bffe0ac3b6c6/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/c9593d1d2ac9d850da95bffe0ac3b6c6/scrambled2.png)

# Hints
- Think of different ways you can "stack" images

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ cd crypto 
                                                         
┌──(kali㉿kali)-[~/crypto]
└─$ wget https://mercury.picoctf.net/static/c9593d1d2ac9d850da95bffe0ac3b6c6/scrambled1.png
--2022-11-20 21:03:19--  https://mercury.picoctf.net/static/c9593d1d2ac9d850da95bffe0ac3b6c6/scrambled1.png
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 197172 (193K) [application/octet-stream]
Saving to: ‘scrambled1.png’

scrambled1.png 100% 192.55K   364KB/s    in 0.5s        

2022-11-20 21:03:20 (364 KB/s) - ‘scrambled1.png’ saved [197172/197172]

                                                         
┌──(kali㉿kali)-[~/crypto]
└─$ wget https://mercury.picoctf.net/static/c9593d1d2ac9d850da95bffe0ac3b6c6/scrambled2.png
--2022-11-20 21:03:37--  https://mercury.picoctf.net/static/c9593d1d2ac9d850da95bffe0ac3b6c6/scrambled2.png
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 197173 (193K) [application/octet-stream]
Saving to: ‘scrambled2.png’

scrambled2.png 100% 192.55K   323KB/s    in 0.6s        

2022-11-20 21:03:39 (323 KB/s) - ‘scrambled2.png’ saved [197173/197173]

                                                         
┌──(kali㉿kali)-[~/crypto]
└─$ ls
ciphertext  scrambled1.png  scrambled2.png  values
                                                         
┌──(kali㉿kali)-[~/crypto]
└─$ sudo wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar
[sudo] password for kali: 
--2022-11-20 21:06:27--  http://www.caesum.com/handbook/Stegsolve.jar
Resolving www.caesum.com (www.caesum.com)... 216.234.173.1
Connecting to www.caesum.com (www.caesum.com)|216.234.173.1|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 312271 (305K) [application/x-java-archive]
Saving to: ‘stegsolve.jar’

stegsolve.jar  100% 304.95K   128KB/s    in 2.4s        

2022-11-20 21:06:30 (128 KB/s) - ‘stegsolve.jar’ saved [312271/312271]

                                                         
┌──(kali㉿kali)-[~/crypto]
└─$ sudo chmod +x stegsolve.jar 
                                                         
┌──(kali㉿kali)-[~/crypto]
└─$ java -jar stegsolve.jar                      
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
en el add es donde aparece la bandera.
picoCTF{da8fcef8}
```
# bandera
- picoCTF{da8fcef8}