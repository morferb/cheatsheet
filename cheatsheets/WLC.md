# Comandos WLC Cisco 
## Recursos VM
```
sh platform software system all
```
## Telemetria 
```Verilog
sh telemetry ietf subscription all brief
```
## Licencia
```
sho licence status
```
## CAPWAP
```
show capwap detailed
```
## TS
```
sh ap status
```
> Descripcion: 
```
sh ap summary
```
> Descripcion: 
```
sh ap tag summary
```
> Descripcion: 
```
sh wireless client mac-address
```
> Descripcion: 
```
sh wireless client mac-address <MAC_address> detail
```
> Descripcion: 
```
sh wireless client mac-address <MAC_address> detail | s Client Statistics:|Protocol :|Channel :|AP Name:|AP slot :|Client State :
```
> Descripcion: 
```
sh wireless client mac-address <MAC_address> mobility history
```
> Descripcion: 
```
sh wireless client mac-address <MAC_address> mobility history
```
> Descripcion: 
```
sh wireless client mac-address <MAC_address> mobility history
```
> Descripcion: 
```
sh wireless client mac-address <MAC_address> stats mobility
```
> Descripcion: 
```
sh wireless client summary | include <MAC_address>
```
> Descripcion: 
```
sh wireless client summary detail
```
---
### AAA
```
show aaa servers | i Platform Dead: total|RADIUS: id
```
---
### show logging
```
show logging trace-on-failure summary
```
> Descripcion: 
```
show logging profile wireless trace-on-failure
```
> Descripcion: 
---
### Show wireless
```
show wireless summary
```
> Descripcion: 
```
show wireless stats client detail
```
> Descripcion: 
```
show wireless stats ap join summary
```
> Descripcion: 
```
show wireless stats ap history
```
> Descripcion: 
```
show wireless stats ap discovery
```
> Descripcion: 
```
show wireless mobility summary
```
> Descripcion: 
```
show wireless management trustpoint
```
> Descripcion: 
```
show wireless interface summary
```
> Descripcion: 
```
show wireless dtls connections
```
> Descripcion: 
```
show wireless client summary detail
```
> Descripcion: 
```
show wireless client summary | include <MAC_address>
```
> Descripcion: 
```
show wireless client mac-address <MAC_address> stats mobility
```
> Descripcion: 
```
show wireless client mac-address <MAC_address> mobility history
```
> Descripcion: 
```
show wireless client mac-address <MAC_address> detail | s Client Statistics:|Protocol :|Channel :|AP Name:|AP slot :|Client State :
```
> Descripcion: 
```
show wireless client mac-address <MAC_address> detail
```
> Descripcion: 
```
show wireless client mac-address
```
> Descripcion:
---
### show ap
```
show ap tag summary
```
> Descripcion: 
```
show ap summary
```
> Descripcion: 
```
show ap status
```
> Descripcion: 
```
show ap name <ap-name> tag detail
```
> Descripcion: 
```
show ap name <ap-name> config general | inc AP Mode
```
> Descripcion: 
```
show ap dot11 dual-band summary
```
> Descripcion: 
```
show ap dot11 5ghz load-info
```
> Descripcion:
---
### show ip http
```
show ip http server status | include server status
```
### show crypto pki
```
show crypto pki trustpoint <wlc> status
```
> Descripcion: 
```
show crypto pki trustpoint <TP_Name> status
```
> Descripcion: 
```
show crypto pki trustpoint
```
> Descripcion: 
```
show crypto pki server
```
> Descripcion: 
```
show crypto pki certificate verbose _tp-name_ 
```
> Descripcion:
---
