# CCNA2
My notes at BME for SEM7

duplex full/auto
speed 100/auto
mdix  auto

controllers ethernet-controller  fa0/1 phy | incldue MDIX
show interfaces
show startup-config
show runni 
show flash 
show version
show history 
show ip interface
show ipv6 interface
show mac-address-table 
shwo mac address-table 
show vlan brief

never have late collisons

### 5: STP
IEEE 802.1D 
IEEE MAC Bridging
BPDU
PRORIY |vlan==| MACADDR | PORT PRIORIY | PORTID
|         BID           |
internal root path cost
802.1d
801.1d-2004
802.1w

### 6: EtherChannel
physical -> port channel interface 
PAgP := port aggregation protocal 
LACP := Link aggregation control protocol (802.3ad)
IEEE 802.1AX 

```
VLAN 1 is used for some controll trafic
```
