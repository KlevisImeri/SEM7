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

### 7: DHCPv4 
lease origination

Note: These messages (primarily the DHCPOFFER and DHCPACK) can be sent as
unicast or broadcast according to IETF RFC 2131.
No DHCP-specific router interface configuration is required.
Connection-specific DNS Suffix 

### 8: DHCPv6 RFC 3315 (Client 546 Server 547)
every 200ms RA router
SOLICIT ->
ADVERRISE <-
REQUEST (Stateful everything) / INVOFMATION REQUEST(Stateles .. DNS) ->
REPLY <-

ff02::1:2 multicalt all DHCPv6
ip unicast-routing (act liek a router adn not like a host) 
ipv6 nd other-config-flag
ipv6 nd manages-config-flag
ipv6 nd prefix default no-autoconfig

show ipv6 interface g0/0/1 | begin ND

The ipv6 unicast-routing command is required to enable IPv6 routing. Although
it is not necessary for the router to be a stateless DHCPv6 server, it is
required for the router to source ICMPv6 RA messages.

ipv6 dhcp pool IPC6-STATELESS

dns-server 
domain-name
exit

ipv6 dhcp server poolname

show ipv6 dhcp interface gnan

address prefix 2001:db8:acad:1::/64

siw ipv6 dhcp binding

ipv6 dhcp relay destination 2001:db8:acad:1::2 G0/0/0

Preemption only allows a router to become the active router if it has a higher
priority. A router enabled for preemption, with equal priority but a higher
IPv4 address will not preempt an active router. Refer to the topology in the
figure.
