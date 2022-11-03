## Redaction gone wrong

# objetivo
- Now you DON’T see me. This [report](https://artifacts.picoctf.net/c/264/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?

# Hints
- How can you be sure of the redaction?

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ mkdir redaction
                                                            
┌──(kali㉿kali)-[~]
└─$ cd redaction 
                                                            
┌──(kali㉿kali)-[~/redaction]
└─$ wget https://artifacts.picoctf.net/c/264/Financial_Report_for_ABC_Labs.pdf
--2022-11-03 11:37:19--  https://artifacts.picoctf.net/c/264/Financial_Report_for_ABC_Labs.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.22, 13.249.74.17, 13.249.74.69, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34915 (34K) [application/octet-stream]
Saving to: ‘Financial_Report_for_ABC_Labs.pdf’

Financial_Repo 100%[====>]  34.10K  --.-KB/s    in 0.01s   

2022-11-03 11:37:19 (2.47 MB/s) - ‘Financial_Report_for_ABC_Labs.pdf’ saved [34915/34915]
(kali㉿kali)-[~]
└─$ mkdir redaction
                                                            
┌──(kali㉿kali)-[~]
└─$ cd redaction 
                                                            
┌──(kali㉿kali)-[~/redaction]
└─$ wget https://artifacts.picoctf.net/c/264/Financial_Report_for_ABC_Labs.pdf
--2022-11-03 11:37:19--  https://artifacts.picoctf.net/c/264/Financial_Report_for_ABC_Labs.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.22, 13.249.74.17, 13.249.74.69, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34915 (34K) [application/octet-stream]
Saving to: ‘Financial_Report_for_ABC_Labs.pdf’

Financial_Repo 100%[====>]  34.10K  --.-KB/s    in 0.01s   

2022-11-03 11:37:19 (2.47 MB/s) - ‘Financial_Report_for_ABC_Labs.pdf’ saved [34915/34915]
(kali㉿kali)-[~]
└─$ mkdir redaction
                                                            
┌──(kali㉿kali)-[~]
└─$ cd redaction 
                                                            
┌──(kali㉿kali)-[~/redaction]
└─$ wget https://artifacts.picoctf.net/c/264/Financial_Report_for_ABC_Labs.pdf
--2022-11-03 11:37:19--  https://artifacts.picoctf.net/c/264/Financial_Report_for_ABC_Labs.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.22, 13.249.74.17, 13.249.74.69, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34915 (34K) [application/octet-stream]
Saving to: ‘Financial_Report_for_ABC_Labs.pdf’

Financial_Repo 100%[====>]  34.10K  --.-KB/s    in 0.01s   

2022-11-03 11:37:19 (2.47 MB/s) - ‘Financial_Report_for_ABC_Labs.pdf’ saved [34915/34915]
(kali㉿kali)-[~]
└─$ mkdir redaction
                                                            
┌──(kali㉿kali)-[~]
└─$ cd redaction 
                                                            
┌──(kali㉿kali)-[~/redaction]
└─$ wget https://artifacts.picoctf.net/c/264/Financial_Report_for_ABC_Labs.pdf
--2022-11-03 11:37:19--  https://artifacts.picoctf.net/c/264/Financial_Report_for_ABC_Labs.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.22, 13.249.74.17, 13.249.74.69, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34915 (34K) [application/octet-stream]
Saving to: ‘Financial_Report_for_ABC_Labs.pdf’

Financial_Repo 100%[====>]  34.10K  --.-KB/s    in 0.01s   

2022-11-03 11:37:19 (2.47 MB/s) - ‘Financial_Report_for_ABC_Labs.pdf’ saved [34915/34915]
(kali㉿kali)-[~]
└─$ mkdir redaction
                                                            
┌──(kali㉿kali)-[~]
└─$ cd redaction 
                                                            
┌──(kali㉿kali)-[~/redaction]
└─$ wget https://artifacts.picoctf.net/c/264/Financial_Report_for_ABC_Labs.pdf
--2022-11-03 11:37:19--  https://artifacts.picoctf.net/c/264/Financial_Report_for_ABC_Labs.pdf
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 13.249.74.22, 13.249.74.17, 13.249.74.69, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|13.249.74.22|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34915 (34K) [application/octet-stream]
Saving to: ‘Financial_Report_for_ABC_Labs.pdf’

Financial_Repo 100%[====>]  34.10K  --.-KB/s    in 0.01s   

2022-11-03 11:37:19 (2.47 MB/s) - ‘Financial_Report_for_ABC_Labs.pdf’ saved [34915/34915]
es un archivo pdf y la bandera esta subrrayada con negro solo seleccione y la muestra 
picoCTF{C4n_Y0u_S33_m3_fully}
```
# bandera
- picoCTF{C4n_Y0u_S33_m3_fully}