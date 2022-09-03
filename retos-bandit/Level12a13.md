# Bandit Level 12 → Level 13

## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Datos de Acceso
bandit0
bandit0

## Solución  
- ls
- file data.txt
- cat data.txt
- cat data.txt | xxd -r
- cat data.txt | xxd -r | file -
 - cat data.txt | xxd -r | zcat | file -
 - cat data.txt | xxd -r | zcat | bzcat | file -
 - cat data.txt | xxd -r | zcat | bzcat | zcat | file -
 - cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO |file -
 - cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | file -
- cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | file -
 - cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | file -
 - cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
 - cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

## Notas Adicionales
exit  compresion   recompresion  descompresion
gz        gzip               gzip -d              zcat
bzz      bzipz              bzipz -d            bcat
tar       tar                  tar xf                 tar xO

## Referencias 