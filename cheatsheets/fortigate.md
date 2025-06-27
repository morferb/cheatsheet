# Aplicar Wildcard #
```bash
config firewall address
edit "10.111.X.122/32"
set type wildcard
set associated-interface "RESTAURANTES"
set wildcard 10.111.0.122 255.255.0.255
end
GET
```
# FLOW #
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


# FINALIZAR EL DEBUG #
```bash
diagnose debug disable 
```
