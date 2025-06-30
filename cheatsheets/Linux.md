# SNMP
```
sudo apt update
sudo apt install snmp
```
Validar comunicación contra el target
```
snmpwalk -v2c -c public x.x.x.x
```
> Modificar 'public' por la comunidad correspondiente
---
