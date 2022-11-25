## B1ll_Gat35

# objetivo
- Can you reverse this [Windows Binary](https://jupiter.challenges.picoctf.org/static/0ef5d0d6d552cd5e0bd60c2adbddaa94/win-exec-1.exe)?

# Hints
- Microsoft provides windows virtual machines https://developer.microsoft.com/en-us/windows/downloads/virtual-machines
- Ollydbg may be helpful
- Flag format: PICOCTF{XXXX}

# solucion
``` bash 
─(kali㉿kali)-[~/binary]
└─$ wget https://jupiter.challenges.picoctf.org/static/0ef5d0d6d552cd5e0bd60c2adbddaa94/win-exec-1.exe
--2022-11-25 14:29:10--  https://jupiter.challenges.picoctf.org/static/0ef5d0d6d552cd5e0bd60c2adbddaa94/win-exec-1.exe
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 518656 (506K) [application/octet-stream]
Saving to: ‘win-exec-1.exe’

win-exec-1.exe 100% 506.50K   765KB/s    in 0.7s        

2022-11-25 14:29:11 (765 KB/s) - ‘win-exec-1.exe’ saved [518656/518656]

                                                         
┌──(kali㉿kali)-[~/binary]
└─$ sudo apt install wine  
[sudo] password for kali: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
(kali㉿kali)-[~/binary]
└─$ sudo apt install wine32:i386
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
(kali㉿kali)-[~/binary]
└─$ wine win-exec-1.exe   
wine: created the configuration directory '/home/kali/.wine'
0050:err:ole:StdMarshalImpl_MarshalInterface Failed to create ifstub, hr 0x80004002
0050:err:ole:CoMarshalInterface Failed to marshal the interface {6d5140c1-7436-11ce-8034-00aa006009fa}, hr 0x80004002
0050:err:ole:apartment_get_local_server_stream Failed: 0x80004002
0048:err:ole:StdMarshalImpl_MarshalInterface Failed to create ifstub, hr 0x80004002
0048:err:ole:CoMarshalInterface Failed to marshal the interface {6d5140c1-7436-11ce-8034-00aa006009fa}, hr 0x80004002
0048:err:ole:apartment_get_local_server_stream Failed: 0x80004002
0050:err:ole:start_rpcss Failed to open RpcSs service
wine: configuration in L"/home/kali/.wine" has been updated.
Input a number between 1 and 5 digits: 1
Initializing...
Enter the correct key to get the access codes: 1234
Incorrect key. Try again.
(kali㉿kali)-[~/binary]
└─$ ghidra &          
[1] 71219
                                                         
┌──(kali㉿kali)-[~/binary]
└─$ Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true

se cambio el binario el JNZ y el JNC para que entrara directo al else de la bandera.

(kali㉿kali)-[~/binary]
└─$ ls                                
need-for-speed  win-exec-1.exe
                                                         
┌──(kali㉿kali)-[~/binary]
└─$ ls
need-for-speed  win-exec-1.exe  win-exec-2.exe.bin
                                                         
┌──(kali㉿kali)-[~/binary]
└─$ mv win-exec-2.bin win-exec-2.exe
mv: cannot stat 'win-exec-2.bin': No such file or directory
                                                         
┌──(kali㉿kali)-[~/binary]
└─$ mv win-exec-2.exe.bin win-exec-2.exe
                                                         
┌──(kali㉿kali)-[~/binary]
└─$ wine win-exec-2.exe                 
Input a number between 1 and 5 digits: 1
Initializing...
Enter the correct key to get the access codes: 1234
Correct input. Printing flag: PICOCTF{These are the acces
s codes to the vault: 1063340}
```
# bandera
- PICOCTF{These are the access codes to the vault: 1063340}