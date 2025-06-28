# Cisco - Cheatsheet Básico

## Validación

```
show version
```
```
show ip interface brief
```
```
show running-config
```
```
show vlan brief
```
# BGP
## 

```
sh run | s bgp
```
```
sh bgp sum
```

## Ver rutas recibidas desde neighboard
```
sh ip bgp neighbors x.x.x.x received-routes
```
## Ver rutas recibidas desde neighboard
```
sh ip bgp neighbors x.x.x.x received-routes
```
```
conf t
router bgp xxxx
neighbor x.x.x.x route-map xxxx out
end
wr
```
