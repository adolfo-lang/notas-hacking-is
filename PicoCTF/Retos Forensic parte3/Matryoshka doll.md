## Matryoshka doll

# objetivo
- Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one?

# Hints
- Wait, you can hide files inside files? But how do you find them?
- Make sure to submit the flag as picoCTF{XXXXX}

# solucion
``` bash 

(kali㉿kali)-[~]
└─$ mkdir matryoshka
                                                          
┌──(kali㉿kali)-[~]
└─$ cd matryoshka
                                                          
┌──(kali㉿kali)-[~/matryoshka]
└─$ wget https://mercury.picoctf.net/static/f6cc2560a70b1ea811c151accba5390f/dolls.jpg             
--2022-11-01 10:28:16--  https://mercury.picoctf.net/static/f6cc2560a70b1ea811c151accba5390f/dolls.jpg
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 651635 (636K) [application/octet-stream]
Saving to: ‘dolls.jpg’

dolls.jpg      100% 636.36K   235KB/s    in 2.7s         

2022-11-01 10:28:22 (235 KB/s) - ‘dolls.jpg’ saved [651635/651635]

                                                          
┌──(kali㉿kali)-[~/matryoshka]
└─$ exiftool dolls.png   
Error: File not found - dolls.png
                                                          
┌──(kali㉿kali)-[~/matryoshka]
└─$ exiftool dolls.jpg
ExifTool Version Number         : 12.44
File Name                       : dolls.jpg
Directory                       : .
File Size                       : 652 kB
File Modification Date/Time     : 2021:03:15 20:23:04-04:00
File Access Date/Time           : 2022:11:01 10:28:22-04:00
File Inode Change Date/Time     : 2022:11:01 10:28:22-04:00
File Permissions                : -rw-r--r--
File Type                       : PNG
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 594
Image Height                    : 1104
Bit Depth                       : 8
(kali㉿kali)-[~/matryoshka]
└─$ strings dolls.jpg                
IHDR
eiCCPICC Profile
 *!     $
(VtUD
@Z(O
eMHKg
aPn;
b1d#9t
}>?g
 _98
2\-h
r.G;
IJ,d]
},#[
`,BQX
X@      k
I5O7
Nh?B

(kali㉿kali)-[~/matryoshka]
└─$ binwalk dolls.jpg  

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378955, uncompressed size: 383936, name: base_images/2_c.jpg
651613        0x9F15D         End of Zip archive, footer length: 22

                                                           
┌──(kali㉿kali)-[~/matryoshka]
└─$ binwalk -e dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378955, uncompressed size: 383936, name: base_images/2_c.jpg
651613        0x9F15D         End of Zip archive, footer length: 22

                                                              
┌──(kali㉿kali)-[~/matryoshka]
└─$ ls
dolls.jpg  _dolls.jpg.extracted
                                                              
┌──(kali㉿kali)-[~/matryoshka]
└─$ cd _dolls.jpg.extracted 
                                                              
┌──(kali㉿kali)-[~/matryoshka/_dolls.jpg.extracted]
└─$ ls
4286C.zip  base_images
                                                              
┌──(kali㉿kali)-[~/matryoshka/_dolls.jpg.extracted]
└─$ cd base_images         
                                                              
┌──(kali㉿kali)-[~/matryoshka/_dolls.jpg.extracted/base_images]                                                             
└─$ ls
2_c.jpg
                                                              
┌──(kali㉿kali)-[~/matryoshka/_dolls.jpg.extracted/base_images]                                                             
└─$ open 2_c.jpg   
                                                              
┌──(kali㉿kali)-[~/matryoshka/_dolls.jpg.extracted/base_images]                                                             
└─$ binwalk -e 2_c.jpg   

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196041, uncompressed size: 201443, name: base_images/3_c.jpg
383803        0x5DB3B         End of Zip archive, footer length: 22
383914        0x5DBAA         End of Zip archive, footer length: 22

                                                              
┌──(kali㉿kali)-[~/matryoshka/_dolls.jpg.extracted/base_images]                                                             
└─$ ls
2_c.jpg  _2_c.jpg.extracted
                                                              
┌──(kali㉿kali)-[~/matryoshka/_dolls.jpg.extracted/base_images]                                                             
└─$ cd _2_c.jpg.extracted  
                                                              
┌──(kali㉿kali)-[~/matryoshka/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└─$ ls
2DD3B.zip  base_images
                                                              
┌──(kali㉿kali)-[~/matryoshka/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted]
└─$ cd base_images       
                                                              
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ ls
3_c.jpg
                                                              
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ open 3_c.jpg         
                                                              
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ binwalk -e 3_c.jpg   

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77649, uncompressed size: 79806, name: base_images/4_c.jpg
201421        0x312CD         End of Zip archive, footer length: 22

                                                              
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ ls
3_c.jpg  _3_c.jpg.extracted
                                                              
┌──(kali㉿kali)-[~/…/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images]
└─$ cd _3_c.jpg.extracted
                                                              
┌──(kali㉿kali)-[~/…/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted]
└─$ ls                     
1E2D6.zip  base_images
                                                              
┌──(kali㉿kali)-[~/…/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted]
└─$ cd base_images       
                                                              
┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ ls 
4_c.jpg
                                                              
┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ open 4_c.jpg                   
                                                              
┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ binwalk -e 4_c.jpg   

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 62, uncompressed size: 81, name: flag.txt
79784         0x137A8         End of Zip archive, footer length: 22

                                                              
┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ ls                
4_c.jpg  _4_c.jpg.extracted
                                                              
┌──(kali㉿kali)-[~/…/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images]
└─$ cd _4_c.jpg.extracted 
                                                              
┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ ls
136DA.zip  flag.txt
                                                              
┌──(kali㉿kali)-[~/…/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted]
└─$ cat flag.txt                      
picoCTF{ac0072c423ee13bfc0b166af72e25b61} 
```
# bandera
- picoCTF{ac0072c423ee13bfc0b166af72e25b61}