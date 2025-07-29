[DRAFT]

```
 [ISP]
   |
   |
[ROUTER]
   |
   |
  ---
  |S|---{VLAN 1 - 1GbE}---[DMZ - M4 MacMini] 
  |W|---{VLAN 2 - 1GbE}---[HYPERVISOR 1 - M4 MacMini]---{TB 4}------|
  |I|---{VLAN 2 - 1GbE}---[HYPERVISOR 2 - M4 MacMini]---{TB 4}-----||
  |T|---{VLAN 2 - 1GbE}---[HYPERVISOR 3 - M4 MacMini]---{TB 4}----|||
  |C|---{VLAN 2 - 1GbE}---[HYPERVISOR 4 - M4 MacMini]---{TB 4}---||||
  |H|---{VLAN 2 - 1GbE}-----------------------------------------|-----------|
  ---                                                           | MacStudio |
                                                                |   M4 MAX  |
                                                                |-----------|


```
