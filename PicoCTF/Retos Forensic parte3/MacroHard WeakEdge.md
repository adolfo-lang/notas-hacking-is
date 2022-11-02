## MacroHard WeakEdge

# objetivo
- I've hidden a flag in this file. Can you find it?

# Hints
- 

# solucion
``` bash 
(kali㉿kali)-[~]
└─$ mkdir macrohard                   
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ cd macrohard 
                                                                                                                                                                      
┌──(kali㉿kali)-[~/macrohard]
└─$ wget https://mercury.picoctf.net/static/52da699e0f203321c7c90ab56ea912d8/Forensics%20is%20fun.pptm
--2022-11-01 11:10:48--  https://mercury.picoctf.net/static/52da699e0f203321c7c90ab56ea912d8/Forensics%20is%20fun.pptm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 100093 (98K) [application/octet-stream]
Saving to: ‘Forensics is fun.pptm’

Forensics is fun.pptm                     100%[===================================================================================>]  97.75K  --.-KB/s    in 0.09s   

2022-11-01 11:10:51 (1.02 MB/s) - ‘Forensics is fun.pptm’ saved [100093/100093]

                                                                                                                                                                      
┌──(kali㉿kali)-[~/macrohard]
└─$ file Forensics\ is\ fun.pptm 
Forensics is fun.pptm: Microsoft PowerPoint 2007+
                                                                                                                                                                      
┌──(kali㉿kali)-[~/macrohard]
└─$ ls -la
total 108
drwxr-xr-x  2 kali kali   4096 Nov  1 11:10  .
drwxr-xr-x 24 kali kali   4096 Nov  1 11:10  ..
-rw-r--r--  1 kali kali 100093 Mar 23  2021 'Forensics is fun.pptm'
                                                                                                                                                                      
┌──(kali㉿kali)-[~/macrohard]
└─$ unzip Forensics\ is\ fun.pptm 
Archive:  Forensics is fun.pptm
  inflating: [Content_Types].xml     
  inflating: _rels/.rels             
  inflating: ppt/presentation.xml    
  inflating: ppt/slides/_rels/slide46.xml.rels  
  inflating: ppt/slides/slide1.xml   
  inflating: ppt/slides/slide2.xml   
  inflating: ppt/slides/slide3.xml   
  inflating: ppt/slides/slide4.xml   
  inflating: ppt/slides/slide5.xml   
  inflating: ppt/slides/slide6.xml   
  inflating: ppt/slides/slide7.xml   
   extracting: docProps/thumbnail.jpeg  
  inflating: ppt/vbaProject.bin      
  inflating: ppt/presProps.xml       
  inflating: ppt/viewProps.xml       
  inflating: ppt/tableStyles.xml     
  inflating: docProps/core.xml       
  inflating: docProps/app.xml        
  inflating: ppt/slideMasters/hidden  
                                                                                                                                                                      
┌──(kali㉿kali)-[~/macrohard]
└─$ ls -la
total 132
drwxr-xr-x  5 kali kali   4096 Nov  1 11:12  .
drwxr-xr-x 24 kali kali   4096 Nov  1 11:10  ..
-rw-r--r--  1 kali kali  10660 Jan  1  1980 '[Content_Types].xml'
drwxr-xr-x  2 kali kali   4096 Nov  1 11:12  docProps
-rw-r--r--  1 kali kali 100093 Mar 23  2021 'Forensics is fun.pptm'
drwxr-xr-x  7 kali kali   4096 Nov  1 11:12  ppt
drwxr-xr-x  2 kali kali   4096 Nov  1 11:12  _rels
                                                                                                                                                                      
┌──(kali㉿kali)-[~/macrohard]
└─$ cd ..                        
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ cd Downloads
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads]
└─$ ls    
buildings.png  code_1.72.2-1665614327_amd64.deb  exp.py    garden.jpg    moon                      Pablito_Visits_Hubiku.png  whitepages.txt
capture.pcap   edenmine.txt                      flag.txt  KUKULKAN.jpg  Obsidian-0.15.9.AppImage  pico_img.png
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads]
└─$ sudo dpkg -i code_1.72.2-1665614327_amd64.deb 
[sudo] password for kali: 
Selecting previously unselected package code.
(Reading database ... 352270 files and directories currently installed.)
Preparing to unpack code_1.72.2-1665614327_amd64.deb ...
Unpacking code (1.72.2-1665614327) ...
Setting up code (1.72.2-1665614327) ...
Processing triggers for desktop-file-utils (0.26-1) ...
Processing triggers for mailcap (3.70+nmu1) ...
Processing triggers for shared-mime-info (2.2-1) ...
                                                                                                                                                                      
┌──(kali㉿kali)-[~/Downloads]
└─$ cd ..       
                                                                                                                                                                      
┌──(kali㉿kali)-[~]
└─$ cd macrohard
                                                                                                                                                                      
┌──(kali㉿kali)-[~/macrohard]
└─$ code .      
                                                                                                                                                                      
┌──(kali㉿kali)-[~/macrohard]
└─$ echo "Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q" | tr -d " " | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input

```
# bandera
- flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}