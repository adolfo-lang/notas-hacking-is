## file-run1

# objetivo
- A program has been provided to you, what happens if you try to run it on the command line? Download the program [here](https://artifacts.picoctf.net/c/308/run).

# Hints
- To run the program at all, you must make it executable (i.e. `$ chmod +x run`)
- Try running it by adding a '.' in front of the path to the file (i.e. `$ ./run`)

# solucion
``` bash 
(kali㉿kali)-[~/reversing]
└─$ file run       
run: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=d21045f436f558afb1bd44f95c663de57f1c8926, for GNU/Linux 3.2.0, not stripped
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ chmod +x run      
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ ls -la           
total 28
drwxr-xr-x  2 kali kali  4096 Nov 23 09:50 .
drwxr-xr-x 42 kali kali  4096 Nov 23 09:49 ..
-rwxr-xr-x  1 kali kali 16736 Mar 15  2022 run
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ .\ŗun    
.ŗun: command not found
                                                         
┌──(kali㉿kali)-[~/reversing]
└─$ ./run    
The flag is: picoCTF{U51N6_Y0Ur_F1r57_F113_9bc52b6b}

```
# bandera
- picoCTF{U51N6_Y0Ur_F1r57_F113_9bc52b6b}