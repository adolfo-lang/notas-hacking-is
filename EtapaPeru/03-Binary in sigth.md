# Binary in sigth

## Objetivo
Can you see the flag in this [BINARY,](https://drive.google.com/file/d/1GN8ajuBVPPxMCWwq7GFDAtzlYADk2ZUr/view?usp=sharing) this [SCRIPT](https://drive.google.com/file/d/1utpRkEmLFhEAZB83XnBXD_ksdhevCrUw/view?usp=sharing) can help

## Solucion
Solo ejecute el archivo sh pasandole el archivo bin y este me regreso 2 archivos. Ya solo los inspeccione con cat y les hice un grep para encontrar la bandera.

```bash
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/Binary in sigth]
└─$ sh help.sh b1n 
Attempting disassembly of b1n ...
Disassembly successful! Available at: b1n.help.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in b1n have been written to b1n.help.strings.txt with file offset

┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/Binary in sigth]
└─$ cat b1n.help.strings.txt | grep Fl
   1020 Fl@g{Mr_Rob0t_3th1c4l_H@ck3R25}
                                                                                
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/Binary in sigth]
└─$ 

```

```bandera
Fl@g{Mr_Rob0t_3th1c4l_H@ck3R25}
```