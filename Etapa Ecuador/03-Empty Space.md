# Empty Space

## Objetivo
Can you find the hidden message?

## Solucion
Ejecutamos el comando xxd en el archivo, ahi vemos que tiene 3 diferentes tipos de espacios el 20, 09 y 0d0a.
```bash
┌──(kali㉿kali)-[~/Desktop/Etapa Ecuador/archivos/Empty Space]
└─$ xxd space_encoded.txt 
00000000: 2020 2020 2020 2009 0d0a 2009 0920 2009         ... ..  .
00000010: 0920 0d0a 2009 0920 0909 2020 0d0a 2009  . .. .. ..  .. .
00000020: 0920 2020 2009 0d0a 2009 0920 2009 0909  .    ... ..  ...
00000030: 0d0a 2009 0909 0920 0909 0d0a 2009 2020  .. .... .... .  
00000040: 2009 2009 0d0a 2009 2009 2020 0909 0d0a   . ... . .  ....
00000050: 2009 2009 2020 2020 0d0a 2009 2020 2020   . .    .. .    
00000060: 2009 0d0a 2009 2020 2020 0909 0d0a 2009   ... .    .... .
00000070: 2020 0920 2009 0d0a 2009 2020 0909 0909    .  ... .  ....
00000080: 0d0a 2009 2009 0909 0909 0d0a 2009 2020  .. . ....... .  
00000090: 2009 2009 0d0a 2009 2009 0920 2020 0d0a   . ... . ..   ..
000000a0: 2009 2009 2009 2020 0d0a 2009 2020 2009   . . .  .. .   .
000000b0: 2009 0d0a 2009 2009 2020 0920 0d0a 2009   ... . .  . .. .
000000c0: 2020 0920 2009 0d0a 2009 2020 0909 0909    .  ... .  ....
000000d0: 0d0a 2009 2009 2020 0920 0d0a 2009 0909  .. . .  . .. ...
000000e0: 0909 2009 0d0a                           .. ...

```

Usamos un exploid en python para cambiar los 20 por 0 y los 09 por 1, depues eliminamos los 0d0a y obtenemos la bandera con un decode de binarios.
```bash
┌──(kali㉿kali)-[~/Desktop/Etapa Ecuador/archivos/Empty Space]
└─$ python3 exp.py       
bytearray(b'0000000101100110011011000110000101100111011110110100010101010011010100000100000101000011010010010100111101011111010001010101100001010100010001010101001001001001010011110101001001111101')
                                                                                
┌──(kali㉿kali)-[~/Desktop/Etapa Ecuador/archivos/Empty Space]
└─$ nano exp.py          
                                                                                    
┌──(kali㉿kali)-[~/Desktop/Etapa Ecuador/archivos/Empty Space]
└─$ python3 exp.py 
b'\x01flag{ESPACIO_EXTERIOR}'
                                                                                
```