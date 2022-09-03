# Bandit Level 16 → Level 17

## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Datos de Acceso
- bandit0
- bandit0

## Solución  
- nmap -p31000-32000 localhost
- openssl s_client -connect localhost:31790
- -----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEaysfcTANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjIwOTAxMDYzMDEzWhcNMjIwOTAxMDYzMTEzWjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCW
SLI0BBG+QwOrlYF7amECTNwYr0o8pAzI0D9nA7ENSZ3iQQrPH+OKeFJoYpzg2D+C
eDBIdZbUl+gNF0pb0nlwosHePsoezlk+i7Al3WoICiUN9mc09YVEViI9jVcOcGzO
TZIbeCsmGbvYTN75qXzZ5EqfySHNWwEV8CuOml+VTVlBiteSK76soKuZzTFPRDUB
NOJkO/ZDUpmCZJ0d4Zv6A2+qeuwNCF5OqH+OF2rAwQIKO6oEYPQGDuWlm+WWEF6P
3fz0wnu+ir44iVDYAb37FvsaSgayo5CLmwOsjB/68+lnTgatvnJLVbR3i33hpirV
3QOkkffspxg6veqkjaFFAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBW
/dHgi5TmckCJQclZmOus7FfwwkURutv4BkmWQYGGg4uxgIvTjp3n3k74w0/InnRR
rJQFtRxWcRsuFnheXfW+cZ6n6nZIDgEzI2iLRjy9b5vQDkqK4xL44sWe4/C11D4a
6oYkoBmhWOoKbjHiEiYUMY+iRhbN6EYf18RjsRE7utDfj0KMG2d0EsBDzyBO25un
G/LxkQG1Kr17pf/KFgYifZaCYIFy9uJ/pOqDMJCiMuqpNPjJ0yyLb1FReU9LOm5U
qARBeYIC6kPP8H/tbgT3KHCfp80PTS75feD80UztCOB9gfsrVnoptyN9cc4+jLgm
K0UL8LZEUDnsrDByEcgr
-----END CERTIFICATE-----

- ssh -i llave17 bandit17@bandit.labs.overthewire.org -p 2220
- cat /etc/bandit_pass/bandit17
- VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e

## Notas Adicionales
- nmap escanear puertos

## Referencias