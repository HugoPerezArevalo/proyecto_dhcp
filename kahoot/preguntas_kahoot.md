# 🦁 Kahoot: Banco de 50 Preguntas sobre DHCP

**Tema:** Administración de Servicios de Configuración Automática de Red (DHCP)
**Nivel:** Técnico / Administrador Junior

---

## 🟢 Bloque 1: Conceptos Básicos y Protocolo (1-10)

1. **¿Qué significan las siglas DHCP?**
   - Dynamic Host Control Protocol
   - **Dynamic Host Configuration Protocol** ✅
   - Domain Host Control Program
   - Data Host Connection Protocol

2. **¿En qué capa del modelo OSI trabaja DHCP?**
   - Capa 2 (Enlace)
   - Capa 3 (Red)
   - Capa 4 (Transporte)
   - **Capa 7 (Aplicación)** ✅

3. **¿Qué protocolo de transporte utiliza DHCP?**
   - TCP
   - **UDP** ✅
   - ICMP
   - HTTP

4. **¿Cuál es el puerto estándar del SERVIDOR DHCP?**
   - **67** ✅
   - 68
   - 80
   - 53

5. **¿Cuál es el puerto estándar del CLIENTE DHCP?**
   - 67
   - **68** ✅
   - 22
   - 443

6. **¿Cuál es el orden correcto del proceso de negociación?**
   - OFFER - REQUEST - ACK - DISCOVER
   - **DISCOVER - OFFER - REQUEST - ACK (DORA)** ✅
   - REQUEST - OFFER - DISCOVER - ACK
   - HELLO - IP - OK - BYE

7. **El mensaje DHCPDISCOVER se envía a la dirección:**
   - 192.168.1.1
   - 127.0.0.1
   - **255.255.255.255 (Broadcast)** ✅
   - La IP del servidor

8. **¿Qué dirección IP se asigna si falla el DHCP en Windows?**
   - 0.0.0.0
   - **169.254.x.x (APIPA)** ✅
   - 192.168.0.1
   - 10.0.0.1

9. **¿Qué RFC define el protocolo DHCP actual?**
   - RFC 791
   - **RFC 2131** ✅
   - RFC 1918
   - RFC 822

10. **El antecesor del protocolo DHCP fue:**
    - RARP
    - **BOOTP** ✅
    - DNS
    - TELNET

---

## 🟡 Bloque 2: Configuración en Linux (11-20)

11. **¿Cuál es el nombre del paquete del servidor en Ubuntu/Debian?**
    - dhcp-server-linux
    - **isc-dhcp-server** ✅
    - dhcpd-service
    - ubuntu-dhcp

12. **¿Dónde se encuentra el archivo de configuración principal?**
    - /etc/dhcpd.conf
    - **/etc/dhcp/dhcpd.conf** ✅
    - /var/lib/dhcp/config
    - /usr/bin/dhcp/conf

13. **¿Qué archivo define la interfaz de escucha (eth0)?**
    - /etc/network/interfaces
    - /etc/dhcp/interface
    - **/etc/default/isc-dhcp-server** ✅
    - /etc/sysconfig/dhcp

14. **Para definir un rango de IPs usamos la directiva:**
    - pool
    - scope
    - **range** ✅
    - ip-pool

15. **¿Cómo se termina cada línea de instrucción en dhcpd.conf?**
    - Con un punto (.)
    - **Con punto y coma (;)** ✅
    - Con dos puntos (:)
    - Sin nada

16. **La opción para configurar la Puerta de Enlace es:**
    - option gateway
    - **option routers** ✅
    - option default-route
    - option next-hop

17. **La opción para configurar los servidores DNS es:**
    - option dns-server
    - option name-server
    - **option domain-name-servers** ✅
    - option nameservers

18. **¿Qué comando verifica la sintaxis del archivo de configuración?**
    - dhcpd -check
    - systemctl check dhcp
    - **dhcpd -t** ✅
    - verify dhcp

19. **¿Qué significa la directiva 'authoritative'?**
    - Que requiere contraseña root
    - **Que el servidor es la autoridad legítima en la red** ✅
    - Que solo acepta clientes autorizados
    - Que es un servidor secundario

20. **¿En qué unidad se mide el 'default-lease-time'?**
    - Milisegundos
    - Minutos
    - **Segundos** ✅
    - Horas

---

## 🟠 Bloque 3: Administración y Comandos (21-30)

21. **¿Qué comando reinicia el servicio DHCP?**
    - service dhcp start
    - **systemctl restart isc-dhcp-server** ✅
    - /etc/init.d/dhcp reload
    - dhcpd --restart

22. **Si ejecutas `systemctl status` y ves "Active: failed", lo primero es:**
    - Reinstalar Linux
    - **Mirar los logs (journalctl -xe)** ✅
    - Cambiar la tarjeta de red
    - Reiniciar el ordenador

23. **¿Dónde se guarda la base de datos de IPs concedidas (leases)?**
    - /etc/dhcp/leases
    - **/var/lib/dhcp/dhcpd.leases** ✅
    - /var/log/dhcp.log
    - /tmp/leases

24. **Para ver los logs del servicio en tiempo real usamos:**
    - tail -f /var/log/messages
    - **journalctl -u isc-dhcp-server -f** ✅
    - cat /etc/dhcp/dhcpd.conf
    - netstat -puta

25. **¿Qué requisito de red tiene el SERVIDOR DHCP?**
    - Tener acceso a Internet
    - **Tener una IP Estática** ✅
    - Usar IPv6 obligatoriamente
    - Tener dos tarjetas de red

26. **¿Cómo se excluye una IP dentro de un rango?**
    - exclude 192.168.1.50;
    - **No hay comando directo, se divide el 'range' en dos partes** ✅
    - ignore-ip 192.168.1.50;
    - ban 192.168.1.50;

27. **¿Qué comando muestra las IPs de tu máquina?**
    - ifconfig /all
    - **ip a (o ip addr)** ✅
    - show ip
    - get-ip

28. **Si cambias el archivo .conf, ¿qué debes hacer para aplicar cambios?**
    - Nada, es automático
    - **Reiniciar el servicio** ✅
    - Reiniciar el cliente
    - Esperar al lease-time

29. **El usuario que ejecuta el servicio por defecto es:**
    - root
    - **dhcpd** ✅
    - nobody
    - admin

30. **¿Qué significa el error "Not configured to listen on any interfaces"?**
    - Falta el cable de red
    - **No se definió INTERFACESv4 en /etc/default/isc-dhcp-server** ✅
    - El firewall está bloqueando
    - La IP es dinámica

---

## 🔴 Bloque 4: Avanzado, Seguridad y Reservas (31-40)

31. **Para hacer una reserva de IP, necesitamos conocer:**
    - El nombre de usuario
    - **La dirección MAC del dispositivo** ✅
    - La marca del ordenador
    - El puerto del switch

32. **¿Qué directiva define la dirección física en una reserva?**
    - mac-address
    - **hardware ethernet** ✅
    - physical-address
    - eth-addr

33. **¿Qué directiva asigna la IP fija en una reserva?**
    - static-ip
    - set-ip
    - **fixed-address** ✅
    - assign-ip

34. **¿Qué es un "Rogue DHCP"?**
    - Un servidor DHCP optimizado
    - **Un servidor DHCP pirata/no autorizado en la red** ✅
    - Un cliente que pide muchas IPs
    - Un protocolo de seguridad

35. **¿Qué ataque consiste en agotar todas las IPs del pool?**
    - DHCP Spoofing
    - **DHCP Starvation** ✅
    - Man in the Middle
    - DDoS DNS

36. **¿Qué función de los switches protege contra Rogue DHCP?**
    - VLAN Tagging
    - **DHCP Snooping** ✅
    - Port Mirroring
    - Spanning Tree

37. **¿Qué es el 'DHCP Relay Agent'?**
    - Un servidor de respaldo
    - **Un router que reenvía peticiones DHCP entre subredes** ✅
    - Un cliente que actúa de servidor
    - Un software de monitoreo

38. **Si un cliente quiere renovar su IP, envía el mensaje:**
    - DHCPDISCOVER
    - **DHCPREQUEST (Unicast)** ✅
    - DHCPRELEASE
    - DHCPINFORM

39. **¿Podemos asignar diferentes DNS a clientes específicos?**
    - No, es global para todos
    - **Sí, usando la declaración 'host' o 'group'** ✅
    - Solo si usamos VLANs
    - Solo en Windows Server

40. **¿Qué opción se usa para arranque por red (PXE)?**
    - option boot-server
    - **filename "pxelinux.0";** ✅
    - next-server-ip
    - start-file

---

## ⚫ Bloque 5: Situaciones y Troubleshooting (41-50)

41. **Error: "No subnet declaration for eth0 (192.168.1.5)". Causa:**
    - **La IP del servidor no coincide con ninguna 'subnet' configurada** ✅
    - Falta el cable de red
    - El servicio está parado
    - El archivo está vacío

42. **Un cliente tiene la IP 169.254.10.10. ¿Diagnóstico?**
    - Todo funciona bien
    - **No ha logrado contactar con el servidor DHCP** ✅
    - El servidor DNS ha fallado
    - Hay conflicto de IPs

43. **¿Qué pasa si configuras dos DHCP en la misma red con el mismo rango?**
    - Se balancean la carga
    - **Conflicto de IPs duplicadas y caos en la red** ✅
    - El segundo se apaga automáticamente
    - Funcionan en modo Failover

44. **Para limpiar todas las concesiones antiguas, debemos:**
    - Reiniciar el servidor
    - **Borrar el archivo dhcpd.leases y reiniciar** ✅
    - Ejecutar 'dhcpd -clear'
    - Formatear el disco

45. **¿Es posible entregar rutas estáticas por DHCP?**
    - No
    - **Sí, con la 'option static-routes'** ✅
    - Solo la puerta de enlace
    - Solo en IPv6

46. **Si queremos que Windows libere su IP, el comando es:**
    - ipconfig /renew
    - **ipconfig /release** ✅
    - ifconfig down
    - ip flush

47. **Si queremos que Windows pida una IP nueva, el comando es:**
    - **ipconfig /renew** ✅
    - ipconfig /request
    - ipconfig /new
    - dhclient -v

48. **¿Qué hace la opción 'option broadcast-address'?**
    - Define la IP del servidor
    - **Indica a los clientes cuál es la dirección de difusión** ✅
    - Bloquea el tráfico broadcast
    - Reinicia la red

49. **En Wireshark, ¿cómo filtramos el tráfico DHCP?**
    - tcp.port == 67
    - **bootp** ✅ (o dhcp en versiones nuevas)
    - udp.port == 80
    - ip.addr == 192.168.1.1

50. **Para ver si el puerto 67 está abierto en el servidor:**
    - **ss -uln o netstat -uln** ✅
    - ping 127.0.0.1
    - systemctl status
    - cat /etc/services
