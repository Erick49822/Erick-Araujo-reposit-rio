
enable
configure terminal
hostname SW-CORE
interface vlan 1
ip address 192.168.0.254 255.255.255.0
no shutdown
description INTERFACE DE GERENCIAMENTO
do wr








enable secret





service-password-encryption




enable
configure terminal
line vty 0 10
password SenhaVTY
exit
enable secret SenhaEnable
do wr










enable
configure terminal
hostname SW-RH
enable secret 49822
banner motd "ACESSO APENAS PARA O DEPARTAMENTO DE TI"
line console 0
password 49822
login
exit
service password-encryption
interface vlan 1
ip address 192.168.0254 255.255.255.0
description INTERFACE DE GERENCIAMENTO
no shutdown
exit
line vty 0 15
password 49822
do wr
