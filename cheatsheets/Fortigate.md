# Validación
##  Interfaces de red
ICMP
```
execute ping 8.8.8.8  
```
```
execute ping-options source x.x.x.x
```
```
execute ping-options view-settings
```
```
execute ping-options sd-wan yes
```
Ver tabla arp
```
get system arp  
```
```
diagnose ip arp list 
```
## Routing
Ver todas las rutas
```
get router info routing-table all  
```
# Troubleshooting
## Debug
```
diagnose sniffer packet any '' 4 0 l
```
## FLOW #
```bash
diagnose debug disable 
diagnose debug flow trace stop 
diagnose debug flow filter clear 
diagnose debug reset 
diagnose debug flow filter saddr 10.0.1.10
diagnose debug flow filter daddr 8.8.8.8
diagnose debug flow filter dport 
diagnose debug flow show function-name enable
diagnose debug console timestamp enable
diagnose debug flow trace start 999
diagnose debug enable
```
>Stop debug
```bash
diagnose debug disable 
```
---
## IDENTIFICAR ZONA
```Verilog
get router info routing-table details X.X.X.X
```

```Verilog
sh sys zone | grep -f portx.x
```

```Verilog
sh sys int portx.x
```
---
---
## Traffic Shaper
```
show firewall shaper traffic-shaper "XXXX"
```
---
# Configuración
---
## Aplicar Wildcard #
```bash
config firewall address
edit "10.0.X.122/32"
set type wildcard
set associated-interface "XXXX"
set wildcard 10.0.0.122 255.255.0.255
end
GET
```
## IPsec
---
```bash
config vdom
edit xxxx

```
```bash
get vpn ipsec tunnel
```

```bash
get vpn ipsec tunnel summary

```

```bash
get vpn ipsec tunnel summary | grep -v "0/0"

```
---
---
##  Admin Profile
```bash
config system accprofile
    edit "Read_Only"
        set secfabgrp read
        set ftviewgrp read
        set authgrp read
        set sysgrp read
        set netgrp read
        set loggrp read
        set fwgrp read
        set vpngrp read
        set utmgrp read
        set wifi read
    next
end
```
> show system accprofile "Read_Only"
---
---
Muestra la configuración global
```
sh system interface  
```
ver información de la tarjeta
```
get hardware nic [portX]  
```
ver información de la tarjeta
```
diagnose hardware deviceinfo nic [puertoX] grep -f Current_HW 
```
ver versión de forti
```
get system status  
```
Ver policy ID
```
sh firewall policy xxx 
```
ver politica de rutas
```
sh router policy  
```
ver lista de sesiones
```
diagnose system session list  
```
limpia todas las xlate/translations
```
diagnose system session clear  
```
Matar proceso
```
diagnose system kill xxx
```
comprobar si se puede acceder con un usuario de ldap
```
diag test auth ldap  
```
ver stado del ha
```
get system ha status  
```
sincronizar ha
```
execute ha synchronize config  
```
```
execute ha synchronize stop execute ha synchronize start  
```
## Monitoreo y performance
### Link Monitor
```
diagnose sys link-monitor status
```

```
show sys link-monitor
```

```
show full-configuration system link-monitor monitor_l2l_oficina
```

Ver el top de procesos
```
diagnose system top  
```
Mostrar las estadísticas del tráfico hasta el momento:
```
get system performance firewall statistics  
```
Mostrar el estado del CPU y tiempo prendido:
```
get system performance status  
```
Mostrar el uso del CPU ordenado por los procesos de mayor peso
```
get system performance top  
```
## SDWAN
# SNMP
```Verilog
config system snmp sysinfo
    set status enable
end
config system snmp user
    edit "morferb"
        set source-ip \#IP
        set security-level auth-priv
        set auth-pwd \#PASSWORD
        set priv-pwd \#PASSWORD
    next
end
```
# Configurar TACACS SERVER
```Bash
config user tacacs+
edit "morferb_TACACS"
set source-ip #IP_MGMT
set server "X.X.X.X"
set secondary-server "Y.Y.Y.Y"
set key #PASSWORD 
set secondary-key #PASSWORD
set authen-type pap
set authorization enable
next
end
```
# Admin Profile
```JavaScript
config system accprofile
    edit "Read_Only"
        set secfabgrp read
        set ftviewgrp read
        set authgrp read
        set sysgrp read
        set netgrp read
        set loggrp read
        set fwgrp read
        set vpngrp read
        set utmgrp read
        set wifi read
    next
end
```
# Configurar Grupo
```JavaScript
config user group
    edit "FG_RW"
        set member "ISE"
    next
end
```
# PERMISOS/Trusted Host de Usuarios

```JavaScript
config system admin
    edit "usr"
        set remote-auth enable
        set trusthost1 X.X.X.X Y.Y.Y.Y
        set trusthost2 X.X.X.X Y.Y.Y.Y
        set trusthost3 X.X.X.X Y.Y.Y.Y
        set accprofile "Read_Only"
        set vdom "root"
        set wildcard enable
        set remote-group "FG_RW"
    next
end
```
# FORTIGUAR (interface-select-method)
```
config system fortiguard
set interface-select-method sdwan
end
```
>Sirve para que el FortiGate use las interfaces del SD-WAN al consultar los servicios de FortiGuard.



