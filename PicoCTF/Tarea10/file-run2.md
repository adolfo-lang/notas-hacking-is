## file-run2

# objetivo
- Another program, but this time, it seems to want some input. What happens if you try to run it on the command line with input "Hello!"? Download the program [here](https://artifacts.picoctf.net/c/351/run).

# Hints
- Try running it and add the phrase "Hello!" with a space in front (i.e. "./run Hello!")

# solucion
``` bash 
(kali㉿kali)-[~/reversing]
└─$ wget https://artifacts.picoctf.net/c/351/run
--2022-11-23 13:04:09--  https://artifacts.picoctf.net/c/351/run
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 65.9.149.62, 65.9.149.57, 65.9.149.85, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|65.9.149.62|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16816 (16K) [application/octet-stream]
Saving to: ‘run’

run            100%  16.42K  --.-KB/s    in 0.01s       

2022-11-23 13:04:09 (1.29 MB/s) - ‘run’ saved [16816/16816]

                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ ls -la
total 28
drwxr-xr-x  2 kali kali  4096 Nov 23 13:04 .
drwxr-xr-x 42 kali kali  4096 Nov 23 09:49 ..
-rw-r--r--  1 kali kali 16816 Mar 15  2022 run
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ chmod +x run
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ ./run                                       
Run this file with only one argument.
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ ./run Hello!
The flag is: picoCTF{F1r57_4rgum3n7_be0714da}

```
# bandera
- picoCTF{F1r57_4rgum3n7_be0714da}