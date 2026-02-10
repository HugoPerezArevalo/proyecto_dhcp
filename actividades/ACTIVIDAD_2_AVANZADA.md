
# 📕 ACTIVIDAD 2: Reservas de IP y Troubleshooting

## 1. Enunciado
El Director General de la empresa se ha quejado de que no puede conectar con su impresora de red porque "la IP cambia cada día".
Se te solicita configurar una **Reserva de IP (DHCP Reservation)** para asegurar que la impresora siempre reciba la misma dirección.

**Datos del dispositivo:**
* **Nombre:** Impresora_Direccion
* **Dirección MAC:** 00:11:22:33:44:55
* **IP Deseada:** 192.168.10.200

## 2. Tareas a realizar
1.  Identificar la dirección MAC del dispositivo.
2.  Editar la configuración DHCP para crear una reserva basada en `hardware ethernet`.
3.  Verificar los logs del sistema para confirmar la asignación.

## 3. Solución Esperada
Añadir el siguiente bloque al final de `dhcpd.conf`:

```bash
host impresora_direccion {
    hardware ethernet 00:11:22:33:44:55;
    fixed-address 192.168.10.200;
}
