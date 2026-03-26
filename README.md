# Implementación de Red Jerárquica con Seguridad SSH

## 🎯 Objetivo
Diseñar una red segmentada en 3 departamentos (Administración, Operaciones e Invitados) utilizando la técnica de **Router-on-a-Stick (RoAS)** y restringir el acceso administrativo mediante **ACLs**.

## 🛠️ Tecnologías Utilizadas
- **Cisco Packet Tracer**
- **VLANs & Trunking (802.1Q)**
- **Inter-VLAN Routing (Subinterfaces)**
- **DHCP Server** (Configurado en Router)
- **Seguridad SSH** con cifrado RSA
- **ACLs Estándar** para control de acceso administrativo

## 🛡️ Implementación de Seguridad
En este laboratorio se aplicó una política de **Menor Privilegio**, donde únicamente los equipos pertenecientes a la **VLAN de Operaciones** tienen permitido el acceso remoto (SSH) al Router principal. Cualquier intento de conexión desde otras VLANs es rechazado automáticamente por el dispositivo.

## 🔍 Comandos Clave Aprendidos
- encapsulation dot1Q [VLAN_ID]
- ip dhcp excluded-address
- access-class [ACL_NAME] in (Aplicado a líneas VTY)
