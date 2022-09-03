# Bandit Level 19 → Level 20

## Objetivo
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

## Datos de Acceso
- bandit0.
- bandit0

## Solución 
- ls -la
-  ./bandit20-do id
-  ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
## Notas Adicionales
- si esta activdo el bit setuid, podemos ejecutar a nombre de otro usuario

## Referencias