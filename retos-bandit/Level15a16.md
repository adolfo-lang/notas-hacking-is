# Bandit Level 15 → Level 16

## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**

## Datos de Acceso
- ssh bandit15@bandit.labs.overthewire.org -p 2220
- jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt

## Solución  
- openssl s_client -connect localhost:30001
     CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Sep  1 06:31:12 2022 GMT
verify return:1
depth=0 CN = localhost
notAfter=Sep  1 06:31:12 2022 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Sep  1 06:30:12 2022 GMT; NotAfter: Sep  1 06:31:12 2022 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEHn8h8jANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjIwOTAxMDYzMDEyWhcNMjIwOTAxMDYzMTEyWjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDK
u/UD6yArwj259J4o2IVQQGvM/oGVIiYYppFd1jxltmQ03SOUVg+4px+7qOJuCbxA
AH9NCAl55r7v/VDlwGkpu4c2GaqR3zSAlidrtJjrVFZP/QilXdv0uV35N4i30BuT
DdI+FzlYcQx7ztZdtDxp61FTjET4BIcFmSzMQLitpYeeiVcKLXTPnsF8216drWjQ
0Ucb+3RvGgPo/rKPra8/7WYFa8ALdnu2rwP07ndtMDL3iJF9VMuBsr8UuTdsktwa
174QGx0f3RFkcKJ1foxYnSoHvy0BhxVGguMKuinY6cyLELwnjcAp4A2oGI438GnV
whe39ZlCkGved612QLhDAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQDE
2X2mgxYDvujnIAL2Qbs8JnUBFe3lZsRZJbPgko3MZ4lScB5Rbz+vb6q6s0KGGMjh
sKweg4BtG4sQWDIwX2yd4XwJa8rrGWuoA4kgCQ/jJhFZrbCPbDN3sbzX8Tql+epd
oJyQcvLOkWDazRPgx0i4dMXIgUv0kbE+NCvj2waXHldMyjT6GFL2bdv/Xd8ffnXg
wlggJKKIzl0RMp/5z5n1bPMoLVl5HcUG3UzOsTcqcSThTr3JXeWLjaL0qJfAfcw5
V+GM2tGTQB3c4jvISAl5RAARpvFUMc4d4hKd6aesRcFHZfbtSjxglPFmeL1VGxJ9
EIg5c/xwHOE6dgDA2WdS
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: F507AB00493D6E986B6B21C240F63A272847471CEC158A3D8541F13CA0ECD88A
    Session-ID-ctx:
    Resumption PSK: A8375C3E5D1CBE7B0D14A65BE4C4AE6823D19953E66E85D5AC07774488920ED4EDA20F630EC65EF7655DE13FEBADB3A0
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 09 86 a0 aa 25 48 38 1d-0e b1 8d f8 fa 82 ac 33   ....%H8........3
    0010 - b3 cb c0 cc a0 50 1a 0a-6d bb 39 1a 13 64 cc 89   .....P..m.9..d..
    0020 - 7f 91 20 20 ae 72 cd b4-b0 e0 3b 91 be 0c ae e8   ..  .r....;.....
    0030 - 64 a8 2d af 49 2b 26 ee-95 ae 9e c0 03 52 ed 9a   d.-.I+&......R..
    0040 - 88 03 1a 6c a0 89 66 0d-f8 5d 5e bd 93 73 2e 8f   ...l..f..]^..s..
    0050 - 73 cb ae 50 d2 e3 f2 97-29 3f 00 45 81 00 48 59   s..P....)?.E..HY
    0060 - 1f a5 d2 b5 6e c1 dc ad-67 e5 79 a2 82 2d 45 6f   ....n...g.y..-Eo
    0070 - f9 31 ac 61 7c 8c 5c cf-e9 e5 5f 2c 2f 56 74 f6   .1.a|.\..._,/Vt.
    0080 - 61 2c 68 bf 97 73 02 c8-11 f8 8a 90 58 8d f7 00   a,h..s......X...
    0090 - f4 13 6e e2 aa 09 43 eb-e5 95 5a 9d 2c 14 31 25   ..n...C...Z.,.1%
    00a0 - 30 a8 2c ff 2e d0 3f ed-c0 4a a6 67 7e cf e7 c7   0.,...?..J.g~...
    00b0 - 41 52 0e bf 4f 53 61 60-d5 6e 6f a6 e3 c1 fc e7   AR..OSa`.no.....
    00c0 - 16 7c d6 3b 8f 74 06 61-12 22 e2 b6 cf b3 50 37   .|.;.t.a."....P7

    Start Time: 1662237878
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: EFC6C043FB25F914F3EC47400D980CEBFE32FEEFB840BFF43AF9C108355F6C0C
    Session-ID-ctx:
    Resumption PSK: 0C990EBE50717DB4063827955BCD22B21A49C3FD9696076C46F0D614595C6B3D561F5F544F2E7652357AF5C80E5A49E1
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 09 86 a0 aa 25 48 38 1d-0e b1 8d f8 fa 82 ac 33   ....%H8........3
    0010 - d6 c9 e6 37 ab c9 88 e9-53 18 bf e0 ef 71 4f 60   ...7....S....qO`
    0020 - e9 11 e2 8f 9e fe e2 57-14 96 98 a3 3d 5c 8b df   .......W....=\..
    0030 - 74 15 8f 95 a6 21 4d 57-5d d3 37 f4 21 6e c2 26   t....!MW].7.!n.&
    0040 - e9 49 d5 77 51 fc 14 5b-15 e6 d1 0b 4d 80 91 1f   .I.wQ..[....M...
    0050 - c8 09 a9 e0 d3 d9 75 a5-2b 9b cc df 40 85 a8 7b   ......u.+...@..{
    0060 - 9b 6c 9b ac 8a 98 cd c1-6f 33 fc 43 e6 9a 54 36   .l......o3.C..T6
    0070 - 34 86 5a e2 97 64 e3 7f-0b 70 90 33 89 19 b9 8f   4.Z..d...p.3....
    0080 - a2 cb 44 d3 f4 9f 26 75-a3 be 99 f8 a7 ab c2 68   ..D...&u.......h
    0090 - cf a8 e8 23 a6 89 2b d0-7e ca 91 ab dc 92 2d ab   ...#..+.~.....-.
    00a0 - db 2c ce 9b 38 8f cf 06-81 1a 9b 5b a0 fb e2 5c   .,..8......[...\
    00b0 - a9 de 26 a4 00 e7 ce 6c-cd a4 06 48 f7 16 a7 e0   ..&....l...H....
    00c0 - 48 e2 ef 80 ea 4c 94 35-ea d0 02 50 3a b4 29 7c   H....L.5...P:.)|

    Start Time: 1662237878
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
   read R BLOCK

- jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
      Correct!
- JQttfApK4SeyHwDlI9SXGR50qclOAil1

## Notas Adicionales

## Referencias