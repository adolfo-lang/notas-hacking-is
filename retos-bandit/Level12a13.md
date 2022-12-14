# Bandit Level 12 → Level 13

## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Datos de Acceso
ssh bandit12@bandit.labs.overthewire.org -p 2220
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

## Solución  
- ls
    data.txt
- file data.txt
     data.txt: ASCII text
- cat data.txt
    00000000: 1f8b 0808 7151 1063 0203 6461 7461 322e  ....qQ.c..data2.
    00000010: 6269 6e00 013f 02c0 fd42 5a68 3931 4159  bin..?...BZh91AY
    00000020: 2653 595d ed11 a800 001b ffff d8ff fde7  &SY]............
    00000030: dff7 ffff ffcf efcf bef7 7e7f dd39 3f7f  ..........~..9?.
	00000040: fafb ffbf cfbf 3eff a9fb bf7f b001 3b1b  ......>.......;.
	00000050: 6d20 0f50 0034 0680 0000 34c2 01ea 0d34  m .P.4....4....4
	00000060: 0000 1900 1a32 1a68 0d00 0000 0034 0000  .....2.h.....4..
	00000070: 000d 0069 91ea 0c6d 5100 0068 00c8 000d  ...i...mQ..h....
	00000080: 0323 4340 3d40 0d0d 1a68 01a3 4c83 401a  .#C@=@...h..L.@.
	00000090: 687a 4034 0340 1a00 3468 0188 c868 34d0  hz@4.@..4h...h4.
	000000a0: 00c8 d01a 6874 d323 40d3 d206 81a1 a680  ....ht.#@.......
	000000b0: d0c8 0190 d034 0340 0d00 c800 01a6 991a  .....4.@........
	000000c0: 0019 3400 d000 0006 800c 4d1a 0189 a001  ..4.......M.....
	000000d0: fc18 2890 6086 162a 8035 6a6b 3d5c 1382  ..(.`..*.5jk=\..
	000000e0: 0a38 e6dd 214b 6fa4 3984 0192 256e e084  .8..!Ko.9...%n..
	000000f0: ed6b ad67 3318 b07a 005d 0e21 dbd1 fb84  .k.g3..z.].!....
	00000100: 770f 055f 0044 3086 8230 d579 2881 afe7  w.._.D0..0.y(...
	00000110: 531e 3071 f859 eeae 01aa 1040 75cd 3c5b  S.0q.Y.....@u.<[
	00000120: f24a 16b8 34e7 43db 9e73 56a1 3d3d fd90  .J..4.C..sV.==..
	00000130: 6bc3 47a5 4c73 af13 a324 5731 b90e 2063  k.G.Ls...$W1.. c
	00000140: 45ef fe11 842e 03f9 b063 8f4c fb41 0a32  E........c.L.A.2
	00000150: 8fdb 7cea 82a0 ee91 4e05 c610 088e a2da  ..|.....N.......
	00000160: 7536 2c72 1701 c248 7ab7 1fef 30f8 142c  u6,r...Hz...0..,
	00000170: 0359 539c 5a21 4e94 6a33 9d18 6120 42a0  .YS.Z!N.j3..a B.
	00000180: 6471 a01e 42a4 da3b 6eaa 5e7e edc3 f973  dq..B..;n.^~...s
	00000190: 2ec7 5009 a7e8 101e a3ac b344 f2bb d9e6  ..P........D....
	000001a0: 7bd7 c5fb 18b6 92ac 9fe8 aef4 673c da0c  {...........g<..
	000001b0: 0cdb 0440 4869 1bd0 7d84 e1e5 85c2 1a60  ...@Hi..}......`
	000001c0: 701c c9ac 50ca adf7 bba9 226f f175 1ec2  p...P....."o.u..
	000001d0: 90de 557e ed09 5c3b 1886 84dc f110 24e7  ..U~..\;......$.
	000001e0: 871b 6148 f224 fb71 c3d1 1096 4a48 48a2  ..aH.$.q....JHH.
	000001f0: 99ea 647b 4f3b ac19 3be6 1cb9 24c3 ce48  ..d{O;..;...$..H
	00000200: 829b 0182 07ef fbee dff1 40da 6f5a c7fb  ..........@.oZ..
	00000210: 5412 78a9 43dd 2198 d456 3c1f e161 2b1f  T.x.C.!..V<..a+.
	00000220: 6e82 f066 70e2 67b8 ec48 d418 3e6a 0ee7  n..fp.g..H..>j..
	00000230: 868a 1dcc e7b0 11ee 8b2a 8c53 0009 37f9  .........*.S..7.
	00000240: 1017 0d29 485a ec30 cb90 45b8 93ff 1772  ...)HZ.0..E....r
	00000250: 4538 5090 5ded 11a8 e965 cb22 3f02 0000  E8P.]....e."?...
- cat data.txt | xxd -r
    i▒▒data2.bin?▒▒BZh91AY&SY]▒▒▒▒▒▒▒▒▒▒▒▒▒▒Ͼ▒~▒9?▒▒▒▒Ͽ>▒▒▒▒▒; P4▒4▒▒
	▒▒▒4▒▒z@4@4h▒▒h4▒▒▒ht▒#@▒▒▒▒▒▒▒▒▒▒4@
	      M▒▒▒(▒`▒*▒5jk=\▒
	8▒▒!Ko▒9▒▒%n▒▒▒k▒g3▒z]!▒▒▒▒w_D0▒▒0▒y(▒▒▒S0q▒Y▒▒@u▒<[▒J▒4▒C۞sV▒==▒▒k▒G▒Ls▒▒$W1▒ cE▒▒▒.▒▒c▒L▒A
	2▒▒|ꂠ▒N▒▒▒u6,r▒Hz▒▒0▒,YS▒Z!N▒j3▒a B▒dq▒B▒▒;n▒^~▒▒▒s.▒P ▒▒▒▒▒D▒▒▒{▒▒▒▒▒▒▒▒▒g<▒
	
	                                                                              ▒@Hi}▒▒▒▒`pɬPʭ▒▒▒"o▒u▒U~▒ \;▒▒▒▒$▒H▒$▒q▒▒▒JHH▒▒▒d{O;▒;▒▒$▒▒H▒▒▒▒▒▒▒▒@▒oZ▒▒Tx▒C▒!▒▒)HZ▒0ːE▒▒▒rE8P▒]▒▒▒e▒"?
- cat data.txt | xxd -r | file -
    /dev/stdin: gzip compressed data, was "data2.bin", last modified: Thu Sep  1 06:30:09 2022, max compression, from Unix
    
 - cat data.txt | xxd -r | zcat | file -
      /dev/stdin: bzip2 compressed data, block size = 900k
      
 - cat data.txt | xxd -r | zcat | bzcat | file -
     /dev/stdin: gzip compressed data, was "data4.bin", last modified: Thu Sep  1 06:30:09 2022, max compression, from Unix
     
 - cat data.txt | xxd -r | zcat | bzcat | zcat | file -
     /dev/stdin: POSIX tar archive (GNU)
     
 - cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO |file -
     /dev/stdin: POSIX tar archive (GNU)
 - cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | file -
- cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | file -
    /dev/stdin: POSIX tar archive (GNU)
    
 - cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | file -
     /dev/stdin: gzip compressed data, was "data9.bin", last modified: Thu Sep  1 06:30:09 2022, max compression, from Unix
     
 - cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
     /dev/stdin: ASCII text
     
 - cat data.txt | xxd -r | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
     The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
     
wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

## Notas Adicionales
exit  compresion   recompresion  descompresion
gz        gzip               gzip -d              zcat
bzz      bzipz              bzipz -d            bcat
tar       tar                  tar xf                 tar xO

## Referencias 