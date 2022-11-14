# Find a Flag

## Objetivo
Unzip this [archive](https://drive.google.com/file/d/15pFs7BTOuJ4jrHZOAHNXfPWunY0K9fGl/view?usp=sharing) and find the file named 'oliver_twist.txt'

## Solucion
Para resolver este reto primero me puse a ver los archivos que habia en cada carpeta, al ver que no estaba me puse a listar los archivos pero tambien los que estaban ocultos, y es en una carpeta oculta donde se encontraba la bandera.
```bash
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/great_author]
└─$ ls    
13771.txt.utf-8  14789.txt.utf-8  acceptable_books  adequate_books  satisfactory_books
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/great_author]
└─$ ls -la
total 1944
drwxr-xr-x 5 kali kali    4096 Oct  5 23:03 .
drwxr-xr-x 3 kali kali    4096 Nov  7 12:42 ..
-rw-r--r-- 1 kali kali 1003806 May  6  2022 13771.txt.utf-8
-rw-r--r-- 1 kali kali  960595 May  7  2022 14789.txt.utf-8
drwxr-xr-x 3 kali kali    4096 May 13 16:10 acceptable_books
drwxr-xr-x 3 kali kali    4096 Oct  5 23:03 adequate_books
drwxr-xr-x 3 kali kali    4096 May 13 16:19 satisfactory_books
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/great_author]
└─$ 
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/great_author]
└─$ cd acceptable_books 
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/Etapa Peru/archivos/great_author/acceptable_books]
└─$ ls -la
total 1780
drwxr-xr-x 3 kali kali   4096 May 13 16:10 .
drwxr-xr-x 5 kali kali   4096 Oct  5 23:03 ..
-rw-r--r-- 1 kali kali 901390 May  8  2022 17879.txt.utf-8
-rw-r--r-- 1 kali kali 901990 May  8  2022 17880.txt.utf-8
drwxr-xr-x 2 kali kali   4096 May 13 16:11 more_books
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/Etapa Peru/archivos/great_author/acceptable_books]
└─$ cd more_books      
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/archivos/great_author/acceptable_books/more_books]
└─$ ls -la       
total 200
drwxr-xr-x 2 kali kali   4096 May 13 16:11 .
drwxr-xr-x 3 kali kali   4096 May 13 16:10 ..
-rw-r--r-- 1 kali kali 196223 Apr 18  2022 40723.txt.utf-8
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/archivos/great_author/acceptable_books/more_books]
└─$ cd ..        
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/Etapa Peru/archivos/great_author/acceptable_books]
└─$ cd ..
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/Meta/Etapa Peru/archivos/great_author]
└─$  cd adequate_books 
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/Etapa Peru/archivos/great_author/adequate_books]
└─$ ls -la            
total 3928
drwxr-xr-x 3 kali kali    4096 Oct  5 23:03 .
drwxr-xr-x 5 kali kali    4096 Oct  5 23:03 ..
-rw-r--r-- 1 kali kali 1988669 Apr 20  2022 44578.txt.utf-8
-rw-r--r-- 1 kali kali 2017890 Sep  7  2014 46804-0.txt
drwxr-xr-x 3 kali kali    4096 Oct  5 23:02 more_books
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/Etapa Peru/archivos/great_author/adequate_books]
└─$ cd more_books 
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/archivos/great_author/adequate_books/more_books]
└─$ ls -la       
total 1968
drwxr-xr-x 3 kali kali    4096 Oct  5 23:02 .
drwxr-xr-x 3 kali kali    4096 Oct  5 23:03 ..
-rw-r--r-- 1 kali kali 2001199 May  1  2022 1023.txt.utf-8
drwxr-xr-x 3 kali kali    4096 May 13 16:14 .secret
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/archivos/great_author/adequate_books/more_books]
└─$ cd .secret   
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/great_author/adequate_books/more_books/.secret]
└─$ ls    
deeper_secrets
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/great_author/adequate_books/more_books/.secret]
└─$ cd deeper_secrets 
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/adequate_books/more_books/.secret/deeper_secrets]
└─$ ls
deepest_secrets
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/adequate_books/more_books/.secret/deeper_secrets]
└─$ cd deepest_secrets 
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/more_books/.secret/deeper_secrets/deepest_secrets]
└─$ ls                
Oliver_Twist.txt
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/more_books/.secret/deeper_secrets/deepest_secrets]
└─$ cat Oliver_Twist.txt             
fl@g{Ch@rRl3$_D1cK3N$}
                                                                                                                                                                     
┌──(kali㉿kali)-[~/…/more_books/.secret/deeper_secrets/deepest_secrets]
└─$ 

```

```bandera
fl@g{Ch@rRl3$_D1cK3N$}
```