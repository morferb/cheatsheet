# Validación
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
