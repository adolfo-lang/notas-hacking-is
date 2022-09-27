## runme.py

# code book
- Run the Python script `code.py` in the same directory as `codebook.txt`.

# Hints
- On the webshell, use `ls` to see if both files are in the directory you are in

# solucion
``` bash (kali㉿kali)-[~]
└─(kali㉿kali)-[~]
└─$ cd Downloads  
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ ls -la
total 88828
drwxr-xr-x  3 kali kali     4096 Sep 26 23:41 .
drwxr-xr-x 19 kali kali     4096 Sep 26 23:33 ..
drwxr-xr-x  3 kali kali     4096 Mar 15  2021 Addadshashanammu
-rw-r--r--  1 kali kali     4520 Sep 26 23:24 Addadshashanammu.zip
-rw-r--r--  1 kali kali       27 Sep 26 23:41 codebook.txt
-rw-r--r--  1 kali kali     1278 Sep 26 23:41 code.py
-rw-r--r--  1 kali kali     1189 Sep 24 20:57 convertme.py
-rw-r--r--  1 kali kali    14551 Sep 26 19:31 file
-rw-r--r--  1 kali kali       34 Sep 24 20:28 flag
-rw-r--r--  1 kali kali      785 Sep 26 23:15 ltdis.sh
-rw-------  1 kali kali      777 Sep 26 23:16 nano.19044.save
-rwxr-xr-x  1 kali kali 90088579 Sep 20 00:59 Obsidian-0.15.9.AppImage
-rw-r--r--  1 kali kali      270 Sep 24 20:51 runme.py
-rw-r--r--  1 kali kali     8376 Sep 26 23:18 static
-rw-r--r--  1 kali kali   776032 Sep 26 18:50 strings
-rw-r--r--  1 kali kali    10936 Sep 24 20:37 warm
                                                                             
┌──(kali㉿kali)-[~/Downloads]
└─$ python code.py     
picoCTF{c0d3b00k_455157_d9aa2df2}
```
# bandera
- picoCTF{c0d3b00k_455157_d9aa2df2}