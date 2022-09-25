## Wave a flag

# objetivo
- This file has a flag in plain sight (aka "in-the-clear").

# Hints
- This program will only work in the webshell or another Linux computer.
- To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm

# solucion
``` bash
wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm
--2022-09-24 20:40:29--  https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: ‘warm’

warm                100%[================>]  10.68K  --.-KB/s    in 0s      

2022-09-24 20:40:30 (67.2 MB/s) - ‘warm’ saved [10936/10936]
┌──(kali㉿kali)-[~]
└─$ ./warm
zsh: permission denied: ./warm
(kali㉿kali)-[~]
└─$ ./warm        
Hello user! Pass me a -h to learn what I can do!
                                                                             
┌──(kali㉿kali)-[~]
└─$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_30e77291}
```

# bandera
- picoCTF{b1scu1ts_4nd_gr4vy_30e77291}