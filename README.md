# NetwerkDocumentatie
Switch config:
Switch> enable
Switch# configure terminal
Switch(config)# hostname Switch1
Switch1(config)# line console 0
Switch1(config-line)# password PXL
Switch1(config-line)# login
Switch1(config)# line vty 0 4
Switch1(config-line)# password PXL
Switch1(config-line)# login
Switch1(config-line)# transport input telnet
Switch1(config)# enable secret PXL
Switch1(config)# interface vlan 1
Switch1(config-if)# ip address 172.16.1.2 255.255.255.224
Switch1(config-if)# no shutdown
Switch1(config)# ip default-gateway 172.16.1.1

Router config:
Router> enable
Router# configure terminal
Router(config)# hostname Router1
Router1(config)# line console 0
Router1(config-line)# password PXL
Router1(config-line)# login
Router1(config)# line vty 0 4
Router1(config-line)# password PXL
Router1(config-line)# login
Router1(config-line)# transport input telnet
Router1(config)# enable secret PXL
Router1(config)# interface gigabitethernet 0/0
Router1(config-if)# ip address 172.16.1.1 255.255.255.224
Router1(config-if)# no shutdown
