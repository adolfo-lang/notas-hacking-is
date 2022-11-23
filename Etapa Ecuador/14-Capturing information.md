# Capturing information
Juan our SPY, managed to get information from the criminal's computer. Juan reports that he tries to get away. Help us to discover where thinks intend to escape.

flag{DESTINY}
 
## Objetivo


## Solucion
```bash
┌──(kali㉿kali)-[/media/…/Meta/Etapa Ecuador/archivos/Drain]
└─$ tshark -r captura.pcapng -T fields -e usbhid.data -Y 'usbhid.data && usb.data_len==8 && usbhid.data!= 0000000000000000'|sed 's/.\{2\}/&:/g' > x
                                                                                                                                                            
┌──(kali㉿kali)-[/media/…/Meta/Etapa Ecuador/archivos/Drain]
└─$ ls                                                  
Cache3.txt  captura.pcapng  ganador.jpg  image2.png  oSINoSINT.jpeg  perro.jpg  x  you.png

```

```bandera
flag{PARIS}
```