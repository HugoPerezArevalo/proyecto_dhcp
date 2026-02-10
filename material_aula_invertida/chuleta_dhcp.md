# 📄 DHCP Cheat Sheet (Hoja de Trucos)

## 📌 Comandos Básicos
| Acción | Comando |
|--------|---------|
| **Instalar** | `sudo apt install isc-dhcp-server` |
| **Editar Config** | `sudo nano /etc/dhcp/dhcpd.conf` |
| **Interfaz** | `sudo nano /etc/default/isc-dhcp-server` |
| **Verificar Sintaxis** | `sudo dhcpd -t` |
| **Reiniciar Servicio** | `sudo systemctl restart isc-dhcp-server` |
| **Ver Estado** | `sudo systemctl status isc-dhcp-server` |
| **Ver Logs** | `journalctl -xeu isc-dhcp-server` |
| **Ver Concesiones** | `cat /var/lib/dhcp/dhcpd.leases` |

## ⚙️ Estructura de `dhcpd.conf`

### 1. Configuración Global
```text
default-lease-time 600;
max-lease-time 7200;
authoritative;

##Declaración de subred
subnet 192.168.10.0 netmask 255.255.255.0 {
    range 192.168.10.50 192.168.10.100;
    option routers 192.168.10.1;
    option domain-name-servers 8.8.8.8;
}


##Reserva de IP fija
host pc_jefe {
    hardware ethernet 00:AA:BB:CC:DD:EE;
    fixed-address 192.168.10.20;
}
