# 📘 ACTIVIDAD 1: Despliegue de DHCP en Entorno Corporativo

## 1. Enunciado
La empresa "TechSolutions" ha abierto una nueva sucursal y te ha contratado como administrador de sistemas.
Se te pide configurar un servidor DHCP en **Ubuntu Server** para gestionar la red local con los siguientes requisitos:

* **Subred:** 192.168.10.0 /24
* **Rango de asignación (Pool):** Desde la IP .50 hasta la .100 (ambas inclusive).
* **Puerta de Enlace (Router):** 192.168.10.1
* **Servidores DNS:** Primario 8.8.8.8, Secundario 8.8.4.4
* **Tiempo de concesión:** 10 minutos (600 segundos).

## 2. Tareas a realizar
1.  Asignar IP estática al servidor.
2.  Instalar el paquete `isc-dhcp-server`.
3.  Configurar el archivo `/etc/dhcp/dhcpd.conf` con los datos proporcionados.
4.  Comprobar que el servicio arranca sin errores.

## 3. Solución Esperada
El archivo `dhcpd.conf` debe contener el siguiente bloque:

```bash
subnet 192.168.10.0 netmask 255.255.255.0 {
    range 192.168.10.50 192.168.10.100;
    option routers 192.168.10.1;
    option domain-name-servers 8.8.8.8, 8.8.4.4;
    default-lease-time 600;
}
