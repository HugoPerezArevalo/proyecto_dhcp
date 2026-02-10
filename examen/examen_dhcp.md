# EXAMEN: SERVICIO DHCP EN LINUX
**Nombre:** _________________________________________________
**Fecha:** __________________ **Calificación:** ____________

---

## PARTE 1: TIPO TEST (1 punto cada una)

1. **¿Qué puerto UDP utiliza el SERVIDOR DHCP para escuchar peticiones?**
   a) 68
   b) 67
   c) 80
   d) 53

2. **¿Cuál es el orden correcto del proceso de asignación de IP?**
   a) Offer, Request, Discover, Ack
   b) Discover, Offer, Request, Acknowledge (DORA)
   c) Request, Offer, Ack, Discover
   d) Hello, Offer, Request, Bye

3. **Si un cliente no encuentra servidor DHCP, ¿qué IP se asigna en Windows?**
   a) 192.168.1.1
   b) 0.0.0.0
   c) 169.254.x.x (APIPA)
   d) 127.0.0.1

4. **¿En qué archivo de configuración se define el rango de IPs en Linux?**
   a) /etc/network/interfaces
   b) /etc/dhcp/dhcpd.conf
   c) /etc/default/isc-dhcp-server
   d) /var/lib/dhcp/leases

5. **¿Qué parámetro define el tiempo máximo que un cliente puede tener una IP sin renovar?**
   a) default-lease-time
   b) max-lease-time
   c) renewal-time
   d) dead-time

6. **Para asignar siempre la misma IP a una impresora, necesitamos:**
   a) Su dirección IP actual
   b) Su nombre de host
   c) Su dirección MAC
   d) Su puerto de enlace

7. **¿Qué comando usamos para reiniciar el servicio DHCP en Ubuntu?**
   a) service dhcp start
   b) systemctl restart isc-dhcp-server
   c) /etc/init.d/dhcp restart
   d) dhcpd -restart

8. **¿Qué significa que un servidor sea "authoritative"?**
   a) Que es el único servidor de la red
   b) Que tiene prioridad sobre otros y puede denegar IPs inválidas
   c) Que solo funciona con usuarios root
   d) Que está conectado a Internet

9. **El mensaje DHCPDISCOVER se envía a la dirección IP:**
   a) 192.168.1.1
   b) 255.255.255.255 (Broadcast)
   c) 127.0.0.1 (Loopback)
   d) La IP del servidor si se conoce

10. **¿Dónde se guardan las concesiones (leases) actuales?**
    a) /etc/dhcp/leases
    b) /var/log/syslog
    c) /var/lib/dhcp/dhcpd.leases
    d) /home/usuario/leases

---

## PARTE 2: PREGUNTAS CORTAS Y CASOS PRÁCTICOS

11. Explica brevemente qué es el **Lease Time** y qué ocurre cuando expira el 50% del tiempo.
12. Un cliente recibe la configuración de red pero no puede navegar por Internet. Tiene IP, Máscara y Gateway. ¿Qué parámetro opcional le falta probablemente?
13. Escribe la línea de comando para instalar el servidor DHCP en Debian/Ubuntu.
14. ¿Qué diferencia hay entre `hardware ethernet` y `fixed-address`?
15. Si ejecutas `systemctl status` y ves el error "Not configured to listen on any interfaces", ¿qué archivo debes editar y qué debes poner?
16. ¿Qué es un "Rogue DHCP" y por qué es peligroso?
17. Define qué es un "Scope" o Ámbito.
18. Escribe la configuración para excluir las IPs de la .1 a la .10 dentro de un rango .0 a .100 (Pista: define el rango empezando en .11).
19. ¿Por qué el servidor DHCP necesita tener una IP estática?
20. Interpreta la siguiente línea de log: `DHCPACK on 192.168.1.50 to 00:11:22:33:44:55 via eth0`.

---

## PARTE 3: VERDADERO O FALSO (Justifica las falsas)

21. ( ) El protocolo DHCP funciona sobre TCP para asegurar que los datos llegan bien.
22. ( ) Es posible tener dos servidores DHCP en la misma red si sus rangos no se solapan.
23. ( ) El cliente DHCP utiliza el puerto 67 para enviar datos.
24. ( ) Podemos asignar servidores DNS diferentes a clientes específicos usando reservas.
25. ( ) Si apago el servidor DHCP, los clientes pierden su IP inmediatamente.
26. ( ) El archivo `dhcpd.conf` distingue entre mayúsculas y minúsculas.
27. ( ) La opción `option routers` define la dirección del servidor DNS.
28. ( ) Una reserva de IP puede hacerse sin conocer la MAC del dispositivo.
29. ( ) El comando `dhcpd -t` sirve para arrancar el servidor.
30. ( ) DHCP solo sirve para asignar direcciones IPv4, no existe para IPv6.
