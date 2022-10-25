## shark on wire 1

# objetivo
- We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.

# Hints
- Try using a tool like Wireshark
- What are streams?

# solucion
``` bash 
(kali㉿kali)-[~/Downloads]
└─$ file capture.pcap
capture.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)

hacemos uso de la herremienta wireshark para ver la captura de paquetes que se hizo. seguimos los de protocolo udp, y vamos busscando hasta encontrar la bandera, ya que son varios paquetes.
picoCTF{StaT31355_636f6e6e}

```
# bandera
- picoCTF{StaT31355_636f6e6e}